<template>
  <div class="layout">
    <Navbar />
    <slot></slot>
    <div class="footer">
      Test
    </div>
  </div>
</template>

<script>
  import Navbar from '~/components/Navbar.vue';

  export default {
    components: {
      Navbar
    }
  }
</script>

<style lang="scss">
  .footer {
    display: none;
    position: absolute;
    bottom: 0;
    width: 100%;
    background: green;
    padding: 3em 0;
  }
</style>
