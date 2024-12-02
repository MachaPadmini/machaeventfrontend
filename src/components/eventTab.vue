<template>
  
        <div class="eventTab">
          <h3>{{ event.name }}</h3>
          <a>Date: {{ event.date }} </a>
          <a>Time: {{ event.time }} EST</a>
          <br />
          <a>Platform {{ event.platform }}</a
          ><br />
          <a>Organizer: {{ event.organizer }}</a>
          <br />
          <a :href='event.Registrationlink'>Registration link</a>
        </div>
</template>

<script>

export default {
  name: "EventTab",
  props:{
    event: Array
  }
}
</script>
<style>
.eventTab h3 {
  color: rgb(2, 34, 57);
}
.eventTab {
  text-align: center;
  border: 1px solid rgb(239, 235, 235);
  width: 90%;
  margin-left: auto;
  margin-right: auto;
  margin-top: 10px;
  margin-bottom: 10px;
  background-color: rgb(235, 227, 224);
}

.heading {
  text-align: center;
}
.eventContainer {
  border: 1px solid rgb(249, 249, 249);
  padding: 10px;
  width: 80%;
  margin-left: auto;
  margin-right: auto;
  background-color: rgb(222, 217, 221);
}

#app{
  background-color: rgb(171, 168, 168);
  text-align: center;
  color: rgb(18, 2, 49);
}
</style>