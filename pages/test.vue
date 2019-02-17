<template>
  <div>
    <h1>Test page</h1>
    <p>This is the test page.</p>
    <ul>
      <li><nuxt-link to="/">Home page</nuxt-link></li>
      <li>Test page</li>
    </ul>
  </div>
</template>

<script>
  export default {
    head() {
      return {
        title: "Test page",
        script: [{
          src: "https://cdnjs.cloudflare.com/ajax/libs/jquery/3.3.1/jquery.slim.min.js"
        }]
      };
    },
    mounted() {
      // if (!process.server && window.jQuery) {
        window.jQuery("h1").append(` <span class="cdn-loaded-message">(CDN script has loaded)</span>`);
      // }
    }
  }
</script>
