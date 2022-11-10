<template>
  <!--<header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
    </div>
  </header>

  <main>-->
    <div class="espace">
        <Renderer resize="window" orbit-ctrl ref="renderer" alpha="0">
          <Camera :position="{ z: 10 }" />
          <Scene>
            <PointLight :position="{ x: 50, y: 50, z: 50 }" />
            <AmbientLight />
            <Sphere ref="sphere" :position="{ x: 50, y: 47, z: 45 }" :radius="8" :rotation="{ y: Math.PI / 2 }">
              <BasicMaterial>
                <Texture path="/splash-bg.jpg"  refraction :refraction-ratio="0.95" />
              </BasicMaterial>
            </Sphere>
            <Box ref="box" :rotation="{ y: Math.PI / 4, z: Math.PI / 4 }" >
              <PhysicalMaterial color="#FF9E80" />
            </Box>

          </Scene>
        </Renderer>
    </div>
  <!--</main>-->
</template>

<script>
import { AmbientLight, BasicMaterial, Box, Camera, GltfModel, PhysicalMaterial, PointLight, Renderer, Scene, Sphere, Texture } from 'troisjs';
export default {
	name: 'App',
	components: {
    AmbientLight, BasicMaterial, Box, Camera, GltfModel, PhysicalMaterial, PointLight, Renderer, Scene , Sphere, Texture
  },
    mounted() {
    /*const renderer = this.$refs.renderer;
    const box = this.$refs.box.mesh;
    renderer.onBeforeRender(() => {
      box.rotation.x += 0.01;
    });*/
    function onReady(){
      return{
        onReady
      }
    }
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

.espace {
  /*background: url('/nightSky.jpg');
  background-repeat: no-repeat;
  background-size: cover;*/
}
</style>
