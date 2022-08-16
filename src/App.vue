<template>
  <div class="allthings">
      <b-navbar toggleable="lg" type="dark" variant="#070C24">
          <b-container>
                    <b-navbar-brand  class="navbarword pr-4 pl-4" href="#">
                      <img src="../src/assets/logopa.png" alt="">
                    </b-navbar-brand>

                    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
                    <b-collapse id="nav-collapse" is-nav>
    
                    <b-navbar-nav class="mx-auto">
                        <b-nav-item><router-link class="home" to="/">Home</router-link></b-nav-item>
                        <b-nav-item><router-link class="about" to="/about">About</router-link></b-nav-item>
                        <b-nav-item><router-link class="Table" to="/Table">Axios</router-link></b-nav-item>
                    </b-navbar-nav> 
                      <!-- Right aligned nav items -->
                      <b-navbar-nav class="ms-auto">
                        <b-nav-item-dropdown text="Lang" right>
                          <b-dropdown-item href="#">EN</b-dropdown-item>
                          <b-dropdown-item href="#">AR</b-dropdown-item>
                        </b-nav-item-dropdown>
                      </b-navbar-nav>
                    </b-collapse>
          </b-container>
      </b-navbar>
  <div>

</div>
    <router-view/>

  </div>

  
</template>


<style scoped>
  .allthings
  {
    background-color: rgb(8, 214, 169);
    height: auto;
  }
  .navbarword
  {
    color:#6783FF;
    font-size:25px;
  }
  .home,.about,.Table
  {
    color: #849FB4;
    font-size: 15px;
    font-family:'Montserrat';
    text-decoration: none;
  }
</style>