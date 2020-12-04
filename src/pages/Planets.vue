<template>
  <q-page padding>
    <div v-for="(planets,index) in planetas" :key="index">
      <Card-Planetas :name="planets.name" :diameter="planets.diameter" :rotation_period="planets.rotation_period" :orbital_period="planets.orbital_period" :gravity="planets.gravity" :climate="planets.climate" :terrain="planets.terrain" :surface_water="planets.surface_water" :population="planets.population" />
    </div>
  </q-page>
</template>

<script>
import axios from 'axios'
import CardPlanetas from 'src/components/CardPlanetas'
export default {
  name: 'PagePlanetas',
  data () {
    return {
      planetas: []
    }
  },
  created: function () {
    axios.get('http://swapi.dev/api/planets/').then(res => {
      console.log('Pegou a lista de planetas')
      this.planetas = res.data.results
    })
  },
  components: {
    CardPlanetas
  }
}
</script>
