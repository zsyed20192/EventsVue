<template>
    <div>
        <img src="" alt="" srcset="">
            <h1>{{university}}</h1>
            <h3>{{office}}</h3>
            <h3>{{subtitle}}</h3>

    </div>

</template>

<script>

export default{ // Exporting Default Object
    name: 'MyHeader',
    props:{ 

        university:String,
        office:String,
        subtitle: String
    }
}

</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@500&display=swap');
div{
    text-align: center;
    font-family: 'Roboto', sans-serif;
}
</style>