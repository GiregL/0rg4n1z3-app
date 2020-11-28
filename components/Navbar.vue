<template>

  <transition appear
              enter-class="from-appear"
              enter-to-class="appeared"
              enter-active-class="transition"

              leave-class="goingToLeave"
              leave-to-class="leaved"
              leave-active-class="transition"
  >
  <nav class="w-full flex flex-row items-center px-6 py-4 bg-white shadow-xl">
    <h1 class="text-gray-900 font-bold text-2xl flex-grow">0rg4n1z3</h1>
    <ul class="flex flex-row items-center">
      <li><a href="#" class="px-6 py-4 text-gray-600 rounded-lg border border-gray-100">S'inscrire</a></li>
      <li><a href="#" class="px-6 py-4 text-white bg-gray-600 rounded-lg">Se connecter</a></li>
    </ul>
  </nav>
  </transition>

</template>

<script>
import Vue from 'vue'

export default Vue.extend({
  name: "Navbar"
})
</script>

<style scoped>

.transition {
  transition: all 0.5s;
}

.from-appear, .leaved {
  transform: translateX(-500px);
  opacity: 0;
}

.appeared, .goingToLeave {
  transform: translateX(0);
  opacity: 1;
}


</style>
