<template>
<div class="container">
    <div class="row mt-4">
      <div class="col text-center">
        <h1 class="light">Markdown Editor</h1>
      </div>

    </div>

    <div class="row mt-8 text-center">
      <div class="col md-6">
        <h3 class="light">Markdown</h3>
        <textarea class="info" 
        v-model="markdown"
        />   

      </div>

      <div class="col md-6 text-center">
        <h3 class="light">Preview</h3>
        <div 
        :key="markdown"
        class="info"
        v-markdown
        >{{markdown}}  
          
        </div>
      </div>

    </div>


  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      markdown: '',
    };
  }
}
</script>

<style scoped>
.info {
    height: 600px;
    width: 100%;
    background-color: rgba(255, 255, 255, 0.9);
    text-align: left ;

}

textarea {
    resize: none;
    border: 2px dashed green;
    outline: none;
}
</style>>

