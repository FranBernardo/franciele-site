<template>
  <div class="app" :class="mode">
    <Headeer :mode="mode" />
    <toggle :mode="mode" @toggle="toggle" />
  </div>
</template>

<script>
import Toggle from "./components/Toggle.vue";
import Headeer from "./components/Headeer.vue";
export default {
  name: "App",
  data() {
    return {
      mode: "light",
    };
  },
  components: {
    Toggle,
    Headeer,
  },
  methods: {
    toggle() {
      if (this.mode === "dark") {
        this.mode = "light";
      } else {
        this.mode = "dark";
      }
    },
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Rounded Mplus 1c";
}
.app {
  width: 100vw;
  min-height: 100vh;
  background: #f1e9db;
  color: #a39b8b;
  transition: background 0.3s ease-in-out;
}
.dark {
  background: #07020d;
  color: #ffffff;
}
</style>
