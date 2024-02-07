<template>
  <div class="card">
    <img :src="card.card_images[0].image_url" alt="" />
    <div class="description">
      <h3 class="name">{{ card.name }}</h3>
      <br />
      <p class="type">{{ card.archetype || card.type }}</p>
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

<style scoped>
.card {
  background-color: white;
  transition: all 1s;
  height: 550px;
  background-color: orange;
  padding-bottom: 10px;

  &:hover {
    filter: drop-shadow(0 0 15px #507183);
    scale: 1.01;
  }

  > img {
    width: 100%;
    display: block;
  }

  > div {
    padding: 1rem;
  }
}
.description {
  background-color: orange;
}
.name {
  color: white;
  text-align: center;
}
.type {
  text-align: center;
}
.background-black {
  background-color: black;
}
</style>
