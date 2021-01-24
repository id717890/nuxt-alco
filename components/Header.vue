<template>
  <div class="header-wrapper container-fluid ma-0 pa-0">
    <div ref="header" class="header">
      <div class="row">
        <div class="col-12">
          <nav class="nav-menu">
            <ul class="menu">
              <li class="menu__item">
                <nuxt-link to="/" class="menu__item__link"> home </nuxt-link>
              </li>
              <li class="menu__item">
                <nuxt-link to="/about" class="menu__item__link">
                  about
                </nuxt-link>
              </li>
              <li class="menu__item">
                <nuxt-link to="/donate" class="menu__item__link">
                  donate
                </nuxt-link>
              </li>
            </ul>
          </nav>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  computed: {
    route() {
      return this.$route
    },
  },
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
      const scrollY = window.scrollY
      const headerElement = this.$refs.header
      if (scrollY > 50) {
        if (!headerElement.classList.contains('header-sticky')) {
          headerElement.classList.add('header-sticky')
        }
      } else {
        if (headerElement.classList.contains('header-sticky')) {
          headerElement.classList.remove('header-sticky')
        }
      }
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
