<template>
  <div class="home">
    <div class="title mt-5 text-center">
      <h3>New Product</h3>
    </div>
    <div class="d-flex justify-content-between size p-3 mt-2">
      <div v-for="item in fetchSeriesGold" :key="item.id" class="card" style="width: 18rem;">
        <img :src="item.image" alt="loading .." class="card-img-top mx-auto mt-3">
        <div class="card-body text-center">
          <h4 class="card-title">{{ item.name }}</h4>
          <a href="#" @click.prevent="showModal(item)" class="card-link">View Details</a>
        </div>
      </div>
      <Modal :data="item" />
    </div>
  </div>
</template>

<script>
import Modal from './ModalDetail.vue';

export default {
  name: 'item-home',
  components: {
    Modal,
  },
  data() {
    return {
      item: null,
    };
  },
  methods: {
    showModal(data) {
      this.item = data;
      this.$bvModal.show('modal-lg');
    },
  },
  computed: {
    fetchSeriesGold() {
      return this.$store.state.seriesGold.slice(0, 3);
    },
  },
  created() {
    this.$store.dispatch('fetchSeriesGold');
  },
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Hind+Siliguri&display=swap');

.home {
 font-family: 'Hind Siliguri', sans-serif;
}

.title {
  color: #cb9b2d;
  font-weight: bold !important
}

.size {
  height: 400px !important;
}

.card {
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
  border: none;
  width: 32% !important;
  height: 330px !important;
}

.card-link {
  color: #cb9b2d !important;
  font-weight: bold
}
.card-link:hover {
  color: #23427e !important;
  font-weight: bold
}

.card-img-top {
  width: 300px !important
}

.card-img-top:hover {
  transform:scale(1.05);
  transition-duration: 0.2s;
}

</style>
