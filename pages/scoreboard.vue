<template> 
	<div id="canvas">
		<div id="deep-space">
			<h1 
				class="custom-title"
			> 
				Placar
			</h1>

			<li v-for="(player, index) in topThree" 
				:key="index" 
				class = "player-display-design"
			>
				<span class="player-rank">{{ index + 1 + "." }}</span>
				<span class="player-score">{{ player.score }}</span>
			</li>

			<div class="button-stack">
				<NuxtLink 
					to = "/"
					class = "custom-nuxtlink"
				> 
					Voltar
				</NuxtLink>
			</div>
		</div>
	</div>
</template>

<script>
	export default {
		data() {
			return {
				players: [{
				  "startTime" : "2023-07-21T17:39:23.216088601",
				  "destroyedAsteroids" : 92,
				  "score" : 94650.0
				}, {
				  "startTime" : "2023-07-22T16:06:00.290696042",
				  "destroyedAsteroids" : 12,
				  "score" : 16200.0
				}, {
				  "startTime" : "2023-07-22T16:06:00.290696042",
				  "destroyedAsteroids" : 15,
				  "score" : 18300.0
				}, {
				  "startTime" : "2023-07-22T16:06:00.290696042",
				  "destroyedAsteroids" : 15,
				  "score" : 18300.0
				}]
			}
		},

		computed: {
			topThree: function() {
				return this.players.slice().sort((a,b) => b.score - a.score).slice(0,3);
			}
		}
	};
</script>

<style>
li.player-display-design {
	color: white;
	font-size: 150px;
	margin-bottom: 5px;
	list-style-type: none;
}

.player-rank {
  flex: 0 0 30px;
}

.player-destroyedAsteroids {
  flex: 1;
}

.player-score {
  flex: 0 0 60px;
}
</style>
