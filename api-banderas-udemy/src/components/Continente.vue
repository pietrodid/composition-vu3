<template>
<div class="text-center">
  <h3>Filtrar por Continente</h3>
    <div class="btn-group mb-3" role="group" aria-label="Basic mixed styles example">
        <button type="button" class="btn btn-danger" @click="filtro('Americas')">AM</button>
        <button type="button" class="btn btn-success" @click="filtro('Europe')">EU</button>
        <button type="button" class="btn btn-success" @click="filtro('Oceania')">OC</button>
        <button type="button" class="btn btn-success" @click="filtro('Africa')">AF</button>
        <button type="button" class="btn btn-success" @click="filtro('')">ALL</button>
</div>        
</div>
</template>

<script>
import {useStore} from 'vuex'
export default {
    setup() {
      const store = useStore()
            
      const filtro = (region) => {
        store.dispatch('filtrarRegion', region)
      }
      return {filtro}
    }
}
</script>

