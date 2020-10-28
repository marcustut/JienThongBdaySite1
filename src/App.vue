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
      if (this.num1 == "9" && this.num2 == "8" && this.num3 == "2" && this.num4 == "5") {
        this.message = "Go down and take your Gift larhhh, haiyaaa"
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
  background-color: #ffb0b0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: black;
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
