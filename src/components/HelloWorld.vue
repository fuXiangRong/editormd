<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div id="editormd">
      <textarea style="display:none;">### Hello Editor.md !</textarea>
    </div>
  </div>
</template>

<script>
import editor from '../public-source/plugins/editor.md/editormd.js'
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  mounted(){
    var testEditor = editormd("editormd", {
        width: "90%",
        height: 740,
    });
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import "../public-source/plugins/editor.md/css/editormd.css";
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
