<template>
  <!-- HolaMundoView> </HolaMundoView> -->
  <!-- ContadorView /> -->
  <!-- EstudianteTablaView /> -->
  <!-- VehiculoView /> -->
  <!-- PreguntaView /> -->
  <PerritoView />
</template>

<script>
import HolaMundoView from "./views/HolaMundoView.vue";
import ContadorView from "@/views/ContadorView.vue";
import EstudianteView from "@/views/EstudianteView.vue";
import EstudianteTablaView from "@/views/EstudianteTablaView.vue";
import VehiculoView from "@/views/VehiculoView.vue";
import PreguntaView from "@/views/PreguntaView.vue";
import PerritoView from "@/views/PerritoView.vue";

export default {
  name: "App",
  components: {
    HolaMundoView,
    ContadorView,
    EstudianteView,
    EstudianteTablaView,
    VehiculoView,
    PreguntaView,
    PerritoView,
  }
};
</script>

<style scopped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #cbe1f6;
  margin-top: 60px;
}
</style>
