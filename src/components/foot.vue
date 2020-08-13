<script>
export default {
    name: 'myFoot',

    computed: {
        date(){
            return new Date().toJSON().slice(0,10).replace(/-/g,'/');
        }
    }
}
</script>

<template>
    <footer>
        <div class="foot">
            {{ date }}
        </div>
    </footer>
</template>

<style scoped>
    footer{
        background-color: white;
        font-size: 40px;
        text-align: center;
        margin: 0px;
        bottom: 0px;
        position: absolute;
        width: 100%;
        border-radius: 15px 15px 0px 0px;
        padding: 9px 0px 0px 0px;
    }
</style>