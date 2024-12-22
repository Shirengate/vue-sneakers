<template>
  <main>
    <div class="flex justify-between items-center mx-5">
      <h2 class="text-3xl font-bold mt-2 text-center">Все кроссовки</h2>
      <select class="text-center items-center  border border-2 border-slate-500 ">
        <option selected>Стандарт</option>
        <option>По цене(возврастанию)</option>
        <option>По цене(убыванию)</option>
      </select>
      <input type="text" class="mt-5" placeholder="Поиск..">
    </div>
    <div class="card-box mt-10">
      <card  v-for="item in items" :img-url="item.imageUrl" :cost="item.price" :title="item.title"></card>

    </div>
  </main>
</template>

<script setup>
import card from "./uiComp/card.vue"

defineProps({
  items:Array,

})
</script>

<style lang="scss" scoped>
@mixin  cardSettings{
  display: grid;
  grid-template-columns: repeat(3,1fr);
  justify-items: center;
  align-items: center;

};
.card-box{
  @include cardSettings;
}
input{
  width: 200px;
  height: 32px;
  border: 1px solid lightgray;
  border-radius: 5px;
  transition: all .4s;
  &:focus{
    outline:  1px solid gray;
  };
  &::placeholder{
    padding-left: 10px;
  }
}
</style>
