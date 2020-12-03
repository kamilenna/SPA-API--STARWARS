<template>
<div>
<q-card dark bordered class="bg-grey-9 my-card q-pa-lg q-mb-md row wrap justify-around">
  <q-card-section>
    <div class="text-h3">{{title}}</div>
  </q-card-section>

  <q-separator dark inset />

  <q-card-section>
    <p>Episódio: {{episode_id}}</p>
    <p>Abertura: {{opening_crawl}}</p>
    <p>Diretor: {{director}}</p>
    <p>Produtores: {{producer}}</p>
    <p>Data de lançamento: {{release_date}}</p>
  </q-card-section>
</q-card>
</div>
</template>

<script>
export default {
  data () {
    return {
      filme: {
        people: '',
        planet: ''
      }
    }
  },
  props: {
    title: String,
    episode_id: Number,
    opening_crawl: String,
    director: String,
    producer: String,
    release_date: String,
    url: String
  }
}
</script>

<style lang="stylus">
p {
    color: $warning;
    font-family: Roboto;
    font-size: 18px;
}
.my-card {
  width: 100%;
}
</style>
