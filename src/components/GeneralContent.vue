<script setup>
import { useLayoutStore } from '@/stores/layout';
// Utilisation du store Pinia
const layout = useLayoutStore ()
</script>

<template>
  <section>
  <div :class="['container', layout.layoutDirection]">
<div class="general">
  Géneral 
</div>
<div class="paiement">
  Paiement
</div>
<div class="Livraison">
  Livraison
</div>
<div class="Role">
  Utilisateurs & Rôles
</div>
<div class="Local">
  Localisation
</div>
<div class="Taxes">
  Les Taxes 
</div>
<div class="affiliation">
  Programme d'affiliation
</div>
  </div>
  </section>
</template>

<style lang="css" scoped>
section {
  display: flex;
}
.general {
  position: relative;
  top: 25px;
  font-size: 1.5em;
  cursor: pointer;
  padding: 8px;
  border-radius: 10px;
}
.general:hover {
 background-color: #B6D8F2;
}
.paiement {
  position: relative;
  top: 45px;
  font-size: 1.5em;
  cursor: pointer;
  padding: 8px;
  border-radius: 10px;
}

.paiement:hover {
 background-color: #B6D8F2;
}
.Livraison {
  position: relative;
  top: 64px;
  font-size: 1.5em;
  cursor: pointer;
  padding: 8px;
  border-radius: 10px;
}

.Livraison:hover {
 background-color: #B6D8F2;
}
.Role {
  position: relative;
  top: 88px;
  font-size: 1.5em;
  cursor: pointer;
  padding: 8px;
  border-radius: 10px;
}

.Role:hover {
 background-color: #B6D8F2;
}
.affiliation {
  position: relative;
  top: 149px;
  font-size: 1.5em;
  cursor: pointer;
  padding: 8px;
  border-radius: 10px;
}

.affiliation:hover {
 background-color: #B6D8F2;
}
.Local {
  position: relative;
  top: 110px;
  font-size: 1.5em;
  cursor: pointer;
  display: flex;
  padding: 8px;
  border-radius: 10px;
}

.Local:hover {
 background-color: #B6D8F2;
}
.Taxes {
  position: relative;
  top: 130px;
  font-size: 1.5em;
  cursor: pointer;
  padding: 8px;
  border-radius: 10px;
}
.Taxes:hover {
 background-color: #B6D8F2;
}
.container {
  position: absolute;
  left: 30%;
  top: 50%;
  padding-bottom: 150px;
  border: 1px solid #ddd;
  border-radius: 8px;
  background-color: #f9f9f9;
}
</style>