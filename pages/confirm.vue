<script setup lang="ts">
const user = useSupabaseUser()

watch(user, () => {
  if (user.value) {
    return navigateTo('/todos')
  }
}, { immediate: true })
</script>

<template>
  <div>
    <p class="u-text-black">
      Redirecting...
    </p>
  </div>
</template>
