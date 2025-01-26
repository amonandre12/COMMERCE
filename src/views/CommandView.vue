<script setup>
import {ref} from 'vue'
const title = ref ('Les commandes')
 import ButtonGroup from '@/components/ButtonGroup.vue'
 import LivraisonSection from '@/components/LivraisonSection.vue'
 import ShopSection from '@/components/ShopSection.vue'
 import ContentShop from '@/components/ContentShop.vue'
 import ContainerShop from '@/components/ContainerShop.vue'
 import ContenuBoutique from '@/components/ContenuBoutique.vue'
 import ShopContent from '@/components/ShopContent.vue'
 import ShopSend from '@/components/ShopSend.vue'
 import ExpeditionContent from '@/components/ExpeditionContent.vue'
 import DeletedContent from '@/components/DeletedContent.vue'
</script>
<template>
  <section>
    <div class="container">
  <div class="containers">
    <div class="breadcrumb">
    <span>Commande</span>
    <span class="symbole">&gt;</span>
    <span>Aperçu</span>
    </div>
    <h1>{{title}}</h1>
    <div  class="navbar">
      <button class="nav-btn-active">Aperçu</button>
      <button class="nav-button">Retours & Echanges</button>
      <button class="nav-button">Panier Abandonnés</button>
      <button class="nav-button">Factures</button>
    </div>
    <div class="container-fluid">
    <div>
      <form class="d-flex" role="search">
      <input class="form-control me-2" type="search" placeholder="recherche commande" aria-label="Search">
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
  <ButtonGroup/>
  <LivraisonSection/>
  <ShopSection/>
  <ContentShop/>
  <ContainerShop/>
  <ContenuBoutique/>
  <ShopContent/>
  <ShopSend/>
  <ExpeditionContent/>
  <DeletedContent/>
</template>

<style scoped>
.nav-btn-active {
  background-color: blue;
  color: #ccc;
  cursor: pointer;
}
.container-fluid {
  display: flex;
  flex-direction: row;
  gap: 100px;
  margin-top: 40px;
}

.breadcrumb {
  color: #666;
  text-decoration: underline;
}
.breadcrumb span {
  font-size: 1.2em;
}
.symbole{
position: relative;
top: 2px;
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
  gap: 10px;
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
  TOP: 8px;
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
