<script setup>
import {ref} from 'vue'
const title = ref ('Les produits')
import { useRouter } from 'vue-router';
const router = useRouter()
const navigateTo = (AjouterProduitView) => {
  router.push((AjouterProduitView))
}
import ProductButton from '@/components/ProductButton.vue'
import ProductSection from '@/components/ProductSection.vue'
import ProductContent from '@/components/ProductContent.vue'
import ProductContainer from '@/components/ProductContainer.vue'
import ProductCard from '@/components/ProductCard.vue'
import ContentProduct from '@/components/ContentProduct.vue'
import ContainerProduct from '@/components/ContainerProduct.vue'
import CardProduct from '@/components/CardProduct.vue'
import SectionProduct from '@/components/SectionProduct.vue'
import ProductContents from '@/components/ProductContents.vue'
</script>

<template>
   <section>
    <div class="container">
  <div class="containers">
    <div class="breadcrumb">
    <span>Produit</span>
    <span class="symbole">&gt;</span>
    <span>Aperçu</span>
    <span class="symbole">&gt;</span>
    <span @click="navigateTo('AjouterProduitView')">Ajouter un produit</span> 
    </div>
    <h1>{{title}}</h1>
    <div  class="navbar">
      <button class="nav-btn-active">Aperçu</button>
      <button class="nav-button">Inventaire</button>
      <button class="nav-button">Catégories</button>
      <button class="nav-button">Attribue</button>
      <button class="nav-button">Upsells</button>
      <button class="nav-button">Factures</button>
      <button class="nav-button">Promo codes</button>
    </div>
    <div class="container-fluid">
    <div>
      <form class="d-flex" role="search">
      <input class="form-control me-2" type="search" placeholder="recherche produits" aria-label="Search">
    </form>
      </div>
      <div class="para">
      <button class="btn"><box-icon type='solid' name='arrow-from-bottom'></box-icon>Exporter</button>
      <button class="btn"><box-icon name='slider-alt'></box-icon>Filtrer</button>
      <button class="command"><box-icon name='plus-circle'></box-icon>Ajouter une commande</button>
    </div>
    </div>
    </div>
  </div>
  </section>
  <ProductButton/>
  <ProductSection/>
  <ProductContent/>
  <ProductContainer/>
  <ProductCard/>
  <ContentProduct/>
  <ContainerProduct/>
  <CardProduct/>
  <SectionProduct/>
  <ProductContents/>
</template>

<style lang="css" scoped>
.nav-btn-active {
  background-color: blue;
  color: #ccc;
  cursor: pointer;
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
.container-fluid {
  display: flex;
  flex-direction: row;
  gap: 100px;
  margin-top: 40px;
}
.btn{
background-color: transparent;
padding: 6px;
border-color: #ccc ;
}
.para {
display: flex;
gap: 40px;
position: relative;
left: 20%;
top: 21px;
}
.para button {
  font-size: 1.3em;
  text-align: center;
  cursor: pointer;
}
.command {
  background-color: #333;
  color: #ccc;
}
.command box-icon {
  color: white;
}
.para box-icon {
  position: relative;
  top: 3px;
  right: 10px;
}

form {
  position: relative;
  top: 29px;
  background-color: transparent;
}
input {
  width: 180px;
  height:38px;
  background-color: transparent;
}
.navbar {
  display: flex;
  gap: 17px;
  background-color: #f8f8f8;
  padding: 10px;
  border-bottom: 1px solid #ccc;
  position: relative;
  right: 62px;
}
.nav-button {
  background-color: #ffffff;
  border: 1px solid #ccc;
  border-radius: 5px;
  padding: 8px 16px ;
  font-size: 16px;
  color: #ccc;
  cursor: pointer;
  transition: background-color 0.3s, color 0.3s;
}

.nav-button:hover {
  background-color: #e5e5e5;
}
h4 {
  text-decoration: underline;
}
.icon {
  text-decoration: underline;
  position: relative;
  top: 8px;
}
h1 {
  font-size: 2.4em;
}
section {
  display: flex;
}
.containers {
  position: absolute;
  left: 33%;
  top: 98px;
}
</style>
