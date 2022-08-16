<template>
    <b-container >
        <b-row>
            <b-col lg="1"></b-col>
              <b-col lg="10">
                  <b-table striped hover :items="items"></b-table>
              </b-col>
            <b-col lg="1"></b-col>
        </b-row>
    </b-container >
</template>


<style>
  table
  {
    color: white;
  }
  tr,th,td
  {
    border-color: white;
    color: white;
  }
  .td
  {
    border-bottom: 2px solid white;
  }
  td
  {
    color: white;
  }

   tr:nth-child(odd) {
    background-color: lightskyblue;
    }

   tr:nth-child(even) {
    background-color: lightpink;
    }

    th {
       background-color: lightseagreen;
    }


</style>



<script>

  import axios from 'axios'
  export default {
    data() {
      return {
      
        items: [

        ]
        
      }
    },
    created() {
      axios.get('https://jsonplaceholder.typicode.com/posts').then((res)=>{
        this.items = res.data
      })
    }
  }
</script>

