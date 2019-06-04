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
    // head() {
    //   return {
    //     title: "Test 1",
    //     script: [{
    //       src: "https://cdnjs.cloudflare.com/ajax/libs/jquery/3.3.1/jquery.slim.min.js"
    //     }]
    //   };
    // },
    // async asyncData({ $axios }) {
    //   let jQueryString = await $axios.$get("https://cdnjs.cloudflare.com/ajax/libs/jquery/3.3.1/jquery.slim.min.js");
    //   return { jQueryString };
    // },
    mounted() {
      if (!window.jQuery) {
        const script = document.createElement("script");
        script.onload = this.onCDNScriptLoaded;
        script.type = "text/javascript";
        script.src = "https://cdnjs.cloudflare.com/ajax/libs/jquery/3.3.1/jquery.slim.min.js";
        document.head.appendChild(script);
      } else {
        this.onCDNScriptLoaded();
      }
    },
    methods: {
      onCDNScriptLoaded(event = null) {
        if (event) {
          console.log("PG1 - Was added");
        } else {
          console.log("PG1 - Already existed");
        }
        console.log(window.jQuery);
        window.jQuery("h1").append(` <span>(CDN script has loaded)</span>`);
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
