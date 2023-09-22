<template>
    <div class="main-content">
      <breadcumb :page="'Bikers'" :folder="'Transport'" :folder2="'Bikers'" />
      
  
  </div>
  </template>
  <script>
  //import { VueEditor } from "vue2-editor";
  
  export default {
    metaInfo: {
      // if no subcomponents specify a metaInfo.title, this title will be used
      title: "Inbox"
    },
    components: {
     // VueEditor
    },
  
    data() {
      return {
        content: "<h1>Some initial content</h1>"
      };
    },
    methods: {
      editor() {}
    }
  };
  </script>