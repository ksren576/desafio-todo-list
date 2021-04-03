<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <label>Tarea:</label>
    <input type="text" v-model="inputMensaje" placeholder="Ingresar nueva tarea" />
    <button @click="agregarTarea">Crear</button>
    <br>
    <h1>Lista</h1>
    <ul>
      <li v-for="(mensaje, index) in lista" :key="index + 'lista-todo'">{{ mensaje }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'ListaTodo',
  data() {
    return {
      lista: [],
      inputMensaje: ''
    }
  },
  methods: {
    agregarTarea() {
      if (this.inputMensaje) {
        this.lista.push(this.inputMensaje);
        this.inputMensaje = '';
      }
    }
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  margin: 10px 10px;
}
a {
  color: #42b983;
}
input {
  margin: 0 10px;
}
</style>
