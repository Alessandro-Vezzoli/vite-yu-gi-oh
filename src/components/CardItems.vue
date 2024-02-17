<template>
  <div class="card">
    <img :src="card.card_images[0].image_url" />
    <h3>{{ card.name }}</h3>
    <div>
      {{ card.archetype }}
    </div>
  </div>
</template>
<script>
export default {
  name: "CardItems",
  props: {
    card: Object,
  },
};
</script>

<style scoped></style>
