<template>
   <section class="vq-policy">
      <ContentRenderer v-if="policy" :value="policy" />
   </section>
</template>

<script lang="ts" setup>
const route = useRoute();
const id = route.params.id as string;

const policy = await queryCollection("policies")
   .where("id", "=", `policies/policies/${id}.md`)
   .first();

if (!policy) {
   throw createError({
      statusCode: 404,
      statusMessage: 'Page not found',
      fatal: true
   });
}


</script>

<style lang="scss">
.vq-policy {
   text-align: justify;
   padding: px-to-rem(24);

   h1,
   h2,
   h3,
   h4,
   h5,
   h6 {
      margin-top: px-to-rem(16);
      margin-bottom: px-to-rem(8);
   }
}
</style>
