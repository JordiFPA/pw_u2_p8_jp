<template>
  <div class="container">
    <label for="id_nombre">Nombre</label>
    <input v-model="nuevoNombre" id="id_nombre" type="text" />
    <label for="id_apellido">Apellido</label>
    <input v-model="nuevoApellido" id="id_apellido" type="text" />

    <button v-on:click="agregarEstudiante()">Agregar Boton</button>
    {{nuevoNombre}}
    {{nuevoApellido}}
    <ul>
      <li
        v-for="{nombre, apellido} in lista"
        :key="nombre"
      >Nombre:{{nombre}} - apellido: {{apellido}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nuevoNombre: "nuevo", 
      nuevoApellido:"nuevoApellido",
      lista: [
        { nombre: "Jordi", apellido: "Pila" },
        { nombre: "Melany", apellido: "Caizapasto" },
        { nombre: "Adriana", apellido: "Pila" },
        { nombre: "Byron", apellido: "Flores" },
        { nombre: "Michael", apellido: "Barrios" },
        { nombre: "Maria", apellido: "Montero" },
        { nombre: "Jordy", apellido: "Caiza" }
      ]
    };
  },
  methods: {
    agregarEstudiante() {
      const nuevo = {
        nombre: this.nuevoNombre,
        apellido: this.nuevoApellido,
      };
      //this.lista.unshift(nuevo);
      this.lista.push(nuevo);
    }
  }
};
</script>

<style>
</style>