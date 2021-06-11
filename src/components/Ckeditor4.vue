<template>
  <div>
    <ckeditor value="Write your story" :config="cke4_config"></ckeditor>
  </div>
</template>

<script>
import Vue from 'vue'
import CKEditor from 'ckeditor4-vue';

Vue.use(CKEditor);

export default {
  name: "Ckeditor4",
  data() {
    return {
      cke4_config: {
        language: 'en',
        uiColor: '#aad5f0',
        toolbarGroups: [
          { name: 'clipboard',   groups: [ 'clipboard', 'undo' ] },
          { name: 'editing',     groups: [ 'find', 'selection', 'spellchecker' ] },
          { name: 'links' },
          { name: 'insert' },
          { name: 'forms' },
          { name: 'tools' },
          { name: 'document',       groups: [ 'mode', 'document', 'doctools' ] },
          { name: 'others' },
          '/',
          { name: 'basicstyles', groups: [ 'basicstyles', 'cleanup' ] },
          { name: 'paragraph',   groups: [ 'list', 'indent', 'blocks', 'align', 'bidi' ] },
          { name: 'styles' },
          { name: 'colors' },
          { name: 'about' }
        ],
        format_tags: 'p;h1;h2;h3;pre',
        removeButtons: 'Underline,Subscript,Superscript',
        removeDialogTabs: 'image:advanced;link:advanced',
        filebrowserImageBrowseUrl: 'http://localhost:8000/filemanager/dialog.php?type=1&editor=ckeditor&fldr=',
        filebrowerImageUploadUrl: 'http://localhost:8000/filemanager/dialog.php?type=1&editor=ckeditor'
      }
    }
  }
}
</script>

<style scoped>
cke_dialog_tab {
  display: none;
}

</style>