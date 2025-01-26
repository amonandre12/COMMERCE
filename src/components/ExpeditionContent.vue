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
  <p>  <box-icon name='power-off' class="box"></box-icon> <span> expédiées</span></p>
  </div>
  <div class="box-lang">
  <p>Sweet (youcan),draria<br>1653,16 aiger ديواني <br>الخط العربي جميل.</p>
  </div>
  <div class="transfer">
    <a href="">YAL-<br>ZARK83</a>
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
  top: 173%;
  gap: 33px;
}

.box-icon span {
  position: relative;
  bottom: 6px;
}
.form-check-input {
  position: relative;
  top: 16px;
}
.box-icon p {
  background-color:#adb5bd;
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
  left: 24px;
  top:12px;
}
.box-icon {
  position: relative;
  top: 10px;
  right: 18px;
  margin-bottom: 20px;
}
.box-icon p {
   background-color:#d1ddf5 ; 
   border-radius:40px;
   padding:1px;
}
.box-icon box-icon {
  position: relative;
  left:4px;
}
.box-date {
  position: relative;
  right: 15px;
  top: 22px;
}
.paiement {
  position: relative;
  top: 5px;
  left: 19px;
}
.box-lang {
  position: relative;
  top: 5px;
  left: 25px;
}
.rounded {
  position: relative;
  left: 22px;
  top: 24px;
}
.number span {
  position: relative;
  left:44px;
  top: 27px;
}
.direct {
  position: relative;
  left: 33px;
  top: 10px;
}
section {
  display:flex;
  cursor: pointer;
}
section :hover {
  background-color: #adb5bd;
}

a {
  color: #333;
  font-size: 1.3em;
  position: relative;
  top: 10px;
}
</style>
