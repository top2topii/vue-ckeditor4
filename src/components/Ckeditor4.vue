<template>
  <div>
    <ckeditor value="Write your story"></ckeditor>
  </div>
</template>

<script>
import Vue from 'vue'
import CKEditor from 'ckeditor4-vue';

Vue.use(CKEditor);

export default {
  name: "Ckeditor4"
}
</script>

<style>

</style>