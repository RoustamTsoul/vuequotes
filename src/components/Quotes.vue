<template>
  <div class="quotes">
    <p class="santence">{{santence}}</p>
    <h3 class="author">{{author}}</h3>
  </div>
  <div class="btn">
    <button @click="generate()" class="btn btn-info">Generate Quotes</button>
  </div>
</template>

<script>
export default {
    data(){
        return{
            quotes:{
                "― Jules Renard":'“The truly free man is the one who can turn down an invitation to dinner without giving an excuse.”',
                "― Patrick McGoohan":'“I am not a number; I am a free man.',
                "― Johann von Goethe":'“The best slave is the one who thinks he is free.”',
                "― John O'Callaghan":'“I am more than what they say I am.”',
                "― Ogwo David Emenike":'“Education is for freedom - freedom from mental slavery.”',
                "-Maya Angelo":'"The truth is, no one of us can be free until everybody is free."'
            },

            author:'',
            santence:'',
        }
    },

    methods:{
        generate(){
            let authors = Object.keys(this.quotes);
            this.author = authors[Math.floor(Math.random() * authors.length )];
            this.santence = this.quotes[this.author]
        }
    }
}
</script>

<style scoped>
.quotes{
width: 800px;
height: 400px;
margin: auto;
display: flex;
flex-direction: column;
justify-content: center;
align-items: center;
padding: 0 50px;
}

.santence{
font-size: 2.5rem;
}

.author{
font-size: 2.5rem;
}

.btn{
width: 200px;
padding: 15px 15px;
margin: auto;
display: flex;
justify-content: center;
background-color: #050801;
color: #03e9f4;
font-weight: bold;
border: none;
border-radius: 5px;
letter-spacing: 4px;
overflow: hidden;
transition: 0.5s;
cursor: pointer;

}

.btn:hover{
background: #03e9f4;
color: #050801;
box-shadow: 0 0 5px #03e9f4,
    0 0 25px #03e9f4,
    0 0 50px #03e9f4,
    0 0 200px #03e9f4;
    -webkit-box-reflect:below 1px linear-gradient(transparent, #0005);
}
</style>