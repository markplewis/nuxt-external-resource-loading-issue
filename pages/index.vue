<template>
  <div>
    <h1>Home page</h1>
    <p>This is the home page.</p>
    <ul>
      <li>Home page</li>
      <li><nuxt-link to="/test">Test page</nuxt-link></li>
    </ul>
  </div>
</template>

<script>
  export default {
    head() {
      return {
        title: "Home page"
      };
    }
  }
</script>
