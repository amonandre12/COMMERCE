<script setup>
import { RouterLink, RouterView } from 'vue-router'
import { useLayoutStore } from '@/stores/layout';
// Utilisation du store Pinia
const layout = useLayoutStore ()

</script>

<template>
  <header>
    <div class="nav-header">
     <div>
        <p><em>admin panel</em></p>
     </div>
    <div class="container-fluid">
    <form class="d-flex" role="search">
      <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
    </form>
  </div>
  <div class="img-class">
    <div>
    <box-icon name='wink-smile'></box-icon>
    </div>
    <div>
    <img src="@/assets/photo.jpg" alt="the photo">
    </div>
    <div>
    <p>Amir sourl(admin)</p>
    </div>
  </div>
    </div>
  </header>
  <header>
    <div class="section">
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
  <box-icon name='expand-vertical' class="expand-vertical"></box-icon>
 </div>
   </div>
 <div class="board">
  <router-link to="/"> <box-icon name='qr'></box-icon>tableau de bord</router-link>
 </div>
 <div class="command">
  <router-link to="/CommandView"> <box-icon name='cart'></box-icon>Commandes</router-link>
 </div>
 <div class="product">
  <router-link to="/ProductView"> <box-icon name='cube'></box-icon>Produits</router-link>
 </div>
 <div class="emballage">
  <router-link> <box-icon type='solid' name='gift'></box-icon> Emballages </router-link>  
  <div>
    <p class="number">23</p>
  </div>
 </div>
 <div class="upsells">
  <router-link>  <box-icon name='font-size'></box-icon>Upsells </router-link>  
  <div>
    <p class="number">23</p>
  </div>
 </div>
 <div class="client">
  <router-link> <box-icon name='user'></box-icon>clients </router-link> 
  <div>
    <p class="number">23</p>
  </div> 
 </div>
 <div class="rapport">
  <router-link> <box-icon name='trending-up'></box-icon>Rapports & Analyses</router-link>
 </div>
 <div class="coupon">
  <router-link>  <box-icon name='notepad'></box-icon>Coupons </router-link> 
  <div>
    <p class="number">23</p>
  </div>
 </div>
     </div>
     <div class="market-class">
 <div class="market">
  <router-link> <box-icon type='solid' name='group'></box-icon>Marketing </router-link>  
  <div>
    <p class="number">342</p>
  </div>
 </div>
 <div class="integration">
  <router-link> <box-icon name='shape-triangle'></box-icon>Integration</router-link>
 </div>
 <div class="setting">
  <router-link to="/SettingView"> <box-icon name='cog'></box-icon>Reglages</router-link>  
  <div>
    <p class="number">128</p>
  </div>
 </div>
 <div class="support">
  <router-link> <box-icon name='bookmarks'></box-icon>Support</router-link>
 </div>
 <div class="deconnect">
  <router-link> <box-icon name='user-x'></box-icon>Deconnecter</router-link>
 </div>
     </div>
    </div>
    <router-view></router-view>
  </div>
  </header> 
</template>

<style scoped>

.nav-header{
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  text-align: center;
  width: 1440px;
  height: 52px;
  background-color: #f8f8f8;
  padding: 10px;
  border-bottom: 1px solid #ccc;
}
.section {
  display: flex;
}
.number {
  position: relative;
  left: 11px;
  background-color: #333;
  color: #ccc;
  padding:5px;
  border-radius:10px;
}
.expand-vertical {
  margin-top: -2px;
  position: relative;
  top: 18px;
}
img {
  border-radius:50%;
  width: 50px;
  height: 50px;
}
.img-class {
display: flex;
gap: 40px;
position: relative;
top: 6px;
left: 50px;
}
.container-fluid {
  position: relative;
  top: 10px;
  left: 50px;
}
input {
width: 440px;
height: 40px;
border-radius: 5px;
}

em {
  font-size: 1.7em;
  position: relative;
  bottom: 5px;
  right: 50%;
}
img {
  border-radius:50%;
  width: 40px;
  height: 40px;
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
  top: 195px;
  border-right: 1px;
  justify-content:space-between ;
  padding: 10px;
}
.container {
  position: absolute;
  top:25%;
  /* padding: 20px; */
  border: 1px solid #ddd;
  border-radius: 8px;
  background-color: #f9f9f9;
  padding-bottom: 400px;
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
  position: relative;
  bottom:60px
}
a{
  text-decoration: none;
  font-size: 1.5em;
  position: relative;
  top: 8px;
  transition: all 0.3s ease;
}
.upsells a {
  padding: 8px;
  border-radius: 5px;
  height: 20px;
  color: black;
  display: inline-flex;
  align-items: center;
  justify-items: center;
}
.upsells {
  display: flex;
  gap: 100px;
  background-color: transparent;
  padding: 1px;
  border-radius: 25px;
  height: 50px;
  width: 310px;
  cursor: pointer;
}
.upsells:hover {
  background-color: #333;
}
.upsells:hover a {
  color: white;
}
.market {
  display: flex;
  gap: 67px;
  background-color: transparent;
  padding: 1px;
  border-radius: 25px;
  height: 50px;
  width: 310px;
  cursor: pointer;
}
.market:hover {
  background-color: #333;
}
.market:hover a {
  color: white;
}

