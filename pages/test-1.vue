<template>
  <div>
    <h1>Test 1</h1>
    <p>This is test page 1.</p>
    <ul>
      <li><nuxt-link to="/">Home</nuxt-link></li>
      <li>Test 1</li>
      <li><nuxt-link to="/test-2">Test 2</nuxt-link></li>
    </ul>
  </div>
</template>

<script>
  export default {
    head() {
      return {
        title: "Test 1",
        script: [{
          src: "https://cdnjs.cloudflare.com/ajax/libs/jquery/3.3.1/jquery.slim.min.js"
        }]
      };
    },
    mounted() {
      window.jQuery("h1").append(` <span>(CDN script has loaded)</span>`);
    }
  }
</script>

<style>
  span {
    font-size: 14px;
    font-weight: normal;
  }
</style>
