<template> 
	<div id="canvas">
		<div id="deep-space">
			<h1 
				class="custom-title"
			> 
				Galaxy Raiders
			</h1>

			<div class="button-stack">
				<NuxtLink 
					to = "/game"
					class = "custom-nuxtlink"
				> 
					Jogar 
				</NuxtLink>

				<NuxtLink 
					to = "/scoreboard"
					class = "custom-nuxtlink"
				> 
					Placar 
				</NuxtLink>

				<button 
					@click = "exitGame"
					class = "custom-button"
				> 
					Sair 
				</button>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	methods: {
		// simulating exiting the game by redirection
		exitGame() {
			window.location.href = "https://www.google.com"
		}
	}
}
</script>

<style>
#canvas {
  height: calc(100vh - 4rem);
  width: calc(100vw - 4rem);

  padding: 2rem;

  background-color: #36bbf5;
  overflow: hidden;

  position: relative;

  display: flex;
  justify-content: center;
  align-items: center;
}

#deep-space {
  height: calc(100vh - 4rem);
  width: calc(100vw - 4rem);

  padding: 0rem;

  background-image: url("~/assets/space.png");
  background-origin: content-box;

  position: relative;

  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}

.button-stack {
	display: flex;
	flex-direction: column;
	align-items: center;
}

.custom-button,
.custom-nuxtlink {
	margin: 10px;
	padding: 15px 30px;
	font-size: 20px;
	background-color: #36bbf5;
	color: #FFFFFF;
	border: none;
	border-radius: 5px;
	cursor: pointer;
	text-decoration: none;
}

.custom-title {
	font-size: 40px;
	margin: 50px;
	color: #FFFFFF;
}
</style>
