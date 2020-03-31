<template>
  <v-ons-page>
    <div class="category_area">
      <banner-area></banner-area>
      <area-header v-bind:area-name="homeArea[0]"></area-header>
      <category-area></category-area>
      <delivery-area></delivery-area>
      <app-footer></app-footer>
    </div>
  </v-ons-page>
</template>

<script>
import CategoryArea from './CategoryArea.vue'
import AreaHeader from './AreaHeader.vue'
import BannerArea from './BannerArea.vue'
import DeliveryArea from './DeliveryArea.vue'
import AppFooter from '../../common/AppFooter.vue'


export default {
  data: function () {
    return {
      homeArea: ['상품 카테고리', '배달 위치 확인']
    }
  },
  components: {
    CategoryArea,
    AreaHeader,
    BannerArea,
    DeliveryArea,
    AppFooter
  }
}
</script>

<style>

</style>