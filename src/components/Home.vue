<template>
  <div>
    <div class="main-one">
      <div class="logo01">
        <img src="../assets/logo01.svg" alt="">
      </div>

      <ul>
        <li><a href="#contact-us">contact us</a></li>
        <li><a href="#what-we-do">what we do</a></li>
        <li><a href="#who-we-are">who we are </a></li>
      </ul>

      <div class="section">
        <span class="typer"> Matspon Consult & Services<br> is about
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
      <div class="item1" id="who-we-are" >
        <h2>WHO WE ARE</h2>
        <P ><strong>Matspon Consult & Sevices Limited</strong> is an indegenous company , we are client focused-business providing professional consultancy and support services in the area of Enviroment, Health and Safety, Project Management and much more. Today , Matspon Consult is strategically positioned to deliver beskpoke integrated solutions combining knowledge, expertise and expeience of our highly skilled partners on field  </P>
      </div>
      <div class="item2">
        <p>HERE AT <strong>MATSPON CONSULT</strong>, WE ARE A TEAM OF PROFESSIONALS GUIDED AND INSPIRED BY OUR VISION TO PROVIDE SUSTAINABLE & INNOVATIVE SOLUTIONS IN CONSONANCE WITH BEST PRACTICES</p>
      </div>
    </div>
    <div class="main-two"></div>
    <div id="what-we-do" class="container-two">
      <div class="item3">
        <h2>WHAT WE DO</h2>
      </div>
      <div class="container-3">
        <div class="item" v-for="(list , index) in lists" :key='index'>
          <i class="material-icons">{{list.icon}}</i>
          <div>{{list.title}}</div>
       </div>
      </div>
    </div>
    <div class="main-three"></div>
    <footer id="contact-us">
      <div class="footers">
        <h3>Matspon Consult & Services Limited <span>(RC12345)</span></h3>
          <div class="addy">
            5, Shakiru Adeoye Street, Ogudu, Lagos.<br>
            +234 802 853 4149 | +234 806 685 5349<br>
            matsponconsult@gmail.com<br>
            <span> <strong>Matspon Consult & Services Limited 2020 </strong></span><i class="material-icons"> coronavirus</i>
          </div>
      </div>
    </footer>
  </div>
 

</template>

<script>
export default {
  name: 'Home',

  data() {
    return {
      lists : [
        {title: "Health Safety Enviroment & Quality HSEQ", icon: "public"},
        {title: "Procurement Services", icon: "assignment"},
        {title: "Construction", icon: "construction"},
        {title: "Logistics", icon: "local_shipping"},
         {title: "Agribusiness", icon: "eco"},
        {title: "Oil and Gas", icon: "local_gas_station"},
        {title: "Project Management", icon: "event"},
        {title: "Business Development", icon: "power"},
         {title: "Tech", icon: "memory"},

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
  height: 80vh;
  opacity: 0.7;
}
.main-three {
  background-image: url("../assets/bk66.jpg");
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  height: 70vh;
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
  font-size: 45px;
  color:white ;
  font-weight: bold;
  letter-spacing: 4px;
}

.container-one {
  display: grid;
  padding: 50px 80px;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
  grid-gap: 10px ;
  letter-spacing: 2px;
  color: #4d2c1f;
}

.item1 {
 grid-column: 1/3;
 font-size: 14px;
 text-align: justify;
}

.item1 p {
  text-align:justify;
  line-height: 25px;
}

.item2 {
 grid-column: 4/6;
 line-height: 35px;
}

.container-two{
  padding: 50px 80px;
  height : 380px;
  background-color:white;

}
.item3 h2 {
  text-align: center;
  letter-spacing: 2px;
  color: #4d2c1f;
}
.container-3 {
  display: grid;
  padding: 50px 80px;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  grid-gap: 20px 20px;
  height: 300px;
  font-size: 14px;
  text-align:center;
  color:#4d2c1f;
} 

footer{
  display: grid;
  grid-template-columns: auto auto ;
  padding: 5px 40px;
  justify-content: space-between;
  background-color:white;
  color: #4d2c1f;
  
}
.addy {
  font-size : 14px;
  line-height: 25px;
}


/* turn off parallax effect for mobile devices and tablets */
@media only screen and (max-device-width: 1024px) {
  .main-one, .main-two, .main-three {
    background-attachment: scroll;
  }
  ul {
  visibility: hidden;
  }

  .logo01 {
    width: 130px;
    position: absolute;
    top: 60px;
    left: 30%;
  }

  .section {
    position: absolute;
    left: 0%;
    top : 50%;
    text-align: center;
    width: 100%;
  }
  .section span.typer {
    font-size: 18px;
    color:white ;
    letter-spacing: 1px;
    font-weight: bold;
    line-height: 30px;
  }


  .container-one {
    display: inline-block;
    padding: 25px 40px;
    letter-spacing: 0px;
    color: #4d2c1f;
  }

  .item1 h2 {
  font-size: 20px;
  text-align: center;
  font-weight: bold;
  margin-top:40px ;
  }

  .item1 p {
    text-align:justify;
    font-size: 15px;
    margin-bottom: 40px;
    line-height: 25px;
  }

  .item2 {
    text-align: center;
    margin-top: 20px;
  }
  .item2 p {
    font-size: 15px;
    letter-spacing: 1px;
    line-height: 35px;
  }


  .container-two{
    padding: 0px 0px;
    height : 500px;
    background-color:white;

  }
  .item3 h2 {
    text-align: center;
    letter-spacing: 1px;
    color: #4d2c1f;
    margin-top: 40px;
    font-weight: bold;
  }
  .container-3 {
    display: grid;
    padding: 25px 40px;
    grid-template-columns: 1fr 1fr;
    grid-gap: 30px 40px;
    height: 300px;
    font-size: 15px;
    text-align:center;
    color:#4d2c1f;
  } 


  footer{
    display: block;
    padding: 0px 0px;
    text-align: center;
    background-color:white;
    color: #4d2c1f;
  }
  .footers h3 {
    font-size: 12px;
    font-weight:bold;
    letter-spacing: 1px;
  }
  .addy {
    font-size : 10px;
    line-height: 15px;
    letter-spacing: 1px;
    margin-bottom: 3px;
  }
}
</style>
