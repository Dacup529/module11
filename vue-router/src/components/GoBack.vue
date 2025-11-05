<template>
  <button @click="goBack">Go Back</button>
</template>

<script>
import { useRouter } from 'vue-router'

export default {
  name: 'GoBack',
  setup() {
    const router = useRouter()
    const goBack = () => {
      router.go(-1)
    }
    return { goBack }
  }
}
</script>

<style>
button {
  margin-top: 20px;
  padding: 8px 16px;
  font-size: 16px;
}
</style>
