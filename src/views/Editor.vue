<template>
  <div>
    <ckeditor value="Write your post" :config="editor_config"></ckeditor>
  </div>
</template>

<script>
import Vue from 'vue'
import CKEditor from 'ckeditor4-vue';

Vue.use(CKEditor);

export default {
  name: "Editor",
  data() {
    return {
      editor_cofig: {
        uiColor: '#AADC6E',
      }
    }
  }
}
</script>

<style>

</style>