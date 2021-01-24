<template>
  <div class="the-fact-wrapper" @click="openTheFact(item.id)">
    <div class="triangle1"></div>
    <div class="triangle2"></div>
    <v-img class="fact-img" height="325" :src="item.img"></v-img>
    <!-- <img
      class="img"
      src="https://themes.muffingroup.com/be/festival/wp-content/uploads/2019/07/festival-pic1.jpg"
      alt=""
    /> -->
    <div class="fact-title">
      <h3 class="text1 text-center">{{ item.title }}</h3>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    item: {
      type: Object,
      required: true,
    },
  },
  methods: {
    openTheFact(id) {
      this.$router.push(`/fact/${id}`)
    },
  },
}
</script>

<style></style>
