<template>
  <div>
    <input v-model="texto" type="text" @change="consultaApi" />

    {{ info }}

<!--         <div v-for="pessoa  in info" v-bind:key="pessoa" >

      {{pessoa}}
    </div> -->
  </div>
</template>

<script>
import axios from "axios";

export default {

  
  data() {
    
    return {
      info: {},
      texto: "",
    };
  },
  methods:{
         consultaApi(){
          
    var session_url = "endereco api"+this.texto;

    var uname = "usuario";
    var pass = "senha";

    const res = axios
      .get(
        session_url,
        {
          withCredentials: true,
          headers: {
            Accept: "application/json",
            "Content-Type": "application/json",
          }
        },
        {
          auth: {
            USERNAME: uname,
            PASSWORD: pass
          },
        }
      )
      .catch((err) => err)
      .then((response) => {
        let responsedata = response.data;
        // get key do array 
      for (var Index in responsedata) {
       this.info = responsedata[Index];
       //console.log( responsedata[Index])
      }
      
      });




    console.log(res.status);
  
         }


  }
  

};
</script>

<style>
</style>