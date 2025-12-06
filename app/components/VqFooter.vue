<template>
   <footer class="vq-footer">
      <div class="vq-footer__links">
         <NuxtLink to="/terms-of-service">Terms of Service</NuxtLink>
         <NuxtLink to="/privacy-policy">Privacy Policy</NuxtLink>
      </div>
      <p>&copy; 2025 ViramQ — Pause. Breathe. Recharge. All rights reserved.</p>
   </footer>
</template>

<script lang="ts" setup>
</script>

<style lang="scss">
.vq-footer {
   text-align: center;
   padding: px-to-rem(24);
   font-size: px-to-rem(12);
   margin-top: px-to-rem(48);

   &__links {
      display: flex;
      justify-content: center;
      gap: px-to-rem(24);
      margin-bottom: px-to-rem(16);
      color: #8E8E8E;

      a:hover {
         color: #F5F0BB;
         cursor: pointer;
         transition: all 0.3s ease;
      }
   }

   @include tablet-up {
      font-size: px-to-rem(14);
      line-height: 1;
   }
}
</style>
