<template>
  <view class="default-layout" :class="[appStore.isDark ? 'dark' : 'light']">
    <MPage>
      <slot></slot>
      <MFooter></MFooter>
    </MPage>
  </view>
</template>

<script setup lang="ts">
  import { useAppStore } from '@/stores/modules/appStore'

  defineOptions({ name: 'DefaultLayout' })

  const appStore = useAppStore()
</script>

<style scoped lang="scss">
  .default-layout {
    @apply relative flex flex-col flex-1 h-full overflow-y-auto color-text-1;
  }
</style>
