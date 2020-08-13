<script>
export default {
    name: 'myMain',
}
</script>

<template>
    <div class="box">
        <div class="temp">25<sup>oc</sup></div>
        <div class="pose">
            <img src="../assets/pose.svg" alt="my pose">
        </div>
    <div class="state">
        Gonaives
    </div>
    </div>
    
</template>

<style scoped>


@media screen and (max-width: 728px){
    .temp{
    color: white;
    font-weight: 600;
    font-size: 50px;
    padding: 0px 0px 0px 20px;
}

img{
    height: 200px;
    width: 200px;
}
.pose{
    justify-content: center;
    text-align: center;
    padding: 0px 0px 0px 0px;
}

.state{
    color: white;
    font-weight: 600;
    font-size: 45px;
    padding: 0px 0px 0px 20px;
}

    .box{
        border: none;
        background: none;
        margin: 40px 0px 0px 0px;
    }
}

img{
    height: 230px;
    width: 230px;
}
.pose{
    justify-content: center;
    text-align: center;
    padding: 0px 0px 0px 0px;
}

.temp, .state{
    padding: 0px;
    text-align: center;
    color: white;
    font-weight: 600;
    font-size: 45px;
}

.box{
    border: solid 1px #6dff3017;
    background-color: #6dff3017;
    box-shadow: 1px 1px 2px 0px rgba(0,0,0,0.75);
    }








</style>