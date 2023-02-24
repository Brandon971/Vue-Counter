<template>
 <div class="container bg-secondary">
  <div class="row">
    <div class="col">
      <div class="form">
        <div>
          <input type="text" placeholder="0" readonly :value="counter
          ">
        </div>
        <div class="row">
          <div class="col">
            <button class="btn btn-success" @click.prevent='increase'>increase</button>
          </div>
          <div class="col">
            <button class="btn btn-success" @click.prevent="decrease">decrease</button>
          </div>
        </div>
      </div>
    </div>
  </div>


 </div>
</template>

<script>


export default {
  computed: {
    counter() {
      return this.$store.state.counter
    }
  },
  methods:{
    increase() {
      this.$store.dispatch('increaseCounter');
    },
    decrease() {
      this.$store.dispatch('decreaseCounter')
    }
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
