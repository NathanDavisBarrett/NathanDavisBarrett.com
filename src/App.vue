<template>
    <div id="app">
        <Header id="baseHeader" />
        <router-view v-slot="{ Component }">
            <transition name="fade" mode="out-in">
                <component :is="Component" />
            </transition>
        </router-view>
    </div>
</template>

<script>
import Header from '@/components/Header.vue'

export default {
    name: "Home",
    components: {
        Header,
    },
    created() {
        this.$globalData = {};
        this.$globalData["headerSelection"] = "about";
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

.wrapper {
    width: 100%;
    min-height: 100%;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease;
}


.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

</style>
