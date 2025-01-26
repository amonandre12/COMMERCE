<script setup>
import '@vueup/vue-quill/dist/vue-quill.snow.css';
</script>

<template>
  <section>
  <QuillEditor toolbar="#my-toolbar" v-model="Description"
  class="quill-editor"
  :modules="modules"
   theme="snow">  
    <template #toolbar>
      <div id="my-toolbar">
        <h3>Description</h3>
        <button class="ql-undo" title="Annuler">
            <box-icon name='undo'></box-icon>
          </button>
          <button class="ql-redo" title="Rétablir">
            <box-icon name='redo'></box-icon>
          </button>
        <select class="ql-header" title="Taille du texte">
            <option value="1">Titre 1</option>
            <option value="2">Titre 2</option>
            <option selected>Normal text</option>
          </select>
          <select class="ql-align" title="Alignement du texte"> 
            <option selected></option>
            <option value="center"></option>
            <option value="right"></option>
            <option value="justify"></option>
          </select>  <box-icon name='chevron-down' class="box"></box-icon>
          <select class="ql-color" title="Couleur du texte" ></select><box-icon name='chevron-down' class="icon"></box-icon>
        <button class="ql-bold"></button>
        <button class="ql-italic"></button>
        <button class="ql-underline" title="Souligné"></button>
        <button class="ql-strike" title="Barré"></button>
        <button class="ql-co"><box-icon name='code'></box-icon></button> 
        <button class="ql-color" title="Couleur du texte">A</button>
        <button class="ql-list" value="ordered" title="Liste numérotée"></button>
        <button class="ql-list" value="bullet" title="Liste à puces"></button>
        <button class="ql-li" ><box-icon name='link'></box-icon></button>
        <button class="ql-image" title="Insérer une image"></button>
        <button class="ql-code-block" title="Bloc de code"></button>
        <button class="ql-blockquote" title="Citation"><box-icon type='solid' name='quote-alt-left'></box-icon></button>
        <button id="insert-dash" @click="insertDash" title="Insérer un tiret">—</button>
        <!-- But you can also add your own -->
        <button id="custom-button"></button>
      </div>
    </template> 
  </QuillEditor>
  </section>
</template>

<style lang="css" scoped>

section {
  display: flex;
}
.ql-li {
  position: relative;
  bottom: 3px;
}
.ql-co {
  position: relative;
  bottom: 3px;
}
.box {
  position: relative;
  right: 466px;
  top: 1px;
  cursor: pointer;
}
button.ql-color {
  font-size: 14px;
  font-weight: bold;
  position: relative;
}
.icon {
  position: relative;
  right: 453px;
  top: 1px;
  cursor: pointer;
}
#my-toolbar {
  position: absolute;
  left: 26%;
  top: 90%;
  gap: 10px;
}
h3 {
  position: absolute;
  bottom: 67%;
}
.ql-color {
  background-color:black;
  color: black;
  border-radius: 3px;
}
</style>
