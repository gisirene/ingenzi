<script >
  export default {
    data() {
      return {
        welcomeMessage: '',
        newGame: '',
        gameList: []
      };
    },
    methods: {
      addGame() {
        if (this.newGame.trim() !== '') {
          this.gameList.push(this.newGame);
          this.newGame = '';
        }
      }
    },
    mounted() {
      this.welcomeMessage = 'Welcome to the Game Wishlist App!';
    }
  };
</script>

<template>
  <div class="app">
    <h1>{{ welcomeMessage }}</h1>

    <input v-model="newGame" placeholder="Type a game title" />
    <button @click="addGame">Add Game</button>

    <h3>My Game Wishlist:</h3>
    <ul>
      <li v-for="(game, index) in gameList" :key="index">
        {{ game }}
      </li>
    </ul>
  </div>
</template>

<style scoped>
.app {
  max-width: 400px;
  margin: auto;
  text-align: center;
  padding: 20px;
  font-family: Arial;
}

input {
  padding: 8px;
  margin-right: 10px;
  width: 60%;
}

button {
  padding: 8px 12px;
}

ul {
  margin-top: 20px;
  text-align: left;
}

</style>
