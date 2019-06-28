<template>
  <div>
    <div>
      <b-navbar toggleable="lg" type="dark" variant="dark">
        <router-link to="/">
          <b-navbar-brand>VueShop</b-navbar-brand>
        </router-link>
        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav>
            <router-link to="/" class="nav-link">Home</router-link>
            <router-link to="/about" class="nav-link">About</router-link>
            <router-link to="/contact" class="nav-link">Contact</router-link>
          </b-navbar-nav>
       <b-navbar-nav class="ml-auto">
        <b-nav-form>
          <b-form-input size="sm" class="mr-sm-2" placeholder="Search"></b-form-input>
          <b-button size="sm" class="my-2 my-sm-0" type="submit">Search</b-button>
        </b-nav-form>
       </b-navbar-nav>
       <b-navbar-nav right>
         <div v-if="!state"><router-link to="/about" class="nav-link">SignIn</router-link></div>
        <div v-else><router-link to="/about" class="nav-link">SignUp</router-link></div>
        
       </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>

    <router-view />
  </div>
</template>

<script>
export default {
  data(){
    return{
      state: false
    }
  }
}
</script>

<style lang="scss">

</style>
