<script>
	export let alt;
	export let width;
	export let height;
	export let title;
	export let tagline;
	export let logotype;
	export let background;
</script>

<section class="hero-banner">
	<div class="hero-container">
		<div class="hero-text">
			<img alt="{title} logotype" width="400" height="50" class="logotype" src={logotype} />
			<h3>{tagline}</h3>
		</div>

		<div class="hero-image">
		<picture>
			<source srcset="{background}.webp">
			<img {alt} {width} {height} src="{background}.png">
		</picture>
	</div>
	</div>
</section>

<style>
	.hero-banner {
		max-width: 100vw;
		background: rgb(211, 214, 217);
		background: radial-gradient(34.14% 72.25% at 47.58% 31.75%, rgba(232, 244, 255, 0.52) 0%, rgba(255, 255, 255, 0) 100%),
linear-gradient(92.4deg, #D1D4D7 14.67%, rgba(238, 247, 255, 0.48) 54.37%, rgba(206, 216, 224, 0.62) 92.49%),
linear-gradient(0deg, #DBE7EF, #DBE7EF);
		position: relative;
		padding: 8rem var(--side-nav) 0;
		display: flex;
		justify-content: flex-start;
		align-items: center;
		overflow: hidden;
	}

	.hero-container {
		width: 100%;
		max-width: 90rem;
		margin: 0 auto;
		/* display: flex; */
		justify-content: center;
	}

	.hero-text {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		mix-blend-mode: multiply;
	}

	.hero-banner h3 {
		margin-top: 0;
		position: relative;
		font-size: 2rem;
		font-weight: 200;
		line-height: 1.2;
		letter-spacing: 0.1em;
		text-align: center;
		text-transform: uppercase;
		color: var(--text);
		max-width: 12em;
	}

	.logotype {
		position: relative;
		width: 100%;
		max-width: 400px;
		margin: 0 0 2rem 0;
	}

	.hero-image {
		display: flex;
		flex: 1;
		justify-content: center;
		align-items: center;
	}

	picture img {
		width: 600px;
		object-fit: contain;
		transform: translate(-2%,0);
	}

	@media (min-width: 480px) {
		.hero-banner h3 {
			max-width: auto;
		}

		picture img {
			width: 800px;
			object-fit: contain;
			transform: translate(-2%,0);
		}
	}

	@media (min-width: 1024px) {
		.hero-banner {
			padding: 0 var(--side-nav);
		}

		.hero-text {
			margin-top: -10rem;
			align-items: flex-end;
			flex: 1;
		}

		.hero-image {
			flex: 1.2;
		}

		.hero-image img {
			width: 480px;
			transform: translate(0,10%) scale(1.8);
		}

		.hero-banner h3 {
			text-align: right;
			max-width: 12em;
		}

		.hero-container {
			height: 70vh;
			display: flex;
			justify-content: flex-start;
			margin: 0 auto;
			padding: 0;
		}
	}
</style>
