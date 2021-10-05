<template>
<div class="footer">
    <footer>
        <spam>{{ dato1 }}</spam> <br/>
        <spam>Grupo: {{ grupo }}</spam> <br/>
        <spam>Materia: {{ materia }}</spam> <br/>
        <spam>Carrera: {{ carrera }}</spam> 
    </footer>
</div>
</template>

<script>
export default {
  name: "misDatos",
  props: {
    dato1: String,
  },
  data() {
    return {
      grupo: '4° A',
      materia: 'Aplicaciones Web Orientadas a Servicios.',
      carrera: 'Tecnologias de la Informacion Desarrollo de Software Multiplataforma.'
    };
  },
};
</script>

<style scoped>
.footer{
    margin: 20px 0px 20px 0;
    background-color: greenyellow;
    color: rgb(16, 34, 138);
}
</style>