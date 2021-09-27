<template>
  <div id="app">
    <h1>Crear una nueva tarea</h1>
    Tarea <input id="datos" v-model="tarea">
    <button v-on:click="agregar">Crear</button>
    <br>
    <h3>Lista</h3>
    <ul v-for="(task, index) in tareas" :key="index">
        <li>{{index}}.- {{task}}</li>
    </ul>
    
  </div>
</template>
<script>
export default {
  name: "App",
  data() {
    return { tarea: "", tareas: [] }
  },
  methods: {
      agregar: function(){
          this.tareas.push(this.tarea);
      }
  }
};
</script>