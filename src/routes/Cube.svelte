<script lang="ts">
	import { Canvas, InteractiveObject, OrbitControls, Three } from '@threlte/core';
	import { spring } from 'svelte/motion';
	import {
		AmbientLight,
		BoxGeometry,
		CircleGeometry,
		DirectionalLight,
		Group,
		Mesh,
		MeshStandardMaterial,
		PerspectiveCamera
	} from 'three';
	import { degToRad } from 'three/src/math/MathUtils';
	import { GLTF } from '@threlte/extras';
	import { Application } from '@splinetool/runtime';
	import { onMount } from 'svelte';

	let canvas: any;
	onMount(() => {
		const app = new Application(canvas!);
		app.load('https://prod.spline.design/KamO0IlCR5qVDcfx/scene.splinecode');
	});

	const scale = spring(1);
</script>

<div>
	<canvas bind:this={canvas} />
</div>

<style>
	div {
		height: 100%;
		width: 100%;
	}
</style>
