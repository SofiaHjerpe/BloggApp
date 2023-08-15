<template>
 <div style="display:flex; flex-direction: column">
   <p><b>{{ title }}</b>| Date: {{ date }}</p> <br />
   <p style="max-width: 900px; align-self: center">{{content}}</p>
     <router-link  :to="{name: 'home'}">
       <button>Go Back</button>
     </router-link>
 </div>
</template>

<script>
import data from "@/data";
export default {
  data() {
    return {
      title: "",
      date: "",
      content: ""
    }
  },
  mounted() {
    const id = this.$route.params.id;
    const post = data.posts.find(post => post.id == id);
    this.title = post.title;
    this.date = post.date;
    this.content = post.content;
  }
}
</script>
<style scoped>
button {
  background-color: #42b983;
  color: #fff;
  border: none;
  font-weight: 600;
  border-radius: 3px;
  padding: 10px 25px;
  height: 40px;
  margin-top: 100px;
}
</style>