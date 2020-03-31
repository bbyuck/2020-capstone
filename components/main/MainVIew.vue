<template>
  <v-ons-tabbar position="auto"
    :tabs="tabs"
    :visible="true"
    :index.sync="activeIndex"
  >
  </v-ons-tabbar>
</template>

<script>
import HomeView from './home_tab/HomeView.vue'
import SearchView from './search_tab/SearchView.vue'
import MypageView from './mypage_tab/MypageView.vue'
import OrderListView from './order_tab/OrderListView.vue'

export default {
  data: function() {
    return {
      activeIndex: 0,
      tabs: [
        {
          icon: 'fa-home',
          label: 'Home',
          page: HomeView,
          key: "homeView"
        },
        {
          icon: 'fa-search',
          label: '검색',
          page: SearchView,
          badge: 7,
          key: "searchView"
        },
        {
          icon: 'fa-clipboard-list',
          label: '주문 내역',
          page: OrderListView,
          key: "orderListView"
        },
        {
          icon: 'fa-user',
          label: '마이페이지',
          page: MypageView,
          key: "myPageView"
        }
      ]
    }
  },
  components: {
    HomeView,
    SearchView,
    OrderListView,
    MypageView
  }
}
</script>

<style>

</style>