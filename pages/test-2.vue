<template>
  <div>
    <h1>Test 2</h1>
    <p>This is test page 2.</p>
    <ul>
      <li><nuxt-link to="/">Home</nuxt-link></li>
      <li><nuxt-link to="/test-1">Test 1</nuxt-link></li>
      <li>Test 2</li>
    </ul>
  </div>
</template>

<script>
  export default {
    head() {
      return {
        title: "Test 2",
        script: [{
          src: "https://cdnjs.cloudflare.com/ajax/libs/jquery/3.3.1/jquery.slim.min.js"
        }]
      };
    },
    mounted() {
      if (!process.server && window.jQuery) {
        window.jQuery("h1").append(` <span class="cdn-loaded-message">(CDN script has loaded)</span>`);
      }
    }
  }
</script>

<style>
  span {
    font-size: 14px;
    font-weight: normal;
  }
</style>
