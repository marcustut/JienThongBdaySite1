<template>
  <div class="container">
    <HelloWorld msg="Welcome to your Gift Redeem Counter"/>
    <div class="pin-box">
      <input v-model="num1" class="box" type="text" maxlength="1"/>
      <input v-model="num2" class="box" type="text" maxlength="1"/>
      <input v-model="num3" class="box" type="text" maxlength="1"/>
      <input v-model="num4" class="box" type="text" maxlength="1"/>
    </div>
    <p>{{ message }}</p>
    <button @click="checkPIN">Submit</button>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data() {
    return {
      num1: "",
      num2: "",
      num3: "",
      num4: "",
      message: "",
    }
  },
  methods: {
    checkPIN() {
      if (this.num1 == "7" && this.num2 == "2" && this.num3 == "4" && this.num4 == "5") {
        this.message = "Congratulations! You can go to the next one!"
      }
      else {
        this.message = "INCORRECT! Try again."
      }
    }
  }
}
</script>

<style>
body {
  background-color: darkslategrey;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: white;
  margin-top: 60px;
}

.pin-box {
  display: flex;
  flex-direction: row;
  justify-content: center;
  margin: auto;
  width: 25%;
  padding: 10px;
}

.box {
  height: 75px;
  width: 50px;
  font-size: 50px;
  text-align: center;
}
</style>
