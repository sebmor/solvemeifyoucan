<template>
  <div>
    <h2 class="subtitle">SPA Page</h2>
    <p>Number of times loaded {{this.$store.state.count.number}}</p>
  </div>
</template>


<script>
export default {
  layout: 'spa',
}
</script>
