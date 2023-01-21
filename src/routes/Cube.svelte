<script lang="ts">
	import { Application } from '@splinetool/runtime';
	import { onMount } from 'svelte';
	import SplineLoader from '@splinetool/loader';
	import * as THREE from 'three';
	import { OrbitControls } from 'three/examples/jsm/controls/OrbitControls.js';

	onMount(async () => {
		// camera
		const camera = new THREE.OrthographicCamera(
			window.innerWidth / -4,
			window.innerWidth / 4,
			window.innerHeight / 4,
			window.innerHeight / -4,
			-200000,
			200000
		);
		camera.position.set(-678.52, 230.73, 736.38);
		camera.quaternion.setFromEuler(new THREE.Euler(-0.19, -0.66, -0.12));

		// scene
		const scene = new THREE.Scene();

		// spline scene
		const loader = new SplineLoader();
		loader.load('https://prod.spline.design/KamO0IlCR5qVDcfx/scene.splinecode', (splineScene) => {
			scene.add(splineScene);
		});

		// renderer
		const renderer = new THREE.WebGLRenderer({ antialias: true });
		renderer.setSize(window.innerWidth / 2, window.innerHeight / 2);
		renderer.setAnimationLoop(animate);
		let cubeContainer = document.getElementById('cube')!;
		cubeContainer.appendChild(renderer.domElement);

		// scene settings
		renderer.shadowMap.enabled = true;
		renderer.shadowMap.type = THREE.PCFShadowMap;

		scene.background = new THREE.Color('#11151c');
		renderer.setClearAlpha(1);

		// orbit controls
		const controls = new OrbitControls(camera, renderer.domElement);
		controls.enableDamping = true;
		controls.dampingFactor = 0.125;

		window.addEventListener('resize', onWindowResize);
		function onWindowResize() {
			camera.left = window.innerWidth / -2;
			camera.right = window.innerWidth / 2;
			camera.top = window.innerHeight / 2;
			camera.bottom = window.innerHeight / -2;
			camera.updateProjectionMatrix();
			renderer.setSize(window.innerWidth / 2, window.innerHeight);
		}

		function animate(time) {
			controls.update();
			renderer.render(scene, camera);
		}
	});
</script>

<div>
	<!-- <canvas bind:this={canvas} /> -->
</div>

<style>
	div {
		height: 100%;
		width: 100%;
	}
</style>
