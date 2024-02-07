<template>
  <div class="container">
    <div class="filters">
      <select name="status" id="status">
        <option value="" selected>All</option>
        <option value="alien">Alien</option>
      </select>
    </div>
    {{ cardItems.name }}
    <CardItems
      v-for="card in cardItems"
      :key="card.id + '_card'"
      :card="cardItems"
    ></CardItems>
  </div>
</template>

<script>
import axios from "axios";
import CardItems from "./CardItems.vue";
export default {
  name: "AppMain",
  components: { CardItems },
  data() {
    return {
      url_api: "https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0",
      cardItems: [],
      error: false,
    };
  },
  mounted() {
    console.log(this.url_api);
    axios
      .get(this.url_api)
      .then((res) => {
        this.cardItems = res.data.data;

        console.log(this.cardItems);
      })
      .catch((error) => {
        console.error("Errore durante la chiamata Axios:", error);
      });
  },
};
</script>

<style scoped></style>
