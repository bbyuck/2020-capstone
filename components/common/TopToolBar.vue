<template>
  <v-ons-toolbar style="text-align: center;">
    <div class="center" v-if="!addr_mod" v-on:click="modifyAddr">{{ addr }}</div>
    <div class="center" v-if="addr_mod">
      <v-ons-input v-model="addr" placeholder="주소 변경 입력"></v-ons-input>
      <v-ons-button class="change_btn" v-on:click="modifyConfirm">변경</v-ons-button>
    </div>
  </v-ons-toolbar>
</template>

<script>
export default {
  data: function () {
    return {
      addr_mod: false,
      addr: '초기주소'
    }
  },
  methods: {
    modifyAddr: function () {
      this.addr_mod = true;
    },
    modifyConfirm: function (){
      this.addr_mod = false;
    }
  }
}
</script>

<style>
.change_btn {
  width: 15%;
}
</style>