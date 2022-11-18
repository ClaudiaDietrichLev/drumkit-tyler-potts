<template>
  <h1>Drumkit with VUE</h1>
  <div class="keys">
    <KeysLetter v-for="(sound, i) in sounds" :sound="sound" :key="i" />
  </div>
</template>

<script>
import KeysLetter from "@/components/Keys.vue";

export default {
  name: "App",
  data() {
    return {
      sounds: [
        {
          name: "boom",
          sound: require("./assets/sounds/boom.wav"),
          letter: "A",
        },
        {
          name: "clap",
          sound: require("./assets/sounds/clap.wav"),
          letter: "S",
        },
        {
          name: "hitat",
          sound: require("./assets/sounds/hihat.wav"),
          letter: "D",
        },
        {
          name: "kick",
          sound: require("./assets/sounds/kick.wav"),
          letter: "F",
        },
        {
          name: "openhat",
          sound: require("./assets/sounds/openhat.wav"),
          letter: "G",
        },
        {
          name: "ride",
          sound: require("./assets/sounds/ride.wav"),
          letter: "H",
        },
        {
          name: "snare",
          sound: require("./assets/sounds/snare.wav"),
          letter: "J",
        },
        {
          name: "tink",
          sound: require("./assets/sounds/tink.wav"),
          letter: "K",
        },
        {
          name: "tom",
          sound: require("./assets/sounds/tom.wav"),
          letter: "L",
        },
      ],
    };
  },
  components: { KeysLetter },
};
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

.keys {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
