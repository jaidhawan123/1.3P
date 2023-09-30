<template>
  <div class="about">
    <h2>About Page</h2>
    <router-link to="/about">Go to About Page</router-link>

    <p>This is the about page content.</p>
  </div>
</template>

<script>
export default {
  name: 'about-page', // Updated component name to kebab-case
};
</script>

<style scoped>
/* Add your component-specific styles here */
</style>
