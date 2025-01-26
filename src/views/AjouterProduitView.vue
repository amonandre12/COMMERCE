<script setup>
import {ref} from 'vue'
const title = ref ('Ajouter un produit')
import ProductLabel from '@/components/ProductLabel.vue'
import DescriptionContent from '@/components/DescriptionContent.vue'
import TarificationSection from '@/components/TarificationSection.vue'
import ImageSection from '@/components/ImageSection.vue'
import ProductForm from '@/components/ProductForm.vue'
</script>

<template>
  <section>
  <div class="container">
    <div class="breadcrumb">
    <span>Produits</span>
    <span class="symbole">&gt;</span>
    <span>Tous</span>
    <span class="symbole">&gt;</span>
    <span>Ajouter un produit</span>
    </div>
    <h1>{{title}}</h1>
  </div>
  </section>
  <ProductLabel/>
  <DescriptionContent/>
  <TarificationSection/>
  <ImageSection/>
  <ProductForm/>
</template>

<style lang="css" scoped>
section {
  display: flex;
}
h1 {
  font-size:2.4em;
  position:relative;
  top:30px;
}
.container {
  position: absolute;
  left:30%;
  top: 26%;
}
.breadcrumb {
  color: #666;
  text-decoration: underline;
  cursor: pointer;
}
.breadcrumb span {
  font-size: 1.2em;
}
.symbole{
position: relative;
top: 2px;
}
</style>
