<template>
    <div class="category_container">
      <div class="category">
        <div v-for="(item, i) in category" v-bind:key="i" class="category_btn center">
          <img v-bind:src="item.imgUrl">
          <p class="category_title">{{ item.name }}</p>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  data: function () {
    return {
      category: [
        {
          imgUrl: './src/assets/images/icons/kimchi.png',
          name: '반찬'
        },
        {
          imgUrl: './src/assets/images/icons/meat.png',
          name: '축산'
        },
        {
          imgUrl: './src/assets/images/icons/bed-sheets.png',
          name: '침구'
        },
        {
          imgUrl: './src/assets/images/icons/vegetable.png',
          name: '농산물'
        },
        {
          imgUrl: './src/assets/images/icons/desk.png',
          name: '생활용품'
        },
        {
          imgUrl: './src/assets/images/icons/eat.png',
          name: '식당'
        },
        {
          imgUrl: './src/assets/images/icons/dried-fish.png',
          name: '건어물'
        },
        {
          imgUrl: './src/assets/images/icons/rice-cake.png',
          name: '방앗간'
        },
        {
          imgUrl: './src/assets/images/icons/fabric.png',
          name: '원단'
        }
      ]
    }
  }
}
</script>

<style>
.category_container {
  overflow: scroll;
  height: 230px;
  margin-top: 5%;
}

.category {
  width: 540px;
}

.category_btn {
  width: 65px;
  height: 65px;
  display: inline-block;
  margin: 20px;
  margin-bottom: 0;
  background-color: white;
  box-shadow: 3px 3px 3px 3px gray;
}

.category_btn > img {
  width: 100%;
}

.category_title {
  margin-top: 5px;
  font-size: 15px;
}
</style>