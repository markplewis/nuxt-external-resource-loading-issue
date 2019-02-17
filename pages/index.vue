<template>
  <div>
    <h1>Home</h1>
    <p>This is the home page.</p>
    <ul>
      <li>Home</li>
      <li><nuxt-link to="/test-1">Test 1</nuxt-link></li>
      <li><nuxt-link to="/test-2">Test 2</nuxt-link></li>
    </ul>
  </div>
</template>

<script>
  export default {
    head() {
      return {
        title: "Home"
      };
    }
  }
</script>
