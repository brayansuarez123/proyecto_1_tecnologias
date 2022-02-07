<template>
  <div>
    <h1 v-if="visibilidad">{{ fecha }}</h1>
    <button @click="presionboton()">boton de acción</button>
  </div>
</template>

<script>
import { defineComponent, ref } from "vue";
import { date } from "quasar";

export default defineComponent({
  setup() {
    const visibilidad = ref(false);
    const fecha = ref("");
    const presionboton = function () {
      visibilidad.value = !visibilidad.value;
      fecha.value = date.formatDate(Date.now(), "DD/MM/YYYY");
    };

    return { visibilidad, presionboton, fecha };
  },
});
</script>
