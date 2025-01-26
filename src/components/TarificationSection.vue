<script setup>

</script>
<template>
    <section>
    <div class="container">
    <div>
    <div class="mb-1">
   <label for="exampleFormControlInput1" class="form-label">Tarification</label> <br>
   <input type="name" class="form-control" id="exampleFormControlInput1" placeholder="Prix">
    </div>
 </div>
 <div>
    <div class="mb-2">
  <!-- <label for="exampleFormControlInput1" class="form-label">Nom</label> <br> -->
  <input type="name" class="form-control" id="exampleFormControlInput1" placeholder="Comparer aux prix">
  </div>
</div>
<div>
 <div class="mb-3">
  <!-- <label for="exampleFormControlInput1" class="form-label">Nom</label> <br> -->
  <input type="name" class="form-control" id="exampleFormControlInput1" placeholder="Prix de revient">
  </div>
</div>
</div>
</section>
</template>

<style scoped>
section {
    display:flex;
}
input {
    height:20px;
    padding:5px;
}
.mb-1 {
    position:relative;
    bottom:19px;
}
.container {
    position:absolute;
    left:30%;
    top:190%;
    display:flex;
    flex-direction:row;
    gap:40px;
}
</style>