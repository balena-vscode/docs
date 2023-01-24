<div class="header">
	<div class="title">
		<h1>Manage your IoT devices without leaving your workspace</h1>
		<h2>Unoffical VS Code extenstion for use with Balena</h2>
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
	<div id="cube">
		<iframe
			title="interactive 3d cube"
			src="https://my.spline.design/iframecubecopy-8dbbb6e86305ccc8e567a450cf015c2e/"
			frameborder="0"
		/>
	</div>
</div>

<style>
	/* .cube {
		height: 15em;
		width: 15em;
	} */
	iframe {
		width: 300px;
		height: 300px;
	}
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
		/* margin-bottom: 0; */
	}

	.header {
		flex-direction: column;
		margin-top: 50px;
	}

	button {
		display: inline-block;
		width: 120px;
		height: 30px;
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
		border: solid 1px #f5faff;
		cursor: pointer;
	}

	.buttons {
		display: flex;
		flex-direction: row;
		margin-top: 20px;
		width: 100%;
	}

	/* .vs-button {
		background: rgb(255, 150, 14);
		background: linear-gradient(180deg, rgba(255, 150, 14, 1) 0%, rgba(255, 241, 118, 1) 100%);
		color: #222832;
	} */

	@media (min-width: 768px) {
		h1 {
			font-size: 40px;
		}
		h2 {
			font-size: 22px;
		}

		button {
			width: 160px;
			height: 40px;
			font-size: 20px;
			margin: 16px;
		}
		.header {
			margin-top: 80px;
		}
		.title {
			max-width: 600px;
		}

		iframe {
			width: 500px;
			height: 500px;
		}
	}
	@media (min-width: 1024px) {
		h1 {
			font-size: 35px;
		}
		h2 {
			font-size: 20px;
		}
		.title {
			width: 80%;
			text-align: left;
			max-width: 500px;
			justify-items: left;
			justify-content: start;
		}

		.buttons {
			justify-content: left;
			text-align: left;
		}
		button {
			margin: 16px 16px 16px 0;
		}
		.header {
			flex-direction: row;
		}

		h2 {
			width: 100%;
		}
	}

	@media (min-width: 1440px) {
		.title {
			width: 50%;
		}
	}
</style>
