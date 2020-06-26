<template>
  <div>
    <div class="main-one">
      <div class="logo01">
        <img src="../assets/logo01.svg" alt="">
      </div>

      <ul>
        <li><a href="">contact us</a></li>
        <li><a href="">what we do</a></li>
        <li><a href="">who we are </a></li>
      </ul>

      <div class="section">
        <span class="typer"> {{message}}
          <vue-typer
            :text='[" Dexterity"," Consistency "," Technology "," Innovation "," Professionalism ", " Safety ", " Client Satisfaction ", "Team Work"]'
            :repeat='Infinity'
            :shuffle='false'
            initial-action='typing'
            :pre-type-delay='1000'
            :type-delay='200'
            :pre-erase-delay='4000'
            :erase-delay='100'
            erase-style='backspace'
            :erase-on-complete='false'
            caret-animation='blink' >
          </vue-typer>
        </span>
      </div>
    </div>

    <div class="container-one">
      <div class="item1">
        <h2>WHO WE ARE</h2>
        <P >Matspon Consult & Sevices Limited is an indegenous company , we are client focused-business providing professional consultancy and support services in the area of Enviroment, Health and Safety, Project Management and much more. Today , Matspon Consult is strategically positioned to deliver beskpoke integrated solutions combining knowledge, expertise and expeience of our highly skilled partners on field  </P>
      </div>
      <div class="item2">
        <h3> HERE AT MATSPON CONSULT, WE ARE GUIDED AND INSPIRED BY OUR VISION TO PROVIDE SUSTAINABLE & INNOVATIVE SOLUTIONS IN CONSONANCE WITH BEST PRACTICES</h3>
      </div>
    </div>
    <div class="main-two"></div>
    <div class="container-two">
      <div class="item3">
        <h2>WHAT WE DO</h2>
      </div>
      <div class="container-3">
        <div class="item" v-for="(list , index) in lists" :key='index'>
          <i class="material-icons">{{list.icon}}</i> <span>{{list.title}}</span>
       </div>
      </div>
      <div class="main-three"></div>
      
    </div>
   
  </div>
 

</template>

<script>
export default {
  name: 'Home',

  data() {
    return {
      message: " Matspon Consult & Services Limited is about ",
      lists : [
        {title: "Health Safety Enviroment & Quality HSEQ", icon: "public"},
        {title: "Procurement Services", icon: "payment"},
        {title: "Construction", icon: "construction"},
        {title: "Logistics", icon: "local_shipping"},
         {title: "Agribusiness", icon: "local_florist"},
        {title: "Oil and Gas", icon: "local_gas_station"},
        {title: "Project Management", icon: "event"},
        {title: "Business Development", icon: "work_outline"},
         {title: "Tech", icon: "security"},

      ]
    }
  }
 
}
</script>


<style scoped>

.main-one {
  background-image: url("../assets/bk01.jpg");
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  height: 100vh;
}
.main-two {
  background-image: url("../assets/bk04.jpg");
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  height: 100vh;
  opacity: 0.7;
}
.main-three {
  background-image: url("../assets/bk03.jpg");
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  height: 100vh;
  opacity: 0.7;
}
.logo01 {
  width: 100px;
  position: absolute;
  top: 20px;
  left: 5%;
}

 ul {
   margin: 0;
   list-style-type: none;
 }
ul li {
  float : right;
  margin: 40px 5% 0px 0px 
}
ul li a {
  text-decoration: none;
  font-size: 14px;
  padding: 5px 5px;
  color: #4d2c1f;
  font-weight: bold;
  letter-spacing: 2px;
}

ul li a:hover {
  color : white;
}
.section {
  position: absolute;
  left: 0%;
  top : 50%;
  text-align: center;
  width: 100%
}

.section span.typer {
  font-size: 40px;
  color:white ;
  padding: 10px;
  background-color: #4d2c1f;
  opacity: 0.8;
}

.container-one {
  display: grid;
  padding: 50px 80px;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
  grid-gap: 10px ;
  height: 300px;
  letter-spacing: 2px;
  color: #4d2c1f;
}

.item1 {
 grid-column: 1/3;
}

.item1 p {
  text-align: justify;
}

.item2 {
 grid-column: 4/6;
}

.container-two{
  padding: 50px 80px;
  height : 400px;

}
.item3 h2 {
  text-align: center;
  letter-spacing: 2px;
  color: #4d2c1f;
}
.container-3 {
  display: grid;
  padding: 50px 80px;
  grid-template-columns: auto auto auto auto;
  grid-gap: 20px 20px;
  height: 300px;
  justify-content: center;
  align-content: space-around;
} 

</style>
