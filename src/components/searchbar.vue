<script>
    import axios from 'axios'



export default {
    name: 'searchbar',
   data(){
    return{
      villes: "",
      temp: "", 
      search: "",   
      }
  },

  methods: {
    getData(){
      const key = '3b6de3748556f5440a632467bbfbc6e2';
      const url = 'http://api.openweathermap.org/data/2.5/weather?q=';

    //   axios.get(url+ this.search + '&appid='+key)
    axios.get(url+this.search+"&?units=metric&APPID="+key)
      .then(response => {
        this.villes = response.data.name + "  " + response.data.sys.country;
        this.temp = response.data.main.temp ;
        console.log(response.data);

      }
      )
      .catch(function (error) {
    console.log(error);
  });
    }
  }
}

</script>

<template>
   <div>
    <header>
        <div class="search">
            <input type="text" class="input" placeholder="Type your request" v-model="search" @keyup.enter="getData"> 
        </div>
    </header>
    <div class="box">
        <div class="temp">{{temp}}<sup>oc</sup></div>
        <div class="pose">
            <img src="../assets/pose.svg" alt="my pose">
        </div>
    <div class="state">
        {{villes}}
    </div>
    </div>
   </div>
</template>

<style scoped>
    .search{
        text-align: center;
        background-color: white;
        border-radius: 10px;
        display: flex;
        align-items: stretch;
        flex-wrap: wrap;
        padding: 10px;
    }

    .input{
        text-align: left;
        width: auto;
        max-width: auto;
        flex-grow: 10;
        border: none;
    }
    input:focus, input:hover{
        border: none;
        outline: none;
        box-shadow: none;
    }

    
    header{
        background-color: white;
        border-radius: 20px 0px 20px 0px;
        text-align: center;
        margin: 10px;
    }
    header:hover{
        box-shadow: 1px 1px 2px 0px rgba(0,0,0,0.75);
    }


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