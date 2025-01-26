<script setup>

</script>
<template>
  <section>
  <div class="container">
    <div class="mb-3">
  <label for="exampleFormControlInput1" class="form-label">Nom</label> <br>
  <input type="name" class="form-control" id="exampleFormControlInput1" placeholder="Nom ex:chemise d'été bleu...">
  </div>
  <div class="label-group">
    <label for="productName">Slug</label> <br>
    <input type="text" v-model="pronductName" placeholder="https://topvetementdz.store/products/"/>
    <input type="text" id="productSlug" :value="slug" readonly placeholder="slug" class="first-input"/>
  </div>
<div class="mb-4">
  <!-- <label for="exampleFormControlTextarea1" class="form-label">Example textarea</label> -->
  <textarea class="form-control" id="exampleFormControlTextarea1" rows="3" placeholder="écriez quelque chose..."></textarea>
  </div>
  </div>
  </section>
</template>

<style lang="css" scoped>
section {
  display: flex;
  position:relative;
  top:260px;
}
.mb-4 {
  position:relative;
  top:130px;
  padding: 2px;
  border-radius: 8px;
  background-color: #f9f9f9;
}
textarea {
  width:680px;
  height:175px;
  border-radius: 4px;
  border: 1px solid #ccc;
  padding: 10px;
  font-size: 14px;
  resize: none;
  position: relative;
  top: 50px;
}
.label-group {
  position:relative;
  top:30px;
}
.label-group input {
  width:200px;
  height:20px;
  padding:5px;
}
input.first-input {
 position:relative;
 left:30px;
 width:444px;
}
.container {
 position:absolute;
 left:338px;
 top:50%;
 padding: 2px;
  /* border-radius: 8px; */
  background-color: #f9f9f9;
}
.mb-3 input {
  width:690px;
  border:1px solide #ccc;
  height:20px;
  padding:5px;
}
</style>
