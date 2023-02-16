<template>
 <div class="container">
   <Quotes/>
 </div>
 
</template>

<script>
import Quotes from './components/Quotes.vue'

export default {
  name: 'App',
  components: {
    Quotes
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Caveat&display=swap');

*{
margin: 0;
padding: 0;
}

body{
background-image: linear-gradient(to top, #30cfd0 10%, #330867 90%);
font-family: 'Caveat', cursive;
}

.container{
margin: 25px;
width: 90%;
height: 95vh;
display: flex;
text-align: center;
flex-direction:column;
}
</style>