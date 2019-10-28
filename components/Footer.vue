<template>
  <div class="footer">
    <h3>Footer.vue</h3>
    <div v-for="link in locale.links" :key="link.href">
      <a :href="`${link.href}`">{{ link.name }}</a>
    </div>
  </div>
</template>

<script>
  export default {
    props: ['locale']
  }
</script>

<style>
  .footer {
    background: #eee;
    border-top: 2px solid #333;
    padding: 1em;
    text-align: center;
    height: 50vh;
    box-sizing: border-box
  }
</style>