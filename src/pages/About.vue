<template>
  <Navbar />
  <section class="about">

        <h1 class="heading"> about <span>me</span> </h1>

        <div class="row">

            <div class="info-container">

                <h1>personal info</h1>

                <div class="box-container">

                    <div class="box">
                        <h3> <span>name : </span> {{name}} </h3>
                        <h3> <span>age : </span> {{age}} </h3>
                        <h3> <span>email : </span> {{email}} </h3>
                    </div>

                    <div class="box">
                        <h3> <span>occupation : </span> {{occupation}} </h3>
                        <h3> <span>address : </span> {{address}} </h3>
                        <h3> <span>language : </span> {{language}} </h3>
                    </div>

                </div>

            </div>

        </div>

    </section>

    <!-- about section ends -->

    <!-- education section starts  -->

    <section class="education">

        <h1 class="heading"> <span>my</span> experience </h1>

        <div class="box-container">

            <div class="box" v-for="e in experiences" :key="e.years">
                <i class="fas fa-briefcase"></i>
                <span>{{e.years}}</span>
                <h3>{{e.company}}</h3>
                <p>{{e.jobs}}</p>
            </div>

        </div>

    </section>
</template>

<script>
import Navbar from '../components/Navbar.vue'
export default {
  components: { Navbar },
  data() {
    return {
      name:'Suwaphat Sriwiset',
      age:'19',
      email:'suwaphat.sriw@bumail.net',
      address:'Pathum Thani, Thailand 12120',
      language:'thai',
      occupation:'student',
      experiences: [{
        years:'2016 - 2017',
        company:'INTER EXPRESS LOGISTICS PRIVATE LIMITED',
        jobs:'Assist the system analyst in conduct analysis, architecture, design database model for the new application.'
      },{
        years:'2017 - 2018',
        company:'PTT Digital Solutions Company Limited',
        jobs:'Front-end coding to develop web applications follows by mock-up screen design. And back-end coding and test to configuration workflows and business processes.'
      },{
        years:'2018 - 2018',
        company:'Thai Beverage PLC',
        jobs:'Develop new features to facilitate related procedures and tools if necessary, Troubleshoot, test, and maintain the core product software and databases to ensure strong optimization and functionality.'
      },{
        years:'2019 - 2020',
        company:'Cigna',
        jobs:'Assist the system analyst in conduct analysis, architecture, design database model for the new application.'
      },{
        years:'2019 - 2020',
        company:'EMETWORKS',
        jobs:'Develop new features to facilitate related procedures and tools if necessary.'
      },{
        years:'2020 - 2021',
        company:'uTech Solutions',
        jobs:'Assist the system analyst in conduct analysis, architecture, design database model for the new application.'
      }]
    }
  }
}
</script>

<style>

</style>