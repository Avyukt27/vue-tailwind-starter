<template>
  <div class="min-h-screen bg-white text-black dark:bg-black dark:text-white">
    <h1 class="text-center text-2xl font-bold p-4">Welcome to My Page</h1>
  </div>
</template>

<script>
export default {
  mounted() {
    // Check for user's preferred color scheme
    const darkModeMediaQuery = window.matchMedia('(prefers-color-scheme: dark)');

    // Add or remove the dark class based on the user's preference
    if (darkModeMediaQuery.matches) {
      document.documentElement.classList.add('dark');
    }

    // Listen for changes in the preference
    darkModeMediaQuery.addEventListener('change', (event) => {
      if (event.matches) {
        document.documentElement.classList.add('dark');
      } else {
        document.documentElement.classList.remove('dark');
      }
    });
  },
};
</script>

<style scoped>
/* Additional styles if necessary */
</style>