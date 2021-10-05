<template>
  <h1>{{ texto }}</h1>
</template>

<script>
export default {
  name: 'Titulo',
  props: {
    texto: String,
  },
};
</script>

/** Cuando solo está style el padre "APP" heredará los estilos a sus hijos,
cuando tiene "scope" solo aplicará a este hijo, es decir; lo tomará separado. */
<style scoped>
h1{
    color: peru;
}
</style>>