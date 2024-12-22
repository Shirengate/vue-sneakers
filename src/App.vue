<template>
<!--  <draver></draver>    корзина-->
  <div class="w-4/5 mx-auto  bg-white  rounded-xl shadow-xl mt-14">
    <sn-header></sn-header>   <!-- header-->
    <sn-main :items="items"></sn-main> <!-- main -->
  </div>
</template>

<script setup>
import SnHeader from "@/components/snHeader.vue";
import SnMain from "@/components/snMain.vue";
import draver from "@/components/draver.vue";

const items = [
  {
    "id": 1,
    "title": "Мужские Кроссовки Nike Blazer Mid Suede",
    "price": 12999,
    "imageUrl": "/sneakers/sneakers-1.jpg"
  },
  {
    "id": 2,
    "title": "Мужские Кроссовки Nike Air Max 270",
    "price": 15600,
    "imageUrl": "/sneakers/sneakers-2.jpg"
  },
  {
    "id": 3,
    "title": "Мужские Кроссовки Nike Blazer Mid Suede",
    "price": 8499,
    "imageUrl": "/sneakers/sneakers-3.jpg"
  },
  {
    "id": 4,
    "title": "Кроссовки Puma X Aka Boku Future Rider",
    "price": 7800,
    "imageUrl": "/sneakers/sneakers-4.jpg"
  },
  {
    "id": 5,
    "title": "Кроссовки Future Rider",
    "price": 9550,
    "imageUrl": "/sneakers/sneakers-5.jpg"
  },
  {
    "id": 6,
    "title": "Кроссовки Black Edition",
    "price": 16999,
    "imageUrl": "/sneakers/sneakers-6.jpg"
  },
  {
    "id": 7,
    "title": "Кроссовки Orange Boomb Edition",
    "price": 7499,
    "imageUrl": "/sneakers/sneakers-7.jpg"
  },
  {
    "id": 8,
    "title": "Кроссовки Nike Air Max 270",
    "price": 15600,
    "imageUrl": "/sneakers/sneakers-8.jpg"
  },
  {
    "id": 9,
    "title": "Кроссовки Nike Air Force 1",
    "price": 5900,
    "imageUrl": "/sneakers/sneakers-9.jpg"
  },
]
</script>

<style scoped lang="scss" >
@mixin  cardSettings{
  display: grid;
  grid-template-columns: repeat(3,1fr);
  justify-items: center;
  align-items: center;

};
.card-box{
  @include  cardSettings;
  .card{
    margin-top: 20px;
    transition: all .4s;
    width: 320px;
    &:hover{
      transform: scale(0.99);
      transform: translateY(-10px);
    };

  }
};
</style>
