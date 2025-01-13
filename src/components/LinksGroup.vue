<script setup>
import { useLayoutStore } from '@/stores/layout';
// Utilisation du store Pinia
const layout = useLayoutStore ()
// import BarContent from '@/components/BarContent.vue'
</script>

<template>
  <section>
  <div>
    <div :class="['container', layout.layoutDirection]">
      <div class="content">
   <div class="box">
 <div>
  <img src="@/assets/photo.jpg" alt="the photo">
 </div>
 <div>
  <p>Amir sourl(admin)</p>
 </div>
 <div>
  <box-icon name='expand-vertical'></box-icon>
 </div>
     </div>
 <div>
  <box-icon name='qr'></box-icon>
<a href="">tableau de bord</a>
 </div>
 <div>
  <box-icon name='cart'></box-icon>
  <a href="">Commandes</a>
 </div>
 <div>
  <box-icon name='cube'></box-icon>
  <a href="">Produits</a>
 </div>
 <div class="emballage">
  <box-icon type='solid' name='gift'></box-icon>
  <a href="">Emballages</a> <span class="number-color">23</span>
 </div>
 <div>
  <box-icon name='font-size'></box-icon>
  <a href="">Upsells</a> <span>23</span>
 </div>
 <div>
  <box-icon name='user'></box-icon>
  <a href="">clients</a> <span>23</span>
 </div>
 <div>
  <box-icon name='trending-up'></box-icon>
  <a href="">Rapports & Analyses</a>
 </div>
 <div>
  <box-icon name='notepad'></box-icon>
  <a href="">Coupons</a> <span>23</span>
 </div>
     </div>
     <div class="market-class">
 <div>
  <box-icon type='solid' name='group'></box-icon>
  <a href="">Marketing</a>  <span>342</span>
 </div>
 <div>
  <box-icon name='shape-triangle'></box-icon>
  <a href="">Integration</a>
 </div>
 <div>
  <box-icon name='cog'></box-icon>
  <a href="">Reglages</a> <span>128</span>
 </div>
 <div>
  <box-icon type='solid' name='copy-alt'></box-icon>
  <a href="">Supports</a> <span>8</span>
 </div>
 <div>
  <box-icon name='user-x'></box-icon>
  <a href="">Deconnecter</a>
 </div>
     </div>
    </div>
  </div>
  </section>
  <!-- <BarContent  title="Tableau de bord"/> -->
</template>

<style scoped>

img {
  border-radius:50%;
  width: 40px;
  height: 40px;
}
section {
display: flex;
position: relative;
right: 20px;
top: 30px;
}
.content {
  width: 296px;
  height: 402px;
  position: relative;
  top: 52px;
  border-right: 1px;
  border-bottom: 1px;
  padding: 16px 16px 10px 10px;
  gap: 24px;
}
.market-class {
  width: 296px;
  height: 240px;
  position: relative;
  top: 455px;
  border-right: 1px;
  justify-content:space-between ;
  padding: 10px;
}
.container {
  position: absolute;
  left: 5%;
  top:15%;
}
.box {
  display: flex;
  flex-direction: row;
  gap: 20px;
  background-color: #ffffff;
  border: 1px solid #ccc;
  padding: 1px ;
  /* color: #ccc;  */
  cursor: pointer;
  transition: background-color 0.3s, color 0.3s;
}
a {
  text-decoration: none;
  font-size: 1.3em;
  color: #333;
  position: relative;
  bottom: 5.2px;
}
box-icon  {
margin: 15px;
}
span {
  position: relative;
  bottom: 4px;
  left: 30px;
}
.number-color {
  background-color: #333;
  color: white;
  cursor: pointer;
}
</style>
