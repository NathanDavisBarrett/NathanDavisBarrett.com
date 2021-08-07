<template>
    <div id="app">
        <Header id="baseHeader" />
        <router-view></router-view>
    </div>
</template>

<script>
import Header from '@/components/Header.vue'

export default {
    name: "Home",
    components: {
        Header,
    }
}
</script>


<style>
#app {
    padding: 15px;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