.coupon:hover {
  background-color: #333;
}

.coupon:hover a{
  color: white;
}
.coupon {
  display: flex;
  gap: 85px;
  background-color: transparent;
  padding: 1px;
  border-radius: 25px;
  height: 50px;
  width: 310px;
  cursor: pointer;
}
.client:hover {
  background-color: #333;
}
.client:hover a {
  color: white;
}
.client {
  display: flex;
  gap: 107px;
  background-color: transparent;
  padding: 1px;
  border-radius: 25px;
  height: 50px;
  width: 310px;
  cursor: pointer;
}
.support a {
  padding: 8px;
  border-radius: 5px;
  height: 20px;
  color: black;
  display: inline-flex;
  align-items: center;
  justify-items: center;
}
.deconnect a {
  padding: 8px;
  border-radius: 5px;
  height: 20px;
  color: black;
  display: inline-flex;
  align-items: center;
}
.deconnect {
  position: relative;
  top: 50px;
}
 .deconnect {
  background-color: transparent;
  padding: 1px;
  border-radius: 25px;
  height: 50px;
  width: 310px;
  cursor: pointer;
}
.deconnect:hover a{
  color: white;
}

.deconnect:hover{
  background-color: #333;
}
.support:hover a{
  color: white;
}

.support:hover {
  background-color: #333;
}
 .support {
  background-color: transparent;
  padding: 1px;
  border-radius: 25px;
  height: 50px;
  width: 310px;
  cursor: pointer;
}
.market a {
  padding: 8px;
  border-radius: 5px;
  height: 20px;
  color: black;
  display: inline-flex;
  align-items: center;
}

.setting {
  display: flex;
  gap: 78px;
  background-color: transparent;
  padding: 1px;
  border-radius: 25px;
  height: 50px;
  width: 310px;
  cursor: pointer;
}
.setting a {
  color: black;
  display: inline-flex;
  align-items: center;
  position: relative;
  top: -2px;
}
.setting:hover a{
  color: white;
}

.setting:hover {
  background-color: #333;
}
.integration a {
  padding: 8px;
  border-radius: 5px;
  height: 20px;
  color: black;
  display: inline-flex;
  align-items: center;
}
.integration {
  background-color: transparent;
  padding: 1px;
  border-radius: 25px;
  height: 50px;
  width: 310px;
  cursor: pointer;
}
.integration:hover a {
  color: white;
}

.integration:hover {
  background-color: #333;
}
.market:hover a{
  color: white;
}
.coupon a {
  padding: 8px;
  border-radius: 5px;
  height: 20px;
  color: black;
  display: inline-flex;
  align-items: center;
  justify-items: center;
}
.coupon a:hover {
  background-color: #333;
  color: white;
}
.rapport a {
  padding: 8px;
  border-radius: 5px;
  height: 20px;
  color: black;
  display: inline-flex;
  align-items: center;
}
.rapport {
  background-color: transparent;
  padding: 1px;
  border-radius: 25px;
  height: 50px;
  width: 310px;
  cursor: pointer;
}
.rapport:hover a{
  color: white;
}

.rapport:hover {
  background-color: #333;
}
.client a {
  padding: 8px;
  border-radius: 5px;
  height: 20px;
  color: black;
  display: inline-flex;
  align-items: center;
}
.client a:hover {
  background-color: #333;
  color: white;
}
.upsells a:hover {
  background-color: #333;
  color: white;
}
.board a{
  padding: 8px;
  border-radius: 5px;
  height: 20px;
  color: black;
  display: inline-flex;
  align-items: center;
}
.board {
  background-color: transparent;
  padding: 1px;
  border-radius: 25px;
  height: 50px;
  width: 310px;
  cursor: pointer;
}

.board:hover a{
  color: white;
}

.board:hover {
  background-color: #333;
}
.emballage a {
  padding: 8px;
  border-radius: 5px;
  height: 20px;
  color: black;
  display: inline-flex;
  align-items: center;
}
.emballage:hover a{
  color: white;
}

.emballage:hover {
  background-color: #333;
}
.emballage {
  display: flex;
  gap: 63px;
  background-color: transparent;
  padding: 1px;
  border-radius: 25px;
  height: 50px;
  width: 310px;
  cursor: pointer;
}
.product a {
  padding: 8px;
  border-radius: 5px;
  height: 20px;
  color: black;
  display: inline-flex;
  align-items: center;
}
.product {
  background-color: transparent;
  padding: 1px;
  border-radius: 25px;
  height: 50px;
  width: 310px;
  cursor: pointer;
}
.product:hover a{
  color: white;
}

.product:hover{
  background-color: #333;
}
.command a {
  padding: 8px;
  border-radius: 5px;
  height: 20px;
  color: black;
  display: inline-flex;
  align-items: center;
}
 .command {
  background-color: transparent;
  padding: 1px;
  border-radius: 25px;
  height: 50px;
  width: 310px;
  cursor: pointer;
}
.command:hover{
  background-color: #333;
}
.command:hover a{
  color: white;
}
.board:hover a{
  background-color: #333;
  color: white;
}
box-icon  {
margin: 15px;
}
span {
  position: relative;
  top: 10px;
  left: 30px;
}

</style>
