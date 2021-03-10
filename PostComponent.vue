
<template>
  <div>
    <h1>Submit data to API</h1>
    <form @submit="postData" mothod="post">
      <input type="text" name="author" placeholder="author" v-model="posts.author"><br><br>
      <input type="text" name="title" placeholder="title" v-model="posts.title"><br><br>
      <button type="submit">Post</button>
    </form>
  </div>

</template>

<script>
import Vue from 'vue'
import axios from 'axios'
import VueAxios from 'vue-axios'
const app = Vue.createApp(App)
app.use(VueAxios, axios)
//Skal lige have hjælp.

export default{
  name:"PostComponent",
  data(){
    return{
      posts:{
        title:null,
        author:null
      }
    }
  },

  methods:{
    postData(e){
      console.warn(this.posts)
      e.preventDefault()
      }
    }
}
</script>
