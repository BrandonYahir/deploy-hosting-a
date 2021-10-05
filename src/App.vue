<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <!--Para llamar a nuestro componente vamos a utilizar nuestra pseudo etiqueta.-->
  <Titulo texto="Mi Banco dinámico 2.0"/>
  <Cuenta />
  <misDatos dato1="Brandon Yahir Flores Vazquez"/>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import Titulo from './components/Titulo.vue'
import Cuenta from './components/Cuenta.vue'
import misDatos from './components/misDatos.vue'

export default {
  name: 'App',
  components: {
    Titulo, Cuenta, misDatos
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>