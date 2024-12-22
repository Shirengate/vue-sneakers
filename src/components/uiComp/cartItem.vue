<template>
  <div class="border rounded-lg itemBox p-3">
    <img src="/sneakers/sneakers-1.jpg" alt="" class="w-20">
    <div class="flex flex-col">
      <p class="text-wrap">Мужские кроссовки Nike</p>
      <b>1500 руб.</b>
    </div>
    <img src="/close.svg" alt="close" class="close cursor-pointer">
  </div>
</template>

<style lang="scss" scoped>
.itemBox {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  justify-items: center;
  align-items: center;
};
.close{
  align-self: end;
  justify-self: end;
  margin-bottom: 10px;
  margin-right: 10px;
}
</style>
