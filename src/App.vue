<script>
import EventsList from './components/EventsList.vue';
import MyHeader from './components/MyHeader.vue';

export default{
  name: "App",
  components:{
    EventsList, MyHeader
  },
  data(){
    return {
      eventlist: []
    }
  },
  methods:{
    //promoises
    async fetchevents(){
      const res = await fetch('https://backend-5nv6.onrender.com/api ');
      const data = await res.json()
      console.log(data)
      return data
    }
  },
  async created(){
      this.eventlist = await this.fetchevents();
  }
}
</script>

<template>
  <MyHeader/>
  <pre>{{eventlist.events}}</pre>
  <div v-for="event in eventlist">
    <EventsList :events="event"/>
  </div>
  
</template>

<style></style>
