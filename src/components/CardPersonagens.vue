<template>
<div>
<q-card id="card" dark bordered class="bg-grey-9 my-card q-pa-lg q-mb-md row wrap justify-around">
  <q-card-section>
    <div class="text-h4">{{name}}</div>
  </q-card-section>

  <q-separator dark inset />

  <q-card-section>
    <p><strong>Altura:</strong> {{height}}</p>
    <p><strong>Ano de Nascimento:</strong> {{birth_year}}</p>
    <p><strong>Cor do cabelo:</strong> {{hair_color}}</p>
    <p><strong>Cor dos olhos:</strong> {{eye_color}}</p>
    <p><strong>Cor da pele:</strong> {{skin_color}}</p>
    <p><strong>Massa:</strong> {{mass}}</p>
    <p><strong>Gênero:</strong> {{gender}}</p>
  </q-card-section>
</q-card>
</div>
</template>

<script>
export default {
  props: {
    name: String,
    height: String,
    birth_year: String,
    hair_color: String,
    eye_color: String,
    skin_color: String,
    mass: String,
    gender: String
  }
}
</script>

<style lang="stylus">
#card
 font-family Roboto
 width: 350px
 height: 450px
 margin-top: 90px
 margin-left: 70px
 float: left

 p {
    color: $warning;
    font-family: Roboto;
    font-size: 16px;
}
</style>
