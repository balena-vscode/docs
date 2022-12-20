<div class="header">
	<div class="title">
		<h1>Manage your IoT devices without leaving your workspace</h1>
		<h2>Unoffical VS Code extenstion for integration with Balena</h2>
		<div class="buttons">
			<a
				rel="noreferrer"
				target="_blank"
				href="https://marketplace.visualstudio.com/items?itemName=kalebpace.balena-vscode"
			>
				<button class="vs-button" type="button">VS Marketplace</button>
			</a>
			<a
				rel="noreferrer"
				target="_blank"
				href="https://open-vsx.org/extension/kalebpace/balena-vscode"
			>
				<button class="vsx-button" type="button">Open VSX</button>
			</a>
		</div>
	</div>
	<div>
		<h1>Image Placeholder</h1>
	</div>
</div>

<style>
	h1 {
		font-size: 24px;
	}
	h2 {
		margin-top: 0;
		font-size: 16px;
		color: #d9d9d9;
	}

	.title {
		max-width: 400px;
	}

	.header {
		flex-direction: column;
		height: 100%;
	}

	button {
		display: inline-block;
		width: 130px;
		height: 31px;
		font-weight: 700;
		font-size: 16px;
		border-radius: 5px;
		border: none;
		outline: none;
		margin: 8px;
		background: #222832;
		color: white;
	}

	button:hover {
		opacity: 0.7;
	}

	.buttons {
		display: flex;
		flex-direction: row;
		margin-top: 20px;
	}

	.vs-button {
		background: rgb(255, 150, 14);
		background: linear-gradient(180deg, rgba(255, 150, 14, 1) 0%, rgba(255, 241, 118, 1) 100%);
		color: #222832;
	}

	@media (min-width: 768px) {
		h1 {
			font-size: 40px;
		}
		h2 {
			font-size: 22px;
		}

		button {
			width: 180px;
			height: 50px;
			font-size: 24px;
			margin: 16px;
		}
		.title {
			max-width: 600px;
		}
	}
	@media (min-width: 1024px) {
		.title {
			width: 80%;
		}
		.header {
			flex-direction: row;
			/* width: 85%; */
		}
	}

	@media (min-width: 1440px) {
		.title {
			width: 50%;
		}
	}
</style>
