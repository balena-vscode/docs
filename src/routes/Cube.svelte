<script lang="ts">
	import { Application } from '@splinetool/runtime';
	import { onMount } from 'svelte';
	import SplineLoader from '@splinetool/loader';
	import * as THREE from 'three';
	import { OrbitControls } from 'three/examples/jsm/controls/OrbitControls.js';

	onMount(async () => {
		let cubeContainer = document.getElementById('cube')!;
		// camera
		const camera = new THREE.PerspectiveCamera(
			45,
			window.innerWidth / 2 / window.innerHeight,
			70,
			100000
		);
		camera.position.set(-924.79, 195.86, 1388.42);
		camera.quaternion.setFromEuler(new THREE.Euler(-0.08, -0.54, -0.04));

		// scene
		const scene = new THREE.Scene();

		// spline scene
		const loader = new SplineLoader();
		loader.load('https://prod.spline.design/KamO0IlCR5qVDcfx/scene.splinecode', (splineScene) => {
			scene.add(splineScene);
		});

		// renderer
		const renderer = new THREE.WebGLRenderer({ antialias: true });
		renderer.setSize(window.innerWidth / 2, window.innerHeight);
		renderer.setAnimationLoop(animate);

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
			console.log('resize');
			camera.aspect = window.innerWidth / window.innerHeight;
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
