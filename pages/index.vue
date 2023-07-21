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
