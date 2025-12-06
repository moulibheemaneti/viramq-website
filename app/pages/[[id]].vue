<template>
   <section class="vq-policy">
      <ContentRenderer v-if="policy" :value="policy" />
   </section>
</template>

<script lang="ts" setup>
const route = useRoute();

const policy = ref();
onMounted(async () => {

   const id = route.params.id as string;

   policy.value = await queryCollection("policies")
      .where("id", "=", `policies/policies/${id}.md`)
      .first();

});
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
