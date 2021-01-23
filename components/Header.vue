<template>
  <div class="header-wrapper">
    <div class="header">
      <div class="row">
        <div class="col-6">1</div>
        <div class="col-6">2</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({}),
  destroyed() {
    window.removeEventListener('scroll', this.handleScroll)
    window.removeEventListener('resize', this.handleScroll)
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll)
    window.addEventListener('resize', this.handleScroll)
  },
  methods: {
    handleScroll() {
      console.log(window.scrollY)
      // const el = this.observedElement
      // if (el) {
      //   console.log('el not null')
      //   const windowHeight = window.innerHeight // высота видимой области
      //   const offsetTop = this.$refs.controlls.offsetTop // отсут контрола от верха окна
      //   const windowScrollY = window.scrollY
      //   const diff = offsetTop - windowHeight
      //   if (diff >= windowScrollY) {
      //     this[appTypes.SET_BOTTOM_OFFSET](0)
      //   } else {
      //     this[appTypes.SET_BOTTOM_OFFSET](windowScrollY - diff)
      //   }
      // }
    },
  },
}
</script>

<style></style>
