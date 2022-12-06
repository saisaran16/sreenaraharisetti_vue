<template>
  <div class="container">
    <!-- #3 must use the component-->
    <Header class="header" TitleName="STUDENTS GRADUATION COLLECTION"  />



    <Studentbox :student="student"  />
    <div class="About">
    <h1> <button><a href="https://sreenaraharisettifinal.herokuapp.com/"> Want to learn more about me!! </a></button> </h1>

    </div>


  </div>
</template>
<script>



//import HelloWorld from './components/HelloWorld.vue'
// 1
import Header from './components/Header.vue'
import Studentbox from './components/Studentbox.vue'



// data url: http://localhost:5555/books , this might be different for you
export default {
  name: 'App',
  components: {
    // 2 register the component 
    Header,
    Studentbox
  },

  data(){
    return {
      student: []
    }
  },
  methods: {
    // promises

      async fetchstudent(){
        //const res= await fetch('https://nodejs-mandadi-final.herokuapp.com/api')
         const res= await fetch('https://sreenaraharisettifinal.herokuapp.com/api')
         const data= await res.json()
          console.log("Data Here",data[0].books)
          console.log("Hello",typeof(data))
         return data[0].Student
      }

  },

  async created(){
    this.student = await this.fetchstudent()
    console.log("Hello1",typeof(this.student))
    console.log("here is",this.student)
  }
}
</script>










<style>


@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0px;
}
.header
{
  background: black;
}
body {
  font-family: 'Montserrat', sans-serif;
}
.container {
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 40px;
  border-radius: 5px;
  width:100%;
  background-color: white;
  background-image: url("https://expertphotography.b-cdn.net/wp-content/uploads/2019/05/graduation-pictures-hat-toss.jpg");

}

div{
  margin-bottom: 0.5em;
  padding:10px;
}
.About{
  width:100%;
}
a{
    text-decoration: none;
    color: rgb(2, 7, 16);

}
button{
    font-size:30px;
    font-family:'Times New Roman', Times, serif;
    background-color: rgb(193, 218, 224);
    width:100%;
    border:3px solid rgb(46, 99, 173);


}



</style>


