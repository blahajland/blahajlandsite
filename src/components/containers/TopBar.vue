<script setup lang="ts">
import ThingsContainer from '@/components/containers/ThingsContainer.vue'
import { assets } from 'blahaj-library'
</script>

<template>
  <div class="TopBar">
    <RouterLink to="/">
      <img alt="Logo" :src="assets.images.pictures.get('text-logo')" />
    </RouterLink>
    <ThingsContainer>
      <slot></slot>
    </ThingsContainer>
  </div>
</template>

<style lang="sass">
.TopBar
  display: flex
  align-items: center

  > a > img
    filter: var(--filter)

@media (min-width: 1201px)
  .TopBar
    flex-direction: row
    justify-content: space-between
    padding: 24px

    > a > img
      height: 32px

@media (max-width: 1200px)
  .TopBar
    flex-direction: column
    justify-content: center
    gap: 16px
    padding: 24px

    > a > img
      height: 36px
</style>
