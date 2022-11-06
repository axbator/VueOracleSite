<template>
  <!--<header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
    </div>
  </header>

  <main>-->
        <Renderer ref="renderer">
          <Camera :position="{ z: 10 }" />
          <Scene>
            <PointLight :position="{ y: 50, z: 50 }" />
            <Box ref="box" :rotation="{ y: Math.PI / 3, z: Math.PI / 4 }">
              <LambertMaterial />
            </Box>
          </Scene>
        </Renderer>
  <!--</main>-->
</template>

<script>
import { Box, Camera, LambertMaterial, PointLight, Renderer, Scene } from 'troisjs';
export default {
	name: 'App',
	components: {
    Box, Camera, LambertMaterial, PointLight, Renderer, Scene 
  },
    mounted() {
    const renderer = this.$refs.renderer;
    const box = this.$refs.box.mesh;
    renderer.onBeforeRender(() => {
      box.rotation.x += 0.01;
    });
  },
}
</script>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
