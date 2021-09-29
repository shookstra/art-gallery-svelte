<script>
	import { fade } from "svelte/transition";
	import Sidebar from "./components/Sidebar.svelte";
	import Loading from "./components/Loading.svelte";

	let displayingPhoto = false;
	let imgSrc = "";

	const setPhoto = (imgPath) => {
		imgSrc = imgPath;
		displayingPhoto = true;
	};
</script>

<main>
	<Loading />
	<Sidebar />
	<ul class="posts">
		{#if displayingPhoto}
			<div id="modal" transition:fade={{ duration: 200 }}>
				<span class="modal-background" />
				<div class="photo-modal">
					<button
						class="photo-modal-close-btn"
						on:click={() => {
							displayingPhoto = false;
						}}>&#215;</button
					>
					<img alt="placeholder" id="photo-modal-img" src={imgSrc} />
				</div>
			</div>
		{/if}
		<h1 class="year-header" id="2021">2021</h1>
		<li class="post">
			<h2>Field of Flowers III</h2>
			<img
				src="/images/FieldOfFlowersIIICompressed(finished).webp"
				alt="A painting of a field of flowers"
				class="post-img"
				on:click={() =>
					setPhoto(
						"images/FieldOfFlowersIIICompressed(finished).webp"
					)}
			/>
			<div class="small-pics">
				<img
					src="/images/FieldOfFlowersIIICompressed(unfinished).webp"
					alt="An unfinished painting of a field of flowers"
					class="small-pic"
					on:click={() =>
						setPhoto(
							"images/FieldOfFlowersIIICompressed(unfinished).webp"
						)}
				/>
			</div>
			<div class="post-description">
				<p>A gift for a friend. Happy birthday 🎉.</p>
				<p>Acrylic on canvas.</p>
				<p>Late September 2021</p>
			</div>
		</li>
		<li class="post">
			<h2>Kettle</h2>
			<img
				src="/images/Kettle(compressed).webp"
				alt="A painting of an orange and yellow kettle with flowers on it."
				class="post-img"
				on:click={() => setPhoto("images/Kettle(compressed).webp")}
			/>
			<div class="post-description">
				<p>
					Inspired by another painting with a poem attached. I liked
					the style and wanted to sort of recreate it. I don't have
					the source anymore, but if I ever find it again I will
					update this post with a link.
				</p>
				<p>Acrylic on canvas.</p>
				<p>Mid August 2021</p>
			</div>
		</li>
		<li class="post">
			<h2>Field of Flowers II</h2>
			<img
				src="/images/FlowersII(compressed).webp"
				alt="A painting of an orange and yellow kettle with flowers on it."
				class="post-img"
				Loading="lazy"
				on:click={() => setPhoto("images/FlowersII(compressed).webp")}
			/>
			<div class="post-description">
				<p>A field of flowers. Part two of a series</p>
				<p>Acrylic on canvas.</p>
				<p>Early August 2021</p>
			</div>
		</li>
		<li class="post">
			<h2>Momtez</h2>
			<img
				src="/images/momtez-finished.webp"
				alt="A portrait of Momtez"
				loading="lazy"
				class="post-img"
				on:click={() => setPhoto("images/momtez-finished.webp")}
			/>
			<div class="small-pics">
				<img
					src="/images/momtez-drawing.webp"
					alt="An initial drawing of Momtez."
					class="small-pic"
					on:click={() => setPhoto("images/momtez-drawing.webp")}
				/>
				<picture class="small-pic">
					<source
						data-srcset="/images/momtez-unfinished-1.webp"
						type="image/webp"
					/>
					<img
						src="/images/momtez-unfinished-1.webp"
						alt="An unfinished portrait of Momtez."
						on:click={() =>
							setPhoto("images/momtez-unfinished-1.webp")}
					/>
				</picture>
				<img
					src="/images/momtez-unfinished-2.webp"
					alt="An unfinished portrait of Momtez 2."
					class="small-pic"
					loading="lazy"
					on:click={() => setPhoto("images/momtez-unfinished-2.webp")}
				/>
				<img
					src="/images/momtez-unfinished-3.webp"
					alt="An unfinished portrait of Momtez 3."
					class="small-pic"
					loading="lazy"
					on:click={() => setPhoto("images/momtez-unfinished-3.webp")}
				/>
				<img
					src="/images/momtez-unfinished-angle.webp"
					alt="An unfinished portrait of Momtez at an angle to show texture."
					class="small-pic"
					loading="lazy"
					on:click={() =>
						setPhoto("images/momtez-unfinished-angle.webp")}
				/>
				<img
					src="/images/momtez-unfinished-wall.webp"
					alt="An unfinished portrait of Momtez displayed on the wall."
					class="small-pic"
					loading="lazy"
					on:click={() =>
						setPhoto("images/momtez-unfinished-wall.webp")}
				/>
			</div>
			<div class="post-description">
				<p>
					A commision portrait piece. Credit to Renee for naming this
					one.
				</p>
				<p>Acrylic on canvas.</p>
				<p>February 2021</p>
			</div>
		</li>
		<li class="post">
			<h2>Snowy Building</h2>
			<img
				src="/images/snowy-buildings.webp"
				alt="A painting of snowy buildings"
				class="post-img"
				on:click={() => setPhoto("images/snowy-buildings.webp")}
			/>
			<div class="post-description">
				<p>
					Inspired by a reddit post. Link posted soon. Created
					entirely using a palette knife.
				</p>
				<p>Acrylic on canvas</p>
				<p>February 2021.</p>
			</div>
		</li>
		<li class="post">
			<h2>Field of Flowers I</h2>
			<img
				src="/images/flowers.webp"
				alt="A painting of snowy buildings"
				class="post-img"
				loading="lazy"
				on:click={() => setPhoto("images/flowers.webp")}
			/>
			<div class="post-description">
				<p>A field of flowers. Part one of a series.</p>
				<p>Febrary 2021.</p>
				<p>Acrylic on canvas</p>
			</div>
		</li>
		<li class="post">
			<h2>Lemon</h2>
			<img
				src="/images/lemon.webp"
				alt="A painting of snowy buildings"
				class="post-img"
				loading="lazy"
				on:click={() => setPhoto("images/lemon.webp")}
			/>
			<div class="small-pics">
				<img
					src="/images/real-lemon.webp"
					alt="A painting of snowy buildings"
					class="small-pic"
					loading="lazy"
					on:click={() => setPhoto("images/real-lemon.webp")}
				/>
			</div>
			<div class="post-description">
				<p>
					Still life painting of a lemon. Plate and lemon done
					completely with a palette knife.
				</p>
				<p>Acrylic on canvas</p>
				<p>January 2021.</p>
			</div>
		</li>
		<h1 class="year-header" id="2020">2020</h1>
		<li class="post">
			<h2>Cloud Series</h2>
			<img
				src="/images/pink-cloud.webp"
				alt="A painting of snowy buildings"
				class="post-img"
				loading="lazy"
				on:click={() => setPhoto("images/pink-cloud.webp")}
			/>
			<img
				src="/images/orange-cloud-1.webp"
				alt="A painting of snowy buildings"
				class="post-img"
				loading="lazy"
				on:click={() => setPhoto("images/orange-cloud-1.webp")}
			/>
			<div class="post-description">
				<p>Series of three works. Clouds. More pictures to come.</p>
				<p>Acrylic on canvas</p>
				<p>December 2020.</p>
			</div>
		</li>
		<li class="post">
			<h2>Treeline</h2>
			<img
				src="/images/treeline.webp"
				alt="A painting of snowy buildings"
				class="post-img"
				loading="lazy"
				on:click={() => setPhoto("images/treeline.webp")}
			/>
			<div class="post-description">
				<p>Night sky and treeline. First painting since 2017.</p>
				<p>Acrylic on canvas</p>
				<p>December 2020.</p>
			</div>
		</li>
	</ul>
</main>

<style>
	@import url("https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500&display=swap");
	main {
		/* padding: 10px; */
		display: flex;
		width: 80%;
		height: 100%;
		margin: 0px auto;

		/* border: 3px solid red; */
	}

	.posts {
		/* border: 2px solid slateblue; */
		/* background-color: #d9d9d9; */
		list-style: none;
		flex: 3;
		margin: 50px 5px 5px 400px;
	}

	.post {
		padding: 15px;
		/* border: 3px solid yellow; */
	}

	img {
		object-fit: cover;
		object-position: center;
		height: 100%;
		width: 100%;
		border-radius: 10px;
		cursor: pointer;
		-webkit-box-shadow: 0 10px 6px -6px rgba(0, 0, 0, 0.35);
		-moz-box-shadow: 0 10px 6px -6px rgba(0, 0, 0, 0.35);
		box-shadow: 0 10px 6px -6px rgba(0, 0, 0, 0.35);
	}

	.post-img {
		background-color: #7fd1b9;
		margin-top: 10px;
		object-fit: cover;
		object-position: center;
		height: 400px;
		width: 400px;
		border-radius: 10px;
		-webkit-box-shadow: 0 10px 6px -6px rgba(0, 0, 0, 0.35);
		-moz-box-shadow: 0 10px 6px -6px rgba(0, 0, 0, 0.35);
		box-shadow: 0 10px 6px -6px rgba(0, 0, 0, 0.35);
	}

	.small-pics {
		display: flex;
		max-width: 500px;
		padding: 0px 5px 0px 0px;
		overflow-x: auto;
		overflow-y: hidden;
		justify-content: space-between;
		align-items: flex-start;
		margin-bottom: 5px;
		height: 180px;
		/* border: 1px solid red; */
	}

	.small-pic {
		/* flex: 1; */
		object-fit: cover;
		object-position: center;
		height: 150px;
		width: 200px;
		min-height: 125px;
		min-width: 125px;
		border-radius: 10px;
		padding: 5px 5px 5px 0px;
		margin: 0;
		-webkit-box-shadow: 0 10px 6px -6px rgba(0, 0, 0, 0.35);
		-moz-box-shadow: 0 10px 6px -6px rgba(0, 0, 0, 0.35);
		box-shadow: 0 10px 6px -6px rgba(0, 0, 0, 0.35);
		/* border: 2px solid red; */
	}

	.photo-modal {
		display: flex;
		flex-direction: column;
		/* background-color: #ccc; */
		padding: 15px;
		position: fixed;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
		width: 700px;
		height: 800px;
		border-radius: 10px;
		/* display: none; */
	}

	.photo-modal-close-btn {
		position: absolute;
		display: flex;
		justify-content: center;
		align-items: center;
		width: 45px;
		height: 45px;
		background-color: #de6c83;
		border: none;
		border-radius: 10px;
		font-size: 36px;
		font-weight: bold;
		padding: 0px;
		margin: 0px;
		right: 10px;
		cursor: pointer;
	}

	.post-description {
		background-color: #ecb0e1;
		padding: 10px;
		max-width: 500px;
		border-radius: 10px;
		-webkit-box-shadow: 0 10px 6px -6px rgba(0, 0, 0, 0.35);
		-moz-box-shadow: 0 10px 6px -6px rgba(0, 0, 0, 0.35);
		box-shadow: 0 10px 6px -6px rgba(0, 0, 0, 0.35);
		margin-top: 5px;
	}

	.post-description p:nth-child(even) {
		margin: 5px 0px;
	}

	.modal-background {
		display: block;
		position: fixed;
		left: 0;
		right: 0;
		bottom: 0;
		top: 0;
		background-color: rgba(0, 0, 0, 0.75);
	}

	.year-header {
		position: relative;
		width: 200px;
		margin: 50px 0px 15px 15px;
		position: relative;
		font-size: 2.5em;
		z-index: 0;
	}

	.year-header::before {
		content: "";
		position: absolute;
		padding: 5px 10px;
		border-radius: 10px;
		background-color: #7fd1b9;
		height: 15px;
		width: 70px;
		top: 30px;
		left: 10px;
		z-index: -1;
	}

	#photo-modal-img {
		object-fit: scale-down;
	}

	@media screen and (max-device-width: 1100px) {
		main {
			/* padding: 10px; */
			display: flex;
			width: 100%;
			height: 100%;
			margin: 0px auto;
			flex-direction: column;
			align-items: center;
			/* border: 3px solid red; */
		}

		.posts {
			width: 100%;
			justify-content: right;
			align-items: flex-end;
			margin: 10px 5px 5px 0px;
			/* width: auto; */
			/* border: 1px solid red; */
		}

		.post-img {
			margin-top: 10px;
			object-fit: cover;
			object-position: center;
			height: 300px;
			width: 300px;
			border-radius: 10px;
			/* padding-right: 30px; */
		}

		.photo-modal {
			width: 300px;
			height: 500px;
			padding: 0px;
		}

		.photo-modal-close-btn {
			right: 0px;
			cursor: pointer;
			box-shadow: 0px 0px 3px 0px rgba(0, 0, 0, 0.75);
		}
	}
</style>
