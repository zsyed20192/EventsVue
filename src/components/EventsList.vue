<template>
    <div v-for="event of events" :key="event.id" >

        <SingleEvent v-if="event" :event=event />
 
     </div>
</template>

<script>
import SingleEvent from './SingleEvent.vue'

export default {
    name: 'EventsList',
    props:{
        events: Array
    },
    components:{
        SingleEvent
    }
    
}
</script>

<style scoped>

div{
    align-content: center;
}
    

</style>

