<script setup>

</script>

<template>
  <section>
  <div class="navbar">
      <button class="nav-btn-active">Tous</button>
      <button class="nav-button">Rupture de stock</button>
      <button class="nav-button">Active</button>
      <button class="nav-button">brouillon</button>
      <button class="nav-button">Archivé</button>
    </div>
  </section>
</template>

<style scoped>
section {
  display: flex;
}
.navbar {
  display: flex;
  gap: 35px;
  background-color: #f8f8f8;
  padding: 10px;
  border-bottom: 1px solid #ccc;
  position: absolute;
  left: 29%;
  bottom: 13%;
 }

.nav-button {
  /* background-color: #ffffff; */
  border: 1px solid #ccc;
  border-radius: 5px;
  padding: 8px 16px ;
  font-size: 16px;
  /* color: #ccc; */
  cursor: pointer;
  transition: background-color 0.3s, color 0.3s;
  font-size: 1.2em;
}
.nav-button:hover {
 background-color: #333;
 color: white;
}
.nav-btn-active {
  background-color: #333;
  color: #ccc;
  font-size: 1.2em;
  cursor: pointer;
}
.nav-btn-active:hover {
  color: #ccc ;

}
</style>
