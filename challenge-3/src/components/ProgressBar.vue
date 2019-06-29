<template>
  <b-container>
    <h3 class="text-center mt-3">Barra de progreso 🚥</h3>
    <h3 class="text-center mt-2">{{ contador }}%</h3>
    <div class="text-center mt-3">
      <button class="btn btn-danger mb-3" @click="lessContador">-</button>
      <button class="btn btn-primary mr-1 mb-3" @click="plusContador">+</button>
    </div>
  </b-container>
</template>

<script>
export default {
  name: "ProgressBar",
  data() {
    return {
      contador: 0
    };
  },
  methods: {
    lessContador() {
      if (this.contador > 0) {
        return this.contador--;
      }
      return this.contador;
    },
    plusContador() {
      if (this.contador < 100) {
        return this.contador++;
      }
      return this.contador;
    }
  }
};
</script>

<style scoped>
</style>