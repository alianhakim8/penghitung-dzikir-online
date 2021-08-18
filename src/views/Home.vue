<template>
  <div class="home">
    <div class="container">
      <h1>Aplikasi Penghitung Dzikir Online</h1>
      <div class="row mt-5">
        <div class="col-md-4 col-4">
          <button class="btn btn-dark" @click="decrease()">-</button>
        </div>
        <div class="col-md-4 col-4">
          <span class="btn btn-outline-dark">{{ counter }}</span>
        </div>
        <div class="col-md-4 col-4">
          <button class="btn btn-dark" @click="increase()">+</button>
        </div>
      </div>
      <button class="btn btn-danger mt-4" @click="reset()">
        Ulangi dari 0
      </button>
      <!-- <p class="mt-4">alianhakim. 2021</p> -->
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      counter: 0,
    };
  },
  components: {},
  methods: {
    increase() {
      this.counter++;
    },
    decrease() {
      if (this.counter != 0) {
        this.counter--;
      }
    },
    reset() {
      let yakin = confirm("Anda yakin ?");
      if (yakin) {
        this.counter = 0;
      }
    },
  },
};
</script>

<style scoped>
</style>
