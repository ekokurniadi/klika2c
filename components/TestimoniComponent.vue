<template>
  <div>
    <div class="container-fluid">
      <div class="row">
        <div class="col-md-12 yellow-section">
          <h3 class="yellow-section-title">Kisah Peminjam Dana</h3>
          <p class="yellow-section-subtitle">
            Kisah-kisah sukses pengguna KlikACC yang berhasil merubah hidupnya
            dengan KlikACC
          </p>
        </div>
      </div>
      <div class="row">
        <div class="image-testimoni-group">
          <div class="image-testimoni-item" v-for="item of testimoniData" :key="item.id">
              <img
                :src="'/images/' + item.image_thumbnail"
                :alt="item.image_thumbnail"
                class="img-testimoni"
              />
              <div class="circle-button-read">
                <a href="">Baca kisah {{ item.person_name }}</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import testimoniDatas from '@/assets/data/testimoni.json'
export default {
  data() {
    return {
      testimoniData: {},
    }
  },
  mounted() {
    this.fetchData()
  },
  methods: {
    fetchData() {
      this.testimoniData = testimoniDatas.data
      console.log(this.testimoniData)
    },
  },
}
</script>
