<template>
  <div>
    <div v-if="hasHDimg" class="container-fluid ma-0 pa-0">
      <v-img :src="item.imgHD"></v-img>
    </div>
    <div class="container">
      <div class="d-flex justify-content-center">
        <v-img
          v-if="hasImg"
          max-width="500"
          max-height="400"
          :src="item.img"
        ></v-img>
      </div>

      <div class="the-fact">
        <div v-if="title" class="the-fact__title text2 text-center">
          {{ title }}
        </div>
        <div v-if="text" class="the-fact__text">
          {{ text }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    item: {
      type: Object,
      default: null,
    },
  },
  computed: {
    hasImg() {
      return this.item?.img && !this.hasHDimg
    },
    hasHDimg() {
      return this.item?.imgHD
    },
    title() {
      return this.item?.title
    },
    text() {
      return this.item?.text
    },
  },
}
</script>
