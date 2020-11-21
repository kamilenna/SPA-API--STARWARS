<template>
  <q-page class="flex flex-center ">
    <div class="absolute-full text-subtitle2 flex flex-center">
            <img
    style="max-width: 400px; height: 200px;"
      alt="Logo do Star Wars"
      src="https://pixy.org/download/583003/"
    >
    <p class="absolute-bottom text-subtitle2 flex flex-center text-weight-bolder q-mb-xl">Conheça mais sobre uma das maiores franquias de filmes de fantasia científica!</p>
    </div>
    <img class="bgSky" src="https://cdn.pixabay.com/photo/2016/01/27/15/25/space-1164579_1280.png" alt="Céu estrelado">
  </q-page>
</template>

<script>
export default {
  name: 'PageIndex'
}
</script>

<style lang="stylus">
p {
  color $warning;
}
.bgSky {
  width: 100%;
}
</style>
