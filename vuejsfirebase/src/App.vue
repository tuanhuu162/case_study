<template>
  <div id="app">
    <img src="./assets/logo.png">
    <router-view/>
  </div>
</template>

<script>
let config = {
  apiKey: "AIzaSyBfebo3lPIg8g82w7Zl_YNYYXDGw3unqpw",
  authDomain: "teko-449de.firebaseapp.com",
  databaseURL: "https://teko-449de.firebaseio.com",
  projectId: "teko-449de",
  storageBucket: "teko-449de.appspot.com",
  messagingSenderId: "257324425236"
}
let app = FireBase.initializeApp(config);
let db = app.database();

let bookRef = db.ref('books');

export default {
  name: 'app',
  firbase:{
    books: booksRef
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
