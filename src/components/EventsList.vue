<template>
    <div v-for="event in events.events">
        <eventTab :event="event"/>
    </div>
</template>
<script>
import eventTab from './eventTab.vue';
export default{
    name: "EventsList",
    components:{
        eventTab
    },
    props:{
        events: Array
    }
}
</script>
<style>
</style>