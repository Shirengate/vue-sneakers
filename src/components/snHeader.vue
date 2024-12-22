<template>
  <header class="flex items-center justify-between border-b border-slate-300 p-8">
    <div class="leftSide flex items-center gap-4">
      <img src="/logo.png" alt="logo" class="w-10">
      <div>
        <h2 class="uppercase font-bold text-xl">vue sneakers</h2>
        <p class="title">Магазин лучших кроссовок</p>
      </div>
    </div>
  <sn-nav></sn-nav>
  </header>
</template>

<script setup>
import snHeader from "./uiComp/snNav.vue"
import SnNav from "@/components/uiComp/snNav.vue";
</script>

<style scoped>
p.title {
  color: #909090;
}
</style>
