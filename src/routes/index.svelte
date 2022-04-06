<main>
	<section class="intro">
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
				flex-direction: column;
				div {
					width: 14rem;
					height: 3.3rem;
					margin: 1rem 0;
					border-radius: $border-radius;
					background-color: var(--secondary-bg-color);
					transition: all 0.5s ease-in-out;
					&:hover {
						width: calc(14rem + 1rem);
						height: calc(3.5rem + 2px);
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
