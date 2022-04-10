<script lang="ts">
	let state = false;
	import { fade } from 'svelte/transition';
</script>

<main>
	<section class="intro">
		{#if state}
			<svg
				on:click={() => (state = !state)}
				in:fade
				xmlns="http://www.w3.org/2000/svg"
				class="h-6 w-6"
				fill="none"
				viewBox="0 0 24 24"
				stroke="currentColor"
				stroke-width="2"
			>
				<path
					stroke-linecap="round"
					stroke-linejoin="round"
					d="M12 3v1m0 16v1m9-9h-1M4 12H3m15.364 6.364l-.707-.707M6.343 6.343l-.707-.707m12.728 0l-.707.707M6.343 17.657l-.707.707M16 12a4 4 0 11-8 0 4 4 0 018 0z"
				/>
			</svg>
		{:else}
			<svg
				on:click={() => (state = !state)}
				in:fade
				xmlns="http://www.w3.org/2000/svg"
				class="h-6 w-6"
				fill="none"
				viewBox="0 0 24 24"
				stroke="currentColor"
				stroke-width="2"
			>
				<path
					stroke-linecap="round"
					stroke-linejoin="round"
					d="M20.354 15.354A9 9 0 018.646 3.646 9.003 9.003 0 0012 21a9.003 9.003 0 008.354-5.646z"
				/>
			</svg>
		{/if}

		<h1>Ca-Jaye's discord bot playground</h1>
		<p>This website is to display the discord bots I make for fun!</p>
	</section>
	<section class="bots">
		<div>
			<div>
				<h2>
					<a
						href="https://discord.com/api/oauth2/authorize?client_id=948338036276609054&permissions=277025704960&scope=applications.commands%20bot"
						target="_blank"
					>
						ANIMISTA
					</a>
				</h2>
			</div>
			<div>
				<h2>COMING SOON</h2>
			</div>
			<div>
				<h2>COMING SOON</h2>
			</div>
		</div>
	</section>
</main>

<style lang="scss">
	svg {
		cursor: pointer;
		color: #fff;
		width: 30px;
		height: 30px;
		margin-bottom: 0.8rem;
	}
	main {
		margin: 0 2.5rem;
		@include break(tablet) {
			margin-top: 0;
		}
		margin-top: 2rem;
		display: grid;
		place-content: center;
		@include break(tablet) {
			height: 100vh;
			@include grid-column-layouts(2);
		}

		.intro {
			display: flex;
			justify-content: center;
			flex-direction: column;

			h1 {
				user-select: none;
				display: inline;
				line-height: 1.2;
				color: var(--text-white);
				@include break(tablet) {
					@include font-props(h1);
				}
				@include font-props(h2);
			}

			p {
				color: var(--text-grey);
				margin-top: 1rem;
				@include font-props(p);
			}
		}
		.bots {
			@include break(tablet) {
				margin-top: 0;
			}
			margin-top: 2rem;
			@extend %reg-flex;
			div {
				@extend %reg-flex;
				@include break(tablet) {
					flex-wrap: wrap;
					flex-direction: row;
				}
				flex-direction: column;
				gap: 1.8rem;
				div {
					display: inline-flex;
					width: 15rem;
					padding: 0.8rem 0;
					border: 1px solid var(--border-color);
					border-radius: $border-radius;
					background-color: var(--secondary-bg-color);
					transition: all 0.23s ease-in-out;
					&:hover {
						width: calc(15rem + 1rem);
						padding: calc(1rem + 2px) 0;
						cursor: pointer;
					}

					h2 {
						color: var(--text-white);

						a {
							color: var(--text-white);
							text-decoration: none;
							&:visited {
								color: var(--text-white);
							}
						}
					}
				}
			}
		}
	}
</style>
