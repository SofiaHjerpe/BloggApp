<template>
 <div class="post">
    <span style="display: flex; flex-direction: column">
      <p><b>{{ title }}</b>| Date: {{ date }}</p> <br />
      <p style="max-width: 900px; align-self: center">{{content}}</p>
    </span>
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
.post {
  display: flex; 
  flex-direction: row;
  justify-content: space-between;
  margin: 16px;
  gap: 10px;
  border-bottom: 2px solid #42b9836e;
}
button {
  background-color: #42b983;
  color: #fff;
  border: none;
  font-weight: 600;
  border-radius: 3px;
  padding: 10px 25px;
  margin-top: 100px;
  height: 40px;
}
</style>