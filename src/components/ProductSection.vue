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
    #
  </label>
</div>
  </div>
<div>
  Produit
</div>
<div class="status">
  Status <span><box-icon name='expand-vertical' class="expand-vertical"></box-icon></span>
</div>
<div>
  Inventaire
</div>
<div>
Catégorie
</div>
<div>
  Prix
</div>
<div>
  Vendeur
</div>
<div>
  <box-icon name='dots-horizontal-rounded'></box-icon>
</div>
 </div>
  </section>
</template>

<style lang="css" scoped>
.container.row {
  display: flex;
  flex-direction: row;
  gap:70px;
  position: absolute;
  left:29%;
  top: 96%;
}
.status {
  position: relative;
  bottom: 10px;
}
span {
  position: relative;
  top: 7px;
  left: 6px;
}
section {
  display: flex;
}

</style>
