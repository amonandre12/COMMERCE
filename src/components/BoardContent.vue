<script setup>
import { useLayoutStore } from '@/stores/layout';
// Utilisation du store Pinia
const layout = useLayoutStore ()
</script>
<template>
    <section>
  <div :class="['container', layout.layoutDirection]">
  <div class="content">
 <div class="box">
  <h4>Total Revenues</h4><br>
  <p>DA45,2310.89</p>
  <p class="color">+20.1%</p>
 </div>
 <div class="box">
  <h4>Total de vesiteurs</h4>
  <span>2350</span><box-icon name='user-check'></box-icon><br>
  <p>impressions,<a href="">voir le rapport</a></p>
 </div>
 <div class="box">
  <h4>Commandes</h4> <box-icon name='cart-alt'></box-icon><br>
  <span>+2234</span>
  <a href="">voir le rapport</a>
 </div>
<div class="box">
  <h4>Taux de vente moyen</h4><br>
  <span>DA4500</span><br>
  <a href="">voir le rapport</a>
</div>
  </div>
  </div>
  </section>
</template>

<style scoped>
.content{
  display: flex;
  flex-direction: row;
  gap: 70px;
  background-color: #f8f8f8;
  padding: 15px;
  border-bottom: 1px solid #ccc;
}
a {
  color: #ccc;
}
.color {
  color: green;
}
.box {
  background-color: #ffffff;
  border: 1px solid #ccc;
  border-radius: 5px;
  padding: 23px 18px ;
  font-size: 16px;
  /* color: #ccc;  */
  cursor: pointer;
  transition: background-color 0.3s, color 0.3s;
}
box-icon{
  position: relative;
  left: 63%;
  bottom: 42px;
}
section {
  position: absolute;
  top: 70%;
  left: 27%;
}

</style>
