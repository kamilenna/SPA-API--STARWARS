<template>
  <q-page padding>
    <div v-for="(people,index) in personagens" :key="index">
      <Card-Personagens :name="people.name" :height="people.height" :birth_year="people.birth_year" :hair_color="people.hair_color" :eye_color="people.eye_color" :skin_color="people.skin_color" :mass="people.mass" :gender="people.gender" />
    </div>
  </q-page>
</template>

<script>
import axios from 'axios'
import CardPersonagens from 'src/components/CardPersonagens'
export default {
  name: 'PagePersonagens',
  data () {
    return {
      personagens: []
    }
  },
  created: function () {
    axios.get('http://swapi.dev/api/people/').then(res => {
      console.log('Pegou a lista de personagens')
      this.personagens = res.data.results
    })
  },
  components: {
    CardPersonagens
  }
}
</script>
