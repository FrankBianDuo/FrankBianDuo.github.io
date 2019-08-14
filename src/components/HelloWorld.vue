<template>
  <div class="hello">
    <!-- <div class="alert alert-success alert-dismissible fade show" role="alert">
      With Bootstrap!
      <button type="button" class="close" data-dismiss="alert" aria-label="Close">
        <span aria-hidden="true">&times;</span>
      </button>
    </div> -->
    <div class="row">
      <div class="ml-4 col">
        <div class="d-flex justify-content-left align-items-center"> 
        <img style="width:100px;height:100px;" alt="Vue logo" src="../assets/frank.png">
        <h2 class="ml-3"> Hello, I'm Duoming! </h2>
        </div>
        <div class="mt-4 d-flex justify-content-left ">
          <h5>I am ...</h5>
        </div>
        <div class="d-flex justify-content-left ">
          <h5>A front-end developer.</h5>
        </div>
        <div class="d-flex justify-content-left ">
          <h5>A person who likes to bring new ideas into reality.</h5>
        </div>
        <div class=" d-flex justify-content-left ">
          <h5>A junior at the University of Michigan studying computer science.</h5>
        </div>
      </div>
      <div class="col">
        <div class="mt-3 pt-3 d-flex justify-content-left ">
          <h5>Find me at...</h5> 
        </div>
        <div class="mt-2 d-flex justify-content-left ">
          <a class="mr-4" href="https://www.linkedin.com/in/duoming-bian-umich/" title="Frank LinkedIn"><img style="width:50px;height:25px;" alt="Vue logo" src="../assets/linkedinIcon.png"></a>
          <a class="mr-4"  href="https://github.com/FrankBianDuo" title="Frank LinkedIn"><img style="width:25px;height:25px;" alt="Vue logo" src="../assets/github.png"></a>
          <img class="ml-3"  style="width:25px;height:25px;" alt="Vue logo" src="../assets/gmailIcon.png">
           <span class="ml-4"> bianduom@umich.edu </span>
        </div>
        <div class="mt-5 d-flex justify-content-left ">
          <h5 class="pt-3">Learn more about my...</h5> 
          <button type="button" v-on:click="greet(0)" class="pt-2 ml-4 btn btn-link btn-lg"> experience </button>
          <button type="button" v-on:click="greet(1)" class="pt-2 btn btn-link btn-lg"> education </button>
          <button type="button" v-on:click="greet(2)" class="pt-2 btn btn-link btn-lg"> projects </button>
        </div>
        <div class="mt-2 d-flex justify-content-left">
          <a href="../assets/Duoming_Bian_Resume_2019.pdf" download>Download My Resume</a>
        </div>
      </div>
    </div>
    <div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel">
      <ol class="carousel-indicators">
        <li data-target="#carouselExampleIndicators" data-slide-to="0" class="active"></li>
        <li data-target="#carouselExampleIndicators" data-slide-to="1"></li>
        <li data-target="#carouselExampleIndicators" data-slide-to="2"></li>
      </ol>
      <div class="carousel-inner" style="height: 550px;">
        <div style="height: 550px; background-color: #00BCF2;" class="carousel-item active">
          <div class="carousel-caption d-none d-md-block">
            <h3>Experience</h3>
            <p>Learn about My internship with Productiv and more</p>
          </div>
          <div class="row">
            <div class="col-3 d-flex flex-column mt-5 justify-content-left">
              <img style="width:250px;height:50px;" alt="Vue logo" src="../assets/Productiv.png">
            </div>
            <div class="col-8 text-left text-white mt-5 mr-2 justify-content-left align-content-center">
              <h4> Internship with Productiv </h4>
              <p> I interned with Productiv during summer 2019. Productiv is a SaaS app analyzing company,
                with a focus on providing insights on employees' usage events for IT managers. At Productiv,
                the tech stack primarily contains Node.js, Vue.js and AWS. As a team, Productiv collects employee usage information via deploying collectors and aggregators through AWS, and storage such data to DynamoDB, then display insights and recommendations for rightsizing on our product.</p>
              <p> As an intern, I had the opportunity to design and implement several different projects, both
                on the front end as well as the back end. </p>
              <p> On the back end, I designed and implemented an AWS lambda function that provides username recommendations during searching. It achieves this functionality by first collecting usernames from Productiv's DynamoDB database, then aggregate the usernames into search-tries that provide fast response when requested. This service is deployed as a lambda function and re-collects the data once a day. </p>
              <p> On the front end, I designed and developed several new UIs and functionalities, such as a dropdown that allows users to segment the data displayed by locations and teams, and an entirely new page that displays analyzing data for Zoom meetings usage. This is done with Vue.js and Vuex. </p>
            </div>
          </div>
        </div>
        <div style="height: 550px; background-color: #002D61;"  class="carousel-item">
          <div class="carousel-caption d-none d-md-block">
            <h3>Education</h3>
            <p>Check out my persue of Computer Science at University of Michigan</p>
          </div>
          <div class="row">
            <div class="col-3 d-flex flex-column justify-content-left align-content-center">
              <img style="width:325px;height:325px;" alt="Vue logo" src="../assets/UofM.png">
            </div>
            <div class="col-8 text-left text-white mt-5 mr-2 justify-content-left align-content-center">
              <h4> Bachelor of Science in Engineering </h4>
              <p> Currently I'm persuing a degree in Computer Science at the University of Michigan. My interest is primarily in front end developing, although I am also interested in computer security and operating system.</p>
              <p> Growing up, computers have been an important part of my childhood. With my father being a software engineer himself, I was greatly influenced by him and developed an interest in computers. Watching my father coding day after day, it was an easy decision for me to pick Computer Science as my major when I was offered a position in the University of Michigan. </p>
              <p>  </p>
            </div>
          </div>
        </div>
        <div style="height: 550px; background-color: #222222;"  class="carousel-item">
          <div class="carousel-caption d-none d-md-block">
            <h3>Projects</h3>
            <p>Ever wonder if there is a best strategy for Poker?</p>
          </div>
          <div class="row">
            <div class="col-3 d-flex flex-column mt-5 ml-5 justify-content-left align-content-center">
            <img style="width:325px;height:325px;" alt="Vue logo" src="../assets/club.png">
            </div>
            <div class="col-8 text-white mt-5 mr-5 text-left pr-5 justify-content-left align-content-center">
              <h4> Evolution of Poker Strategy </h4>
              <p> Poker is a complicated game. Some suggest there are superior strategies one can take, other suggest that it is pure gamble. Out of curiosity, along with two other friends, we are currently developing a website that gives you the options to create your own poker strategy and have it compete with other default strategies through a series of Poker games. The games will be simulated visually and winning strategies will replace losing strategies, similar to how evolution works. If your strategy ends up being the most populated one, it is a good indicator for a winning strategy. </p>
              <p> We are currently working on this project. It is made with React.js and Node.js. </p>
              <h4> Prisoner's Dilemma Simulator </h4>
              <p> I also worked on a project that lets two strangers play a game based off the famous Prisoner's Dilemma. The game is slightly modified so that the two players have to go through a series of games, where they have to choose to either cooperate or betray. We analyzed the data of how people make their decisions and found out that the most successful players tend to deploy a "tit for tac" strategy, meaning they alway cooperate when their opponent also cooperates, and vice versa. </p>
            </div>
          </div>
        </div>
      </div>
      <a class="carousel-control-prev" href="#carouselExampleIndicators" role="button" data-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="sr-only">Previous</span>
      </a>
      <a class="carousel-control-next" href="#carouselExampleIndicators" role="button" data-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="sr-only">Next</span>
      </a>
    </div>
  </div>
</template>

<script>

import JQuery from 'jquery'
const $ = JQuery;

export default {
  name: 'HelloWorld',
  props: {
  },
  methods: {
    greet(window) {
      // `this` inside methods points to the Vue instance
      $('.carousel').carousel(window)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
