<template>
  <div class="home">
    <div class="bg-text">
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

<style>
body, html{
  background: black;
  background-image: url("https://images.unsplash.com/photo-1519834089823-08a494ba5a12?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=968&q=80");
  background-repeat: no-repeat;
   /* Center and scale the image nicely */
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

* {
  box-sizing: border-box;
}

/* Position text in the middle of the page/image */
.bg-text {
  background-color: rgb(0,0,0); /* Fallback color */
  background-color: rgba(255, 255, 255, 1); /* Black w/opacity/see-through */
  color: white;
  border-radius: 10px;
  font-weight: bold;
  border: 3px solid #f1f1f1;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 2;
  width: 80%;
  padding: 20px;
  text-align: center;
}

h1 {
  background-color: black;
  color: white;
  padding-top: 10px;
  padding-bottom: 10px;
  border-radius: 10px;
}

@media only screen and (max-width: 600px) {
  body {
    background-repeat: no-repeat;
    background-color: black;
    background-size: cover;
    background-image: url("https://images.unsplash.com/photo-1540866225557-9e4c58100c67?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=640&q=80");
  }
}
</style>
