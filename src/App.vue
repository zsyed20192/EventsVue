<template>

  <div class="left">
  <img  src="https://scontent.fijd1-1.fna.fbcdn.net/v/t39.30808-6/241234267_10159535211425540_3858195344294893669_n.jpg?_nc_cat=106&ccb=1-7&_nc_sid=efb6e6&_nc_ohc=lSIX97INUwcAX-YvDKB&_nc_ht=scontent.fijd1-1.fna&oh=00_AfB9jcj8H_36cgbJJIiqHaq8QauBWNdQUU9PHefMOx21Hw&oe=6576DE2E" alt="">
  </div>
  <div class="right">
  <img src="https://i.ibb.co/P6mzHX1/OGISL-Logo-Blue-Background-1.jpg" alt="">
</div>

  <MyHeader university="University of New Haven" office="Office of Graduate and International Student Life" subtitle="Events List" />
  <EventsList :events=events />
  
</template>

<script>

import MyHeader from "./components/MyHeader.vue"
import EventsList from "./components/EventsList.vue"

export default{

  name: 'App',

  components:{
    MyHeader,
    EventsList
  },data(){
    return {
      events: []
    }
  },
  methods:{
    //promoises
    async fetchEvents(){
      const res = await fetch('https://eventsserver-2m6m.onrender.com/api');
      const data = await res.json()
      
      console.log(data)
      return data
    }
  },
  async created(){
      this.events = await this.fetchEvents();
  }

}

</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
}
.container {
  max-width: 400px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
}

.div{
  margin-bottom: 0.5em;
  display: inline-block;

}

.left{
  float: left;
}

.right{
  float: right  ;
}

.imgUNH{
  height: 150px;
  width: 150px;
  float: left;
}
.imgOGISL{
  height: 150px;
  width: 150px;
  float:right;

}

img{
  height: 250px;
  width:250px;
}


</style>
