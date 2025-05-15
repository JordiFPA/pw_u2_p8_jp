<template>
  <div class="container">
    <h1>Contador</h1>
    <p>{{ this.numero }} <sup> 2</sup> = {{ calCuadrado }}</p>
 
    <div> 
        <button v-on:click = "incrementar()"> +1 </button>
        <button v-on:click = "decrementar()" > -1 </button>

    </div>

    <!-- 
    <p>{{ numero + 1 }}</p>
    <p>{{ texto }}</p>
    <p>{{ activo }}</p>
    <p>{{ usuario }}</p>
    <p>{{ arreglo }}</p>
    <p>{{ usuario.edad }}</p>
    1+1
    {{ 1 + 1 }}
    true?'Es Verdadero' :'Es Falso'
    {{ false ? "Es Verdadero" : "Es Falso" }} -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      numero: 5,
      texto: "Jordi Pila",
      activo: true,
      usuario: {
        nombre: "Jordi Pila",
        edad: "35",
        genero: "masculino",
      },
      arreglo: ["Amarillo", "Azul"],
    };
  },

  methods: {
    calcularCuadrado() {
      console.log("Entro al metodo");
      return this.numero * this.numero;
    },
    incrementar() { 
        return this.numero ++; 
    }, 
    decrementar(){ 
        return this.numero --;
    },
  },

  computed: {
    calCuadrado() {
      console.log("Entro a la propiedad computada");
      return this.numero * this.numero;
    },
  },
};
</script>

<style>
</style>