<main>
	<div id="canvas">
		<div id="coffee-root">
			<div id="coffee-shadow"></div>
			<div id="handle"></div>
			<div id="coffee-cup-bottom"></div>
			<div id="coffee-cup-top"></div>
			<div id="coffee-empty"></div>
			<div id="coffee-liquid"></div>
		</div>
		<div id="donut-container">
			<div id="donut-shadow"></div>
			<div id="donut-base">
				<div id="donut-hole">
					<div id="frosting">
						<div id="drip"></div>
						<div class="decoration" id="sprinkle-1"></div>
						<div class="decoration" id="sprinkle-2"></div>
						<div class="decoration" id="sprinkle-3"></div>
						<div class="decoration" id="sprinkle-4"></div>
					</div>
				</div>
			</div>
		</div>

	</div>
	<div id="canvas">

	</div>
</main>

<style>
	:root {
		--coffee-color: rgb(185, 101, 22);
		--cup-height: 12vh;
		--cup-top-offset: -13vh; /* Note: Due to this being vanilla CSS, this needs to be calculated by hand. It is -(cup-height)-1. */
		--frosting-color: rgb(255, 110, 243);
	}

	#coffee-root {
		margin-top: auto;
		margin-right: 40%;
	}

	#canvas {
		display: flex;
		flex-direction: column;
		margin: 0;
		background-color: antiquewhite;
		width: 25vw;
		height: 25vh;
		align-items: center;
		justify-content: center;
	}

	#coffee-liquid {
		background-color: var(--coffee-color);
		border-radius: 50%;
		width: 7vw;
		height: 1vh;
		margin-left: 1.5vw;
	}

	#coffee-empty {
		background-image: linear-gradient(aliceblue, rgb(214, 214, 214));
		border-radius: 50%;
		width: 7vw;
		height: 1vh;
		margin-bottom: -1vh;
		margin-left: 1.5vw;
	}

	#coffee-cup-top {
		background-image: linear-gradient(rgb(255,255,255), aliceblue);
		border-radius: 50%;
		width: 8vw;
		height: 2vh;
		margin-bottom: -1.5vh;
		margin-left: 1vw;
	}

	#coffee-cup-bottom {
		background-image: radial-gradient(at top, aliceblue, rgb(233, 233, 233));
		border-bottom-left-radius: 40%;
		border-bottom-right-radius: 40%;
		width: 8vw;
		height: var(--cup-height);
		margin-bottom: var(--cup-top-offset);
		margin-top: -8vh; /* Affects the handle positioning too, be careful */
		margin-left: 1vw;
	}

	#coffee-shadow {
		background-image: radial-gradient(rgba(0,0,0,0.1), rgba(0,0,0,0));
		border-radius: 70%;
		width: 7vw;
		height: 0.7vw;
		margin-bottom: -11.2vh;
	}

	#handle {
		border-color: rgb(221, 221, 221);
		border-width: 0.7vw;
		border-style: solid;
		border-radius: 100%;
		width: 1vw;
		height: 4vh;
		margin-left: 8vw;
	}

	#donut-shadow {
		position: relative;
		background-image: radial-gradient(rgba(0,0,0,0.1), rgba(0,0,0,0));
		background-color: rgba(0,0,0, 0.1);
		border-radius: 100%;
		filter: blur(2px);
		width: 8.5vw;
		height: 4vh;
		margin-top: 3vh;
		transform: rotate(-5deg);
	}

	#donut-base {
		position: absolute;
		background-image: radial-gradient(at top, rgb(223, 156, 31), rgb(190, 133, 27));
		background-color: rgb(185, 129, 24);
		border-radius: 100%;
		width: 8.5vw;
		height: 8vh;
		margin-top: -9vh;
		margin-left: 2vw;
	}

	#donut-hole {
		position: relative;
		background-image: linear-gradient(rgb(185, 129, 24), rgb(122, 87, 22));
		background-color: rgb(92, 46, 2);
		border-radius: 100%;
		width: 6vw;
		height: 3.5vh;
		margin-top: 1vh;
		margin-left: 1.3vw;
	}

	#frosting {
		position: absolute;
		border-width: 0.9vw;
		border-style: solid;
		border-color: var(--frosting-color);
		border-radius: 100%;
		width: 5.9vw;
		height: 2.5vh;
		margin-top: -1.3vh;
		margin-left: -0.9vw;
	}

	#drip {
		transform: rotate(230deg);
		margin-top: 2.3vh;
		background-color: var(--frosting-color);
		width: 0.7vw;
		height: 1vw;
		border-radius: 100%;
	}

	#sprinkle-1 {
		background-color: greenyellow;
		margin-top: -4.2vh;
		transform: rotate(10deg);
	}

	#sprinkle-2 {
		background-color: aqua;
		margin-top: 3vh;
		transform: rotate(100deg);
	}

	#sprinkle-3 {
		background-color: red;
		margin-top: -0.7vh;
		margin-left: 4vw;
		transform: rotate(-30deg);
	}

	#sprinkle-4 {
		background-color: greenyellow;
		margin-top: -3.5vh;
		margin-left: 4vw;
	}

	.decoration {
		width: 0.4vw;
		height: 0.2vh;
	}
</style>