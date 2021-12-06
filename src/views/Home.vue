<template>
  <main id="home" class="quoter_wrapper">
      <h1 class="quoter_wrapper--title">randomQuoter</h1>
      <MainDisplay />
  </main>
</template>

<script>
import MainDisplay from '../components/MainDisplay.vue'
export default {
  components: { MainDisplay },
  name: 'Home'
}
</script>