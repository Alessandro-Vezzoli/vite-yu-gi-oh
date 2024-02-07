<template>
  <div class="col-12 col-sm-6 col-lg-4">
    <div class="card">
      <img :src="card.img" alt="" />
      <div>
        {{ card.name }}
        {{ card.type }}
      </div>
    </div>
  </div>
  <!-- /.col-12 col-sm-6 col-md-3 -->
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
</style>
