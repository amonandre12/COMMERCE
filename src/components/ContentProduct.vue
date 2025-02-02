<script setup>
import { useLayoutStore } from '@/stores/layout';
// Utilisation du store Pinia
const layout = useLayoutStore ()
</script>

<template>
  <section>
 <div :class="['container', layout.layoutDirection]">
  <div>
    <div class="form-check">
  <input class="form-check-input" type="checkbox" value="" id="defaultCheck1">
  <label class="form-check-label" for="defaultCheck1">
  </label>
</div>
  </div>
<div class="shirt">
  Costume avec <br> Chemise Blanc c...
</div>
<div class="box-icon">
  <p><box-icon name='badge-check' class="box"></box-icon> <span> Active</span></p>
</div>
<div class="variantes">
  50 en stock
</div>
<div class="lang">
 الخط العربي جميل
</div>
<div class="number">
  <span>4800DA</span>
</div>
<div class="personal">
  Amir sourl
</div>
<div class="rounded">
  <box-icon name='dots-horizontal-rounded'></box-icon>
</div>
 </div>
  </section>
</template>

<style lang="css" scoped>
.container.row {
  display: flex;
  flex-direction: row;
  gap:49.6px;
  position: absolute;
  left:29%;
  top:144%;
}
.rounded {
  position: relative;
  top: 14px;
}
.variantes {
  position: relative;
  top: 14px;
  right: 10px;
}
.form-check {
  position: relative;
  top: 16px;
}
.personal {
  position: relative;
  right: 10px;
  top: 16px;
}

.box-icon p {
  background-color:#9FCDA8;
   border-radius:50px;
   position: relative;
   right: 10px;
}
section :hover {
  background-color: #adb5bd;
}
.lang {
  position: relative;
  left: 6px;
  top: 16px;
}
.shirt {
  position: relative;
  left: 10px;
  top: 10px;
}
.number {
  position: relative;
  top: 16px;
  right: 4px;
}
.box-icon {
  position: relative;
   bottom: 13px;
   right: 17px;
   top: 2px;
}
.box-icon span {
  position: relative;
 bottom: 5px;
}
section {
  display: flex;
  cursor: pointer;
}
</style>
