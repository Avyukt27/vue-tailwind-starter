<template>
  <div class="min-h-screen bg-white text-black dark:bg-black dark:text-white flex flex-col items-center">
    <h1 class=" p-4">Welcome to My Page</h1>
    <button
      class="text-white bg-black"
      v-if="blackTurn"
      @click="changeTurn"
    >
      Time
    </button>
    <button
      class="text-center text-2xl text-black font-bold font-mono bg-white w-1/4 h-72 m-4 border-gray-500 border-solid border-2"
      v-if="whiteTurn"
      @click="changeTurn"
    >
      Time
    </button>
  </div>
</template>

<script lang="js">
  export default {
    data() {
      return {
        number: 0,
        whiteTurn: true,
        blackTurn: false,
      }
    },

    methods: {
      changeTurn() {
        if (this.whiteTurn) {
          this.whiteTurn = false;
          this.blackTurn = true;
        } else if (this.blackTurn) {
          this.whiteTurn = true;
          this.blackTurn = false;
        }
      }
    }
  }
</script>

<style lang="css" scoped>
  button {
    @apply text-center text-2xl font-bold font-mono w-1/4 h-72 m-4 border-gray-500 border-solid border-2
  }
</style>