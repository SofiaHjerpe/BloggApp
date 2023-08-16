<template>
  <div class="about-container">
        <h1 style="font-size: 20px;">About</h1>
        <p class="about-text"> This is a blogg made in Vue.js. I used V-for to display a For-loop of Objects. The user can show one Object by itself by clicking on the Show Post button. To get one post by itself I used params to get the id. In the mounted function I read in the params and a constant called post that found the id with the find method. Then I pass the props to the post page.</p> <br />
        <p class="about-text"> In this app the user can look at the blog posts on the Homepage. If the user clicks on Show post the user can show one post at the time. To go back to the Homepage the user can click on Go Back button. I use Vues green color on the buttons. The button also has a white bold text and a border-radius of 3px</p>
 </div>

</template>
<style scoped>
.about-container {
  display: flex; 
  justify-content: space-between;
  flex-direction: column;
  border-bottom: 2px solid #42b9836e;
}
.about-text {
  max-width: 900px;
  align-self: center;
}
</style>