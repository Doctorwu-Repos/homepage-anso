<script setup lang="ts" generic="T extends any, O extends any">
defineOptions({
  name: 'IndexPage',
})

const router = useRouter()
router.replace('/home')
</script>

<template>
  跳转中...
</template>
