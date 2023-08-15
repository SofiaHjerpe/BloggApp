<template>
  <div class="about">
    <h1>About</h1>
    <p style="max-width: 900px; align-self: center"> This is a blogg. The blogg is made in Vue.js. I used V-for to display a For-loop of Objects. The user can show one Object by itself by clicking on the Show Post button To show one object I used a router-link to pass props to the child component.</p> <br />
    <p style="max-width: 900px; align-self: center"> In this app the user can look at the blog posts on the Homepage. If the user clicks on Show More Text the user can see more content. The user can then click on Show less button to show less content. If the user clicks on Show post the user can show one post at the time. To go back to the Homepage the user can click on  Back button. I use Vues green color on the buttons. The button also has a white bold text and a border-radius of 3px</p>
  </div>
</template>
<style scoped>
.about {
  display: flex;
  flex-direction: column;
}
</style>