<template>
    <nav class="navbar" role="navigation" aria-label="main navigation">
  <div class="navbar-brand">
    <a class="navbar-item" href="https://bulma.io">
      <img src="@/assets/Koffe.png" width="28" height="28">
    </a>
    <router-link class="navbar-item" to="/">
    <h3 class="title is-3">Ekoffe</h3>
     
    </router-link>

    <a role="button" class="navbar-burger" :class="{'is-active': isOpen}" @click.prevent="toggleMenu" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample">
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
    </a>
  </div>

  <div id="navbarBasicExample" class="navbar-menu" :class="{'is-active': isOpen}">
    <div class="navbar-start">
      <router-link class="navbar-item" to="/">
        Home
      </router-link>

    </div>

    <div class="navbar-end">
      <div class="navbar-item">
        <div class="buttons">
          <router-link class="button is-primary" to="/Register">
            <strong>Registrarme</strong>
          </router-link>
          <router-link class="button is-light" to="/Login">
            Iniciar Sesión
          </router-link>
        </div>
      </div>
    </div>
  </div>
</nav>
</template>

<script>


export default {
    data(){
        return{
            isOpen: false
        }
    },
    methods:{
        toggleMenu(){
            const status = !this.isOpen
            this.isOpen = status
        }
    }
}
</script>
