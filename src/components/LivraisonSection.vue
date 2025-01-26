<script setup>
import { ref } from "vue"
const hidden = ref(false)
const isVisible = () => {
  hidden.value = !hidden.value
}
const hidMenu = () => {
  hidden.value=!hidden.value
}
</script>
<template>
  <section>
  <div class="container">
    <div class="form-check">
  <input class="form-check-input" type="checkbox" value="" id="defaultCheck1">
  <label class="form-check-label" for="defaultCheck1">
    #
  </label>
</div>
 <p class="date"> <span>Date </span><box-icon name='expand-vertical' class="expand-vertical"></box-icon></p> 
 <p class="status"><span>Status </span><box-icon name='expand-vertical' class="expand-vertical"></box-icon></p> 
 <p class="send">Livrée à</p>
 <p class="tracking">Tracking n°</p>
 <p class="paiment">Paiement</p>
 <p class="total" >Total</p>
  <box-icon name='dots-horizontal-rounded' @click.prevent="isVisible" class="box"></box-icon>
 <div class="menu" v-if="hidden">
    <ul>
        <li @click="hidMenu">Voir détails</li>
        <li>Modifier</li>
        <li>Labels<span class="arrow">></span></li>
        <li class="delete">Supprimer <span class="shortcut">⌘ X</span></li>
    </ul>
</div>
  </div>
  </section>
</template>

<style scoped>
.container{
  display: flex;
  gap: 50px;
  position: absolute;
  left:29%;
  top: 90%;
}
.box {
  cursor: pointer;
  position: relative;
  left: 90px;
  top: 20px;
}
.expand-vertical {
  position: relative;
  top: 4px;
}
.menu {
    position:absolute;
    left:105%;
    top:5px;
    background-color: white;
    border: 1px solid #E2EBF0;
    border-radius: 8px;
    width: 170px;
    height:158px;
    max-width: 128px;
    border-radius: 6px;
    border: 1px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    z-index: 1000;
}

.menu ul {
    list-style: none;
    padding: 0;
    margin: 0;
}

.menu li {
    padding: 12px 16px;
    border-bottom: 1px solid #eee;
    color: #333;
    cursor: pointer;
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 16px;
}

.menu li:last-child {
    border-bottom: none;
}

.menu li:hover {
    background-color: #F4CFDF;
}

.menu .delete {
    color: #d9534f;
    font-weight: bold;
}

.menu .shortcut {
    color: #666;
    font-size: 14px;
}

.menu .arrow {
    font-size: 14px;
    color: #999;
}
.total {
  position: relative;
  left: 102px;
}
.details {
  position: relative;
  left: 99px;
}
.paiment {
  position: relative;
  left:89px
}
.form-check {
  position:relative;
  left:3px;
}
.date {
  position:relative;
  left:45px;
  bottom: 8px;
}
.tracking {
  position:relative;
  left:90px;
}
.status {
  position: relative;
  left: 50px;
  bottom: 7px;
}
.send {
  position: relative;
  left: 70px;
}

.deleted {
  position: relative;
  top: 35px;
}

.form-check {
  position: relative;
  top: 20px;
}
.container p {
  font-size: 1.2em;
}
section {
  display: flex;
}
</style>
