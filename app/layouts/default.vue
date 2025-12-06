<template>
   <Analytics />
   <vq-header />

   <main class="main">
      <nuxt-page />
   </main>

   <vq-footer />

   <vq-footer-decorator />
</template>

<script lang="ts" setup>
import { Analytics } from '@vercel/analytics/nuxt'

</script>

<style lang="scss">
.main {
   max-width: px-to-rem(800);
   display: flex;
   flex-direction: column;
   align-items: center;
   justify-content: center;
   margin: 0 auto;
   gap: px-to-rem(24);
   text-align: center;
   padding: 0 px-to-rem(16);

   @include tablet-up {
      gap: px-to-rem(32);
      padding: 0;
   }
}
</style>
