<template>
  <div class="footer-wrapper">
    <div class="footer">
      <div class="footer__block2">
        <div class="container">
          <div class="row">
            <div class="col-lg-10 col-sm-12 text-center">
              <script src="https://yastatic.net/share2/share.js"></script>
              <div
                class="ya-share2"
                data-curtain
                data-size="l"
                data-services="vkontakte,facebook,odnoklassniki,telegram,twitter,viber,whatsapp"
              ></div>
            </div>
            <div class="col-lg-2 col-sm-12 text-center">
              <v-btn fab outlined color="pink" @click="scrollTop">
                <v-icon>mdi-arrow-up-bold-outline</v-icon>
              </v-btn>
            </div>
          </div>
        </div>
      </div>
      <div class="footer__block1">
        © 2020 BeFestival - BeTheme. All Rights Reserved. Muffin group
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    scrollTop() {
      window.scrollTo({ top: 0, left: 0, behavior: 'smooth' })
    },
  },
}
</script>

<style></style>
