<template>
  <div class="color-game">
    <div id="play-game">
      <button @click="toggleColorDiv">Wanna be creative?</button>
    </div>
    <div class="color-div" v-show="showColorDiv">
      <h4>Pick a color</h4>
      <p>Change the background color of the entire website!</p>
      <div class="color-picker-wrapper">
        <span>🎨</span>
        <input type="color" id="color-picker" :value="currentColor" @input="changeBackgroundColor" />
      </div>
      <button @click="resetColor">Reset</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "ColorGame",
  data() {
    return {
      showColorDiv: false,
      currentColor: "#0084FF",
      initialBackgroundColor: null,
      initialButtonAndTableColor: null,
    };
  },
  mounted() {
    this.initialBackgroundColor =
      getComputedStyle(document.body).backgroundColor || "#ffffff";
  },
  methods: {
    toggleColorDiv() {
      this.showColorDiv = !this.showColorDiv;
    },
    changeBackgroundColor(event) {
      this.currentColor = event.target.value;
      document.body.style.backgroundColor = this.currentColor;
    },
    resetColor() {
      document.body.style.backgroundColor = this.initialBackgroundColor;
      this.currentColor = "#0084FF";
    },
  },
};
</script>
