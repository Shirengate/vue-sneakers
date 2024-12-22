<template>
  <div class="card relative border bg-white border-slate-100 rounded-3xl hover:shadow-xl p-8 cursor-pointer">
    <img :src="isFavorite ? '/like-2.svg' : '/like-1.svg'" alt="like1" class="absolute top-8 left-8">
    <img :src="imgUrl" alt="firstSneaker">
    <p class="mt-2">{{ title }}</p>
    <div class="flex justify-between mt-5">
      <div class="fex justify-between ">
        <div class="flex flex-col "><span class="text-slate-500">Цена:</span><b>{{ cost }} руб.</b></div>
      </div>
      <img :src=" !isAdded ? '/plus.svg' : '/checked.svg'" alt="add" @click="addToCard">
    </div>
  </div>
</template>

<script setup>
defineProps({
  imgUrl:{
    type: String,

  },
  title:{
    type: String,
    required: true,
  },
  cost:{
    type: [String, Number],
    required: true,
  },
  isFavorite:{
    type: Boolean,
    default: false,
  },
  isAdded:{
    type: Boolean,
    default: false,
  }
})
</script>

<style lang="scss" scoped>

.card {
  margin-top: 20px;
  transition: all .4s;
  width: 320px;

  &:hover {
    transform: scale(0.99);
    transform: translateY(-10px);
  }
;
}

</style>
