<template>
  <h1
    :style="{'color': color}"
  >contador: {{signoPeso}}</h1>
</template>

<script>
import { computed } from 'vue'
export default {
    props: ['contador', 'color'],
    setup(props) {
        const signoPeso = computed (() => {
            return '$' + props.contador
        })
        return {signoPeso}
    }
  
  // computed: {
     //   signoPeso() {
       //     return '$' + this.contador
        //}
   // }
}
</script>

<style>

</style>