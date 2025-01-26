<script setup>
import { useLayoutStore } from '@/stores/layout';
// Utilisation du store Pinia
const layout = useLayoutStore ()
</script>
<template>
  <section>
  <div :class="['container', layout.layoutDirection]">
    <div class="form-check">
      <input class="form-check-input" type="checkbox" value="" id="defaultCheck1">
  <label class="form-check-label" for="defaultCheck1">
    <a href="">#324-325<br><span>youcan</span></a>
  </label>
  </div>
  <div class="box-date">
   <span>28-03-2024<br>16:09:32</span>
  </div>
  <div class="box-icon">
   <p> <box-icon name='power-off' class="box"></box-icon><span>pas confirmé</span></p> 
  </div>
  <div class="box-lang">
  <p>Sweet (youcan),draria<br>1653,16 aiger ديواني <br>الخط العربي جميل.</p>
  </div>
  <div class="transfer">
    <box-icon name='transfer'></box-icon>
  </div>
  <div class="paiement">
    <p>paiement a<br> la livraison</p>
  </div>
  <div class="number">
    <span>6200DA</span>
  </div>
  <div>
    <p class="direct">Direct</p>
  </div>
  <div class="rounded">
    <box-icon name='dots-horizontal-rounded'></box-icon>
  </div>
  </div>
  </section>  
</template>

<style scoped>
.container.row{
  display: flex;
  flex-direction: row;
  position: absolute;
  left: 29%;
  top: 147%; 
  gap: 34px;
}

section :hover {
  background-color: #adb5bd;
}
.form-check a {
  position: relative;
  left: 3px;
  bottom: 10px;
}
.form-check span  {
  position: relative;
  left: 18px;
}
.transfer {
  position: relative;
  left: 14px;
  top:25px;
}
.box-icon p {
  position: relative;
  bottom: 38px;
}

.box-icon {
  position: relative;
  top: 47px;
  margin-bottom: 20px;
  right:27px;
}
.box-icon p {
  background-color:#FBBFB8; 
   border-radius:40px;
   padding:2px;
}
.box-icon span {
  position: relative;
  bottom: 4px;
}
.box-icon box-icon {
  position: relative;
  top:3px;
}
.box-date {
  position: relative;
  right: 15px;
  top: 22px;
 
}
.paiement {
  position: relative;
  top: 6px;
  left: 54px;
}
.box-lang {
  position: relative;
  top: 4px;
  left: 2px;
}
.rounded {
  position: relative;
  left: 50px;
  top: 25px;
}
.number span {
  position: relative;
  left:74px;
  top: 26px;
}
.direct {
  position: relative;
  left: 60px;
  top: 10px;
}
section {
  display:flex;
  cursor: pointer;
}
.form-check-input {
  position: relative;
  top: 16px;
}
a {
  color: #333;
  font-size: 1.3em;
  position: relative;
  top: 10px;
}
</style>
