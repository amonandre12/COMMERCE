<script setup>
defineProps({
  title:String
});
// import BoardContent from '@/components/BoardContent.vue'
</script>
<template>
  <section>
   <div class="btn-group">
  <div>
<h1>{{ title }}</h1>
  </div>
  <div class="navbar">
      <button class="nav-btn-active">Aperçu</button>
      <button class="nav-button">Analytics</button>
      <button class="nav-button">Reports</button>
      <button class="nav-button">Notifications</button>
    </div>
    </div>
    <div class="btn-smell">
    <button type="button" class="btn" ><box-icon name='calendar'></box-icon>Jan 20, 2024-Avr 9, 2024 </button>
    <button type="button" class="dark">Export</button>
    </div>
  </section>
  <!-- <BarChart/> -->
   <!-- <BoardContent/> -->
</template>

<style  scoped>
.btn {
  position: relative;
  right: 55px;
  height: 40px;
  padding-bottom: 10px;
}
box-icon {
  position: relative;
  top:5px;
  right: 5px;
}
.dark {
  position: relative;
  right: 35px;
  top: -3px;
  background-color: #333F;
  color: #ccc;
  padding: 10px 10px;
  cursor: pointer;
  bottom: 37px;
}
.dark:hover {
  color: white;
  transition: background-color 0.3s, color 0.3s;
}
.btn-smell {
  position: relative;
  top: 215px;
  left: 1078px;
}
.nav-btn-active {
  background-color: blue;
  color: #ccc;
  cursor: pointer;
}
.navbar {
  display: flex;
  gap: 10px;
  background-color: #f8f8f8;
  padding: 10px;
  border-bottom: 1px solid #ccc;
  position: relative;
  right: 62px;
}
.nav-button {
  background-color: #ffffff;
  border: 1px solid #ccc;
  border-radius: 5px;
  padding: 8px 16px ;
  font-size: 16px;
  color: #ccc;
  cursor: pointer;
  transition: background-color 0.3s, color 0.3s;
}

.nav-button.active {
background-color: #5a4fe4 !important;
color: #ffffff !important;
}
.nav-button:hover {
  background-color: #e5e5e5;
}
section {
  display: flex;
}
.btn-group {
  position: absolute;
  left: 32%;
  top: 30%;
}
h1 {
  font-size:2.2em ;
  position: relative;
  right: 55px;
}
</style>


