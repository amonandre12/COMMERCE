<script setup>

</script>

<template>
    <section>
    <div  class="container">
  <div>
    <div class="mb-1">
   <label for="exampleFormControlInput1" class="form-label">images</label> <br>
   <input type="name" class="form-control" id="exampleFormControlInput1" placeholder="Remarque">
    </div>
 </div>
 <div class="button-container">
    <div>
    <button class="costum-button">télecharger des images</button>
    <button class="btn">ajouter un lien vidéo</button>
 </div>
</div>
    </div>
</section>
</template>

<style scoped>
section {
    display:flex;
}
.container {
    position:absolute;
    left:30%;
    top:199%;
    display:flex;
    gap:49px;
}
.mb-1 {
    position:relative;
    top:5px;
}
.mb-1 input {
    width:200px;
  height:20px;
  padding:5px;
}
.button-container {
    display:flex;
    gap:20px;
    margin-top:20px;
}
.costum-button {
 background-color:#212E53;
 color:white;
 border:none;
 border-radius:5px;
 padding:10px 20px ;
 font-size:14px;
 cursor:pointer;
 transition:background-color 0.3s;
}
.costum-button:hover {
    background-color:#1c7cd6;
}
.btn {
 background-color:#212E53;
 color:white;
 border:none;
 border-radius:5px;
 padding:10px 20px ;
 font-size:14px;
 cursor:pointer;
 transition:background-color 0.3s;
 position:relative;
 left:20px;
}
.btn:hover {
    background-color:#1c7cd6;
}
</style>
