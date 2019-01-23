<template>
  <div id="editor">
    <quill-editor>

    </quill-editor>
  </div>
</template>

<script>
    export default {
        name: "Quill",
      data(){
        return{
          content:null,
          editorOption:{
            modules:{
              toolbar:[
                ['bold', 'italic', 'underline', 'strike'],        // toggled buttons
                ['blockquote', 'code-block']
              ]
            }
          },
        }
      },
    }
</script>

<style scoped>
  .quill-editor{
    height: 500px;
    width: 900px;
  }
</style>
