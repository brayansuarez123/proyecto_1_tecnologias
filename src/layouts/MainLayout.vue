<template>
  <div>
  <h1 v-if="visibilidad"> </h1>
  <button>boton de acción</button>
  </div>
</template>

<script>
import { defineComponent,ref } from 'vue'

export default defineComponent({
  setup() {
    const visibilidad = ref(false);
    const date = ref("")
    const presionboton = function () {
      visibilidad.value = !visibilidad.value
      const date = new Date();
      
    }

  return{visibilidad, presionboton}
  },
})
</script>
