<script setup>
import {ref} from 'vue'
const title = ref("Géneral")
import GenralContent from '@/components/GeneralContent.vue'
import ProfilContent from '@/components/ProfilContent.vue'
</script>

<template>
   <section>
   <div class="container">
    <div class="breadcrumb">
    <span>Réglages</span>
    <span class="symbole">&gt;</span>
    <span>Géneral</span>
    </div>
    <h1>{{title}}</h1>
  </div>
  </section>
  <GenralContent/>
  <ProfilContent/>
</template>

<style lang="css" scoped>
.container {
  position: absolute;
  left: 30%;
  top: 156px;
}
section {
  display: flex;
}
h1 {
  font-size:2.4em;
  position:relative;
  top: 38px;
}

.breadcrumb {
  color: #666;
  text-decoration: underline;
  cursor: pointer;
}
.breadcrumb span {
  font-size: 1.2em;
}
.symbole{
position: relative;
top: 2px;
}
span {
  font-size: 1.6em;
}
</style>
