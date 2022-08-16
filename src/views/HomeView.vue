<template>
  <b-container>
      <B-row>
          <b-col lg="1"></b-col>
          <b-col lg="10">
            
                <div class="overflow-auto">
                <b-pagination
                  v-model="currentPage"
                  :total-rows="rows"
                  :per-page="perPage"
                  aria-controls="my-table"
                ></b-pagination>  

      

                <p class="Current mt-3">Current Page: {{ currentPage }}</p>

                <div class="d-flex justify-content-end">
                     <b-button @click="goToHome()" class="btn-sing mb-2 " variant="outline-primary">
                      go forms
                    </b-button>
                </div>


                <b-table
                  id="my-table"
                  :items="items"
                  :per-page="perPage"
                  :current-page="currentPage"
                  small
                ></b-table>
              </div>
          </b-col>

          <b-col lg="1"></b-col>
      </B-row>
  </b-container>
</template>

<script>
  export default {
    data() {
      return {
        perPage: 4,
        currentPage: 1,
        items: [
          { id: 1, first_name: 'Fred', last_name: 'Flintstone' },
          { id: 2, first_name: 'Wilma', last_name: 'Flintstone' },
          { id: 3, first_name: 'Barney', last_name: 'Rubble' },
          { id: 4, first_name: 'Betty', last_name: 'Rubble' },
          { id: 5, first_name: 'Pebbles', last_name: 'Flintstone' },
          { id: 6, first_name: 'Bamm Bamm', last_name: 'Rubble' },
          { id: 7, first_name: 'The Great', last_name: 'Gazzoo' },
          { id: 8, first_name: 'Rockhead', last_name: 'Slate' },
          { id: 9, first_name: 'Pearl', last_name: 'Slaghoople' }
        ]
      }
    },
    computed: {
      rows() {
        return this.items.length
      }
    },
     methods:{
        goToHome(){
        this.$router.push('/about'); 
    }
  }
  }
</script>


<style scoped>
  .Current
  {
    color: white;
  }
  .sing
  {
    color: white;
    text-decoration: none;
  }
  .btn-sing
  {
    width: 100px;
  }
  .btn-sing:hover
  {
    background-color: #070C24;
  }
</style>