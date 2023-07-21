<template> 
	<div id="canvas">
		<div id="deep-space">
			<h1> 
				Placar
			</h1>

			<h2>
				<NuxtLink to = "/"> Voltar </NuxtLink>
			</h2>
		</div>
	</div>
</template>

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
  height: calc(100% - 4rem);
  width: calc(100% - 4rem);

  background-image: url("~/assets/space.png");
  background-origin: content-box;

  position: relative;

  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
