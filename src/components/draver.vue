<template>
  <div class="fixed top-0 left-0 z-10 h-full w-full bg-black opacity-60">

  </div>
  <div class="bg-white h-full fixed right-0 top-0 z-20 p-10 cartCurtain flex flex-col justify-between">
    <div class="flex-1">
      <div class="flex items-center gap-5">
        <svg class="" width="20" height="20" viewBox="0 0 16 14" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M1 7H14.7143" stroke="black" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
          <path d="M8.71436 1L14.7144 7L8.71436 13" stroke="black" stroke-width="2" stroke-linecap="round"
                stroke-linejoin="round"/>
        </svg>
        <h2 class="text-3xl font-bold ">Корзина</h2>
      </div>
      <cart-list></cart-list>
    </div>

    <footer>
      <div class="info flex justify-center mt-5">
        <span>Итого:</span>
        <div class="flex-1 border-dotted border-slate-300 border-b "></div>
        <b>12900 руб</b>
      </div>
      <button  class="bg-green-500 text-white  text-center rounded-2xl w-full h-12 mt-5 hover:bg-green-700 transition-all duration-200 disabled:bg-slate-400">Оформить заказ</button>
    </footer>
  </div>
</template>

<script setup>
import cartList from "./uiComp/cartList.vue";
</script>

<style lang="scss" scoped>
@mixin arrowClose {
  transform: rotate(180deg);
  cursor: pointer;
}

svg {
  transition: .2s ease-in-out;
  text-align: center;

  &:hover {
    @include arrowClose;
  }
};
.cartCurtain{
  width: 30%;
}

</style>
