
<template>
  <q-page padding>
    <div v-for="(movie,index) in filmes" :key="index">
      <Filmes :title="movie.title" :url="movie.url" :episode_id="movie.episode_id" :opening_crawl="movie.opening_crawl" :director="movie.director" :producer="movie.producer" :release_date="movie.release_date"/>
    </div>
  </q-page>
</template>

<script>
import axios from 'axios'
import Filmes from 'src/components/CardFilmes'
export default {
  name: 'PageMovies',
  data () {
    return {
      filmes: []
    }
  },
  created: function () {
    axios.get('https://swapi.dev/api/films/').then(res => {
      console.log('Pegou a lista de filmes')
      this.filmes = res.data.results
      console.log(this.filmes)
    })
  },
  components: {
    Filmes
  }
}
</script>
