<script setup>

import { ref } from "vue";

// Données réactives
const visibility = ref(false);
const sku = ref("");
const barcode = ref("");
const weight = ref(0);
const trackInventory = ref(false);
const categorySearch = ref("");
const tags = ref("");

// Fonction pour ajouter une catégorie
const addCategory = () => {
  if (categorySearch.value.trim()) {
    alert(`Nouvelle catégorie ajoutée : ${categorySearch.value}`);
    categorySearch.value = "";
  } else {
    alert("Veuillez saisir une catégorie.");
  }
};
</script>
<template>
  <section>
    <div class="form-container">
    <div class="section">
      <h3 class="title">Visibilité</h3>
      <label class="visible">
        <input type="checkbox" v-model="visibility" />
       <span class="store">Boutique en ligne</span>
      </label>
    </div>
    <div class="section">
      <h3>Détails de stockage</h3>
      <label>
        SKU :
        <input type="text" v-model="sku" placeholder="Saisir le SKU" />
      </label>
      <label>
        Code de barre :
        <input type="text" v-model="barcode" placeholder="Saisir le code de barre" />
      </label>
      <label>
        Poids (kg) :
        <input type="number" v-model="weight" placeholder="Saisir le poids" />
      </label>
    </div>
    <div class="section">
      <h3 class="title">Inventaire</h3>
      <label class="visible">
        <input type="checkbox" v-model="trackInventory" />
       <sapn class="store">Suivre l'inventaire</sapn>
      </label>
    </div>
    <div class="section">
      <h3>Catégorie</h3>
      <label>
        Rechercher une catégorie :
        <input type="text" v-model="categorySearch" placeholder="Rechercher une catégorie" />
      </label>
      <p @click="addCategory"><box-icon name='plus-circle' class="box"></box-icon> <span class="catégorie">Ajouter une catégorie</span></p>
    </div>
    <div class="section">
      <h3>Vendeurs</h3>
      <label>
        <input type="text" v-model="tags" placeholder="tags (séparer par des virgules)" />
      </label>
      <p @click="addCategory"><box-icon name='plus-circle' class="box"></box-icon> <span class="catégorie">Ajouter une catégorie</span></p>
    </div>
  </div>
  </section>
</template>

<style scoped>
.form-container {
  max-width: 500px;
  margin: 20px auto;
  font-family: Arial, sans-serif;
  padding: 20px;
  border: 1px solid #ddd;
  border-radius: 8px;
  background-color: #f9f9f9;
  position: absolute;
  left: 80%;
  top: 56%;
}
.catégorie {
  position: relative;
  bottom: 7px;
}
.title {
  position: relative;
  top: 15px;
}
.box {
  background-color: #007bff;
}
.visible input {
  position: relative;
  right: 107px;
  top: 18px;
}
.store {
  position: relative;
  left: 28px;
}
.section {
  margin-bottom: 20px;
}
section {
  display: flex;
}
h3 {
  margin-bottom: 10px;
}

label {
  display: block;
  margin-bottom: 10px;
}

input {
  width: 100%;
  padding: 8px;
  margin-top: 5px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

p {
  /* padding: 8px 16px; */
  /* background-color: #007bff; */
  color: #007bff;
  cursor: pointer;
}

</style>
