<script>
	import '../app.css';
	import { page } from '$app/stores';
</script>

<header>
	<a href="/" class="balena_logo">
		<picture>
			<source srcset="balena_icon.svg" type="image/svg+xml" />
			<img width="50px" height="50px" alt="Balena logo" src="balena_icon.svg" />
		</picture>
		<h2>Balena (unoffical)</h2>
	</a>
	<div class="links">
		<h2 class="docs">
			<a href="/docs" class:active={$page.url.pathname === '/docs'}>Docs</a>
		</h2>
		<a rel="noreferrer" target="_blank" href="https://github.com/balena-vscode/balena-vscode">
			<svg
				class="github_logo"
				role="img"
				id="Layer_1"
				xmlns="http://www.w3.org/2000/svg"
				viewBox="0 0 100 97.53"
			>
				<title>GitHub Logo</title>
				<defs /><path
					class="cls-2"
					d="M50,0C22.39,0,0,22.38,0,50c0,22.09,14.33,40.83,34.19,47.44,2.5,.46,3.42-1.09,3.42-2.41,0-1.19-.05-5.13-.07-9.31-13.91,3.02-16.85-5.9-16.85-5.9-2.27-5.78-5.55-7.32-5.55-7.32-4.54-3.1,.34-3.04,.34-3.04,5.02,.35,7.66,5.15,7.66,5.15,4.46,7.64,11.7,5.43,14.55,4.16,.45-3.23,1.74-5.44,3.17-6.69-11.11-1.26-22.78-5.55-22.78-24.71,0-5.46,1.95-9.92,5.15-13.42-.52-1.26-2.23-6.34,.48-13.23,0,0,4.2-1.34,13.75,5.13,3.99-1.11,8.27-1.66,12.52-1.68,4.25,.02,8.53,.57,12.53,1.68,9.54-6.47,13.74-5.13,13.74-5.13,2.72,6.89,1.01,11.97,.49,13.23,3.21,3.5,5.15,7.96,5.15,13.42,0,19.2-11.7,23.43-22.83,24.67,1.79,1.55,3.39,4.59,3.39,9.26,0,6.69-.06,12.07-.06,13.72,0,1.33,.9,2.89,3.43,2.4,19.86-6.62,34.16-25.35,34.16-47.44C100,22.38,77.61,0,50,0Z"
				/><path
					class="cls-1"
					d="M18.94,71.79c-.11,.25-.5,.32-.86,.15-.36-.16-.57-.5-.45-.75,.11-.26,.5-.33,.86-.16,.36,.16,.57,.51,.44,.75h0Zm-.62-.46"
				/><path
					class="cls-1"
					d="M20.96,74.05c-.24,.22-.71,.12-1.02-.23-.33-.35-.39-.82-.15-1.04,.25-.22,.7-.12,1.03,.23,.33,.35,.39,.82,.14,1.04h0Zm-.48-.51"
				/><path
					class="cls-1"
					d="M22.93,76.93c-.31,.21-.81,.01-1.12-.43-.31-.44-.31-.98,0-1.19,.31-.21,.8-.02,1.12,.42,.31,.45,.31,.99,0,1.2h0Zm0,0"
				/><path
					class="cls-1"
					d="M25.64,79.71c-.27,.3-.86,.22-1.28-.19-.44-.4-.56-.98-.28-1.28,.28-.3,.87-.22,1.3,.19,.43,.4,.57,.98,.27,1.28h0Zm0,0"
				/><path
					class="cls-1"
					d="M29.36,81.33c-.12,.39-.68,.57-1.25,.4-.57-.17-.94-.63-.82-1.03,.12-.39,.68-.58,1.25-.4,.57,.17,.94,.63,.82,1.02h0Zm0,0"
				/><path
					class="cls-1"
					d="M33.45,81.62c.01,.41-.47,.75-1.06,.76-.6,.01-1.08-.32-1.09-.73,0-.42,.47-.75,1.07-.76,.59-.01,1.08,.32,1.08,.73h0Zm0,0"
				/><path
					class="cls-1"
					d="M37.26,80.98c.07,.4-.34,.82-.93,.93-.58,.11-1.12-.14-1.19-.54-.07-.41,.35-.83,.93-.93,.59-.1,1.12,.14,1.2,.55h0Zm0,0"
				/></svg
			>
		</a>
	</div>
</header>

<main>
	<slot />
</main>

<style>
	header {
		display: flex;
		flex-direction: row;
		justify-content: space-between;
		width: 90vw;
		margin-top: 16px;
		align-items: center;
		max-width: 1440px;
		padding-bottom: 15px;
		border-bottom: 1px solid rgb(56, 56, 56);
	}
	header h2 {
		font-size: 18px;
	}

	.docs {
		margin-right: 20px;
	}

	a {
		color: white;
		text-decoration: none;
	}

	a:hover {
		color: #ffc100;
	}

	a:active {
		color: #ffc100;
	}
	.links {
		display: flex;
		flex-direction: row;
		margin-right: 0;
	}

	main {
		width: 90vw;
		height: 80vh;
		text-align: center;
		max-width: 1440px;
	}
	.github_logo {
		width: 30px;
		height: 30px;
		fill: white;
	}

	.github_logo:hover {
		fill: #ffc100;
	}

	.balena_logo {
		display: flex;
		flex-direction: row;
		margin-left: 0;
		align-items: center;
	}

	.balena_logo img {
		width: 20px;
		height: 20px;
		margin-right: 8px;
	}

	.balena_logo h2 {
		margin: 0;
	}

	@media (min-width: 768px) {
		.github_logo {
			width: 30px;
			height: 30px;
		}

		.balena_logo img {
			width: 30px;
			height: 30px;
			margin-right: 16px;
		}
		.docs {
			margin-right: 40px;
		}
	}

	@media (min-width: 1024px) {
		header {
			margin-top: 30px;
			width: 85vw;
		}

		main {
			width: 85vw;
		}
	}
</style>
