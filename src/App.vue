<template>
  <div id="app">
    <header>
      <nav class="navbar">
        <div class="logo"></div>
        <ul>
          <li><router-link to="/">Home</router-link></li>
          <li><router-link to="/about">About</router-link></li>
          <li><router-link to="/portfolio">Portfolio</router-link></li>
        </ul>
      </nav>
    </header>
    <transition name="fade" mode="out-in">
      <router-view></router-view>
    </transition>
      
  </div>
</template>

<script>


export default {
  name: 'App',
  components: {

  }
}
</script>

<style lang="scss">
@import url('assets/scss/index.scss');
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  overflow: hidden;
  
  header {
    padding: 10px;
    .navbar {
      max-width: 80%;
      margin: auto;
      display: flex;
      justify-content: space-between;
      align-items: center;
      .logo {
        width: 50px;
        height: 50px;
        background: rgb(59, 73, 223);
        border-radius: 50%;
      }
      ul {
        display: flex;

        li {
          margin: 5px 15px;
          white-space: nowrap;

          a{
            text-decoration: none;
          }
        }
      }
    }
  }

  div {
    text-align: center;
    height: 90vh;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .fade-enter , .fade-leave-to {
    opacity: 0;
    transform: translateX(2em);
  }

  .fade-enter-active , .fade-leave-active {
    transition: all .3s ease-in-out;
  }
}
</style>
