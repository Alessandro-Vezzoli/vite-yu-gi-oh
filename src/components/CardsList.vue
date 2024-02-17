<template>
  <section class="cards">
    <div class="container">
      <div class="row">
        <div class="col" v-for="card in cards">
          <CardItems :card="card"></CardItems>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
import CardItems from "./CardItems.vue";

export default {
  name: "CardsList",
  props: {
    cards: Array,
  },
  components: { CardItems },
};
</script>

<style scoped></style>
