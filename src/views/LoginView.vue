<script setup lang="ts">
import { useRouter } from 'vue-router'

const router = useRouter()

const callback = (response) => {
  // This callback will be triggered when the user selects or login to
  // his Google account from the popup
  console.log('Handle the response', response)
  router.push('/home')
}
</script>
<template>
  <div class="min-h-screen flex justify-center items-center">
    <GoogleLogin :callback="callback" />
  </div>
</template>
