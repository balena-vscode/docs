<div class="title">
	<h1>Manage your IoT devices without leaving your workspace</h1>
	<h3>Unoffical VS Code extenstion for integration with Balena</h3>
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
	<picture>
		<source src="balena-asset-simple.png" type="png" />
		<img
			class="balena-asset"
			alt="extension visualization in VS code"
			src="balena-asset-simple.png"
		/>
	</picture>
</div>
<div class="cards">
	<div class="card">
		<picture>
			<source src="summary.svg" type="svg/xml" />
			<img alt="list icon" src="summary.svg" />
		</picture>
		<div>
			<h3 class="card_title">Summary</h3>
			<p class="card_text">
				View a rich, interactive summary. Common information and state is easily copied, toggled, or
				updated
			</p>
		</div>
	</div>
	<div class="card">
		<picture>
			<source src="devices.svg" type="svg/xml" />
			<img alt="list icon" src="devices.svg" />
		</picture>
		<div>
			<h3 class="card_title">Devices</h3>
			<p class="card_text">Easily view and filter your devices for the active fleet</p>
		</div>
	</div>
	<div class="card">
		<picture>
			<source src="verified.svg" type="svg/xml" />
			<img alt="list icon" src="verified.svg" />
		</picture>
		<div>
			<h3 class="card_title">Releases</h3>
			<p class="card_text">View and filter your releases, see build status, and list services</p>
		</div>
	</div>
	<div class="card">
		<picture>
			<source src="wrench.svg" type="svg/xml" />
			<img alt="list icon" src="wrench.svg" />
		</picture>
		<div>
			<h3 class="card_title">Services</h3>
			<p class="card_text">View service status, logs, and control status</p>
		</div>
	</div>
	<div class="card">
		<picture>
			<source src="variable.svg" type="svg/xml" />
			<img alt="list icon" src="variable.svg" />
		</picture>
		<div>
			<h3 class="card_title">Variables</h3>
			<p class="card_text">View and edit your fleet wide or device variables</p>
		</div>
	</div>
	<div class="card">
		<picture>
			<source src="metadata.svg" type="svg/xml" />
			<img alt="list icon" src="metadata.svg" />
		</picture>
		<div>
			<h3 class="card_title">Metadata</h3>
			<p class="card_text">
				Can’t find the information you need in any view? View the entirety of an SDK model’s meta!
			</p>
		</div>
	</div>
</div>
<div class="contribute">
	<h3>
		Want to contribute? Check out <a
			rel="noreferrer"
			target="_blank"
			href="https://github.com/balena-vscode/balena-vscode/blob/main/CONTRIBUTING.md"
			>CONTRIBUTING.md</a
		> in the repo
	</h3>
</div>

<style>
	h1 {
		font-size: 20px;
	}
	h3 {
		margin-top: 0;
		font-size: 14px;
		color: #222832;
	}

	a {
		color: #ffc100;
	}

	p {
		color: #222832;
	}
	.title {
		width: 90%;
		margin-top: 30px;
	}

	.balena-asset {
		width: 90vw;
		max-width: 1440px;
	}

	button {
		width: 120px;
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

	.cards {
		display: flex;
		flex-direction: row;
		flex-wrap: wrap;
		margin: 0;
		margin-top: 58px;
	}

	.card {
		display: flex;
		flex-direction: row;
		margin-top: 8px;
		height: 120px;
		width: 100%;
		justify-content: unset;
	}

	.card div {
		display: block;
		text-align: left;
		margin: 0;
	}

	.card h3 {
		font-size: 18px;
		margin-bottom: 0px;
		margin-top: 8px;
	}

	.card p {
		font-size: 16px;
		margin-top: 8px;
	}

	.card img {
		width: 40px;
		margin-right: 16px;
	}

	.contribute {
		margin-top: 150px;
		margin-bottom: 100px;
	}

	@media (min-width: 768px) {
		h1 {
			font-size: 40px;
		}
		h3 {
			font-size: 24px;
		}

		button {
			width: 180px;
			height: 50px;
			font-size: 24px;
			margin: 16px;
		}

		.card {
			border: #ffc100 solid 2px;
			border-radius: 10px;
			display: flex;
			flex-direction: row;
			padding: 8px 16px;
			width: 43%;
			margin-top: 16px;
			height: 140px;
		}

		.card div {
			width: 80%;
		}

		.card h3 {
			font-size: 26px;
		}

		.card p {
			font-size: 18px;
		}

		.card img {
			width: 60px;
		}
	}
	@media (min-width: 1024px) {
		.title {
			width: 80%;
		}

		.balena-asset {
			width: 60vw;
		}
		.card {
			height: 120px;
		}
	}

	@media (min-width: 1440px) {
		.title {
			width: 50%;
		}
	}
</style>
