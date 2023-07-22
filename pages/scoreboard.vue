<template> 
	<div id="canvas">
		<table id="deep-space">
			<h1 
				class="custom-title"
			>
				PLACAR
			</h1>
			<tbody>
				<tr v-for="(player, index) in topThree" 
					:key="index" 
					class = "player-display-design"
				>
					<td class="custom-leaderboard">{{ index + 1 + "." }}</td>
					<td class="custom-leaderboard">{{ player.score }}</td>
				</tr>

			</tbody>

			<NuxtLink 
				to = "/"
				class = "custom-nuxtlink"
			> 
				VOLTAR
			</NuxtLink>
		</table>
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
				  "score" : 180300.0
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
.custom-leaderboard {
	font-size: 80px;
	font-family: 'FontArcade', sans-serif;

	color: #FFA500;
}
</style>
