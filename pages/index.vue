<template>
  <div>
    <div class="container">
      <div>
        <logo />
        <h1 class="title">Solve Me</h1>
        <nuxt-child />
        <div class="links">
          <n-link to="/" class="button--green">To Universal Page</n-link>
          <n-link to="spa" class="button--grey">To SPA Page</n-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from '../components/Logo'

export default {
  components: {
    Logo
  },
  created () {
    if (typeof window === 'undefined') {
      this.$store.dispatch('count/addNumber')
    }

  },
  middleware ({ redirect, route }) {
    if (route.path === "/") {
      return redirect('/universal')
    }
  },
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>

