<template>
  <h2>Tipo de cuenta: {{ cuenta }}</h2>
  <h2>Saldo: {{ saldo }}</h2>
  <h3>Cuenta: {{ estado ? "Activada 🟢" : "Desactivada 🔴" }}</h3>
  <div v-for="(servicios, index) in servicios" :key="index">
    {{ index + 1 }} - {{ servicios }}
  </div>

  <AccionSaldo 
    texto="Aumentar saldo"
    @accion = "aumentar"
    />
  <AccionSaldo 
    texto="Disminuir saldo"
    @accion = "disminuir" :desactivar="desactivar"
    />
</template>

<script>
import AccionSaldo from "./AccionSaldo.vue";

export default {
  name: "Cuenta",

  components: {
    AccionSaldo, alert
  },

  data() {
    return {
      saldo: 1000,
      cuenta: "Visa Elecktron",
      estado: true,
      servicios: ["Giro", "Abono", "Transferencia", "Retiro"],

      desactivar:false
    }
  },

  methods: {
    aumentar() {
      this.saldo += 100
      this.desactivar = false
    },
    disminuir() {
      if (this.saldo === 0){
          this.desactivar = true
          alert('Saldo agotado.');
      } else {
          this.saldo -= 100;
      }
    },
  },

};
</script>

<style scoped>
</style>

