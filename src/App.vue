<template>
  <div class="app">hello, hydrule
    <p>{{jobs}}</p>
  </div>
</template>

<script lang="ts">
// import { defineComponent, reactive, toRefs } from 'vue'
import { defineComponent, ref } from 'vue';
import Job from "@/types/Job"

export default defineComponent({
  name: "App",
  setup(){
    // const state = reactive({
    //   name: "link" as string,
    //   age: 25 as number | string
    // })
    // return {...toRefs(state)}

    const jobs=ref<Job[]>( [
      {title: "frontend developer", location: "Voronez", salary: 150000, takesRelocation: false, id: 1},
      {title: "Pediatrician", location: "St-Petersburg", salary: 80000, takesRelocation: true, id: 2},
      {title: "Teacher", location: "Moscow", salary: 60000, takesRelocation: true, id: 3},
      {title: "Flute player", location: "St-Petersburg", salary: 75000, takesRelocation: true, id: 4},
      {title: "Farm worker", location: "Rostov", salary: 50000, takesRelocation: true, id:5},
    ])
    return {jobs}
  }
})
</script>


<style lang="scss">
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
