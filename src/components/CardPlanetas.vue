<template>
<div>
<q-card id="card" dark bordered class="bg-grey-9 my-card q-pa-lg q-mb-md row wrap justify-around">
  <q-card-section>
    <div class="text-h4">{{name}}</div>
  </q-card-section>

  <q-separator dark inset />

  <q-card-section>
    <p><strong>Diâmetro:</strong> {{diameter}}</p>
    <p><strong>Período de Rotação:</strong> {{rotation_period}}</p>
    <p><strong>Período Orbital:</strong> {{orbital_period}}</p>
    <p><strong>Gravidade:</strong> {{gravity}}</p>
    <p><strong>Clima:</strong> {{climate}}</p>
    <p><strong>Terreno:</strong> {{terrain}}</p>
    <p><strong>Água da surperfície:</strong> {{surface_water}}</p>
    <p><strong>Gênero:</strong> {{population}}</p>
  </q-card-section>
</q-card>
</div>
</template>

<script>
export default {
  props: {
    name: String,
    diameter: String,
    rotation_period: String,
    orbital_period: String,
    gravity: String,
    climate: String,
    terrain: String,
    surface_water: String,
    population: String
  }
}
</script>

<style lang="stylus">
#card
 font-family Roboto
 width: 350px
 height: 470px
 margin-top: 90px
 margin-left: 70px
 float: left

 p {
    color: $warning;
    font-family: Roboto;
    font-size: 16px;
}
</style>
