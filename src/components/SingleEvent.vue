<template>
    <div>
    <div class="event">
       
            {{event.name}}<br>
            {{event.date}}<br>
            {{event.time}}<br>
            {{event.host}}<br>
            {{event.venue}}<br>
            {{event.type}}<br>
       
        </div>
</div>
</template>

<script>
export default{
    name: 'SingleEvent',
    props:{
        event: Array
}
}

</script>

<style scoped>
h4{
    margin: 2px;
}

div{
    
    margin: 20px;
    
    

    

}

@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@500&display=swap');
.event{
    padding: 100px;
    color: #ffca02;
    padding: 1em;
    text-align: center;
    width: 50%;
    margin: auto;
    background-color: #004785;
    border-style: dashed;
    font-size: larger;
    font-family: 'Roboto', sans-serif;
}
div{
    align-content: center;
}
</style>