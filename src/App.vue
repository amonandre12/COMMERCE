<script setup>
// import { RouterLink, RouterView } from 'vue-router'
import LinksGroup from './components/LinksGroup.vue'
import BarContent from '@/components/BarContent.vue'
import BoardContent from '@/components/BoardContent.vue'
import BarChart from '@/components/BarChart.vue'
import SectionBar from '@/components/SectionBar.vue'
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
   <LinksGroup/>
   <BarContent title="Tableau de bord"/>
   <BoardContent/>
   <BarChart/>
   <SectionBar/>
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
box-icon {
  position:relative;
  top: 15px;
}
em {
  font-size: 1.7em;
  position: relative;
  bottom: 5px;
  right: 50%;
}
</style>
