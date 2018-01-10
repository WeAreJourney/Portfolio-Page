<template>
  <b-navbar toggleable="md" type="light" variant="info">

  <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>

  <b-navbar-brand to="/">Tony Oliver-Paull</b-navbar-brand>

  <b-collapse is-nav id="nav_collapse">
    <!-- Right aligned nav items -->
    <b-navbar-nav class="ml-auto">
      <div v-for="link in links">
        <b-nav-item :to="link.to">{{ link.text }}</b-nav-item>
      </div>

    </b-navbar-nav>

  </b-collapse>
</b-navbar>

</template>

<script>
export default {
   /* eslint-disable */
  name: 'navBar',
  data () {
    return {
      links: [
        { text: 'Home', to: '/' },
        { text: 'Projects', to: '/projects' },
        { text: 'Resume', to: '/resume' },
        { text: 'Contact', to: '/contact' }
      ]
    }
  }
}
</script>

<style scoped>
 nav {
  font-family: 'Montserrat', sans-serif;
  letter-spacing: 0.2rem;
  text-transform: uppercase;
  box-shadow: 0px 3px 6px rgba(0,0,0,0.16),0px 3px 6px rgba(0,0,0,0.23);
 }

 .bg-info {
   background-color: rgb(255, 255, 255) !important;
 }

 .nav-links {
    text-decoration: none;
    color: rgba(0, 0, 0, 0.9);
 }

 @media (max-width: 400px) {
  .navbar-brand {
    font-size: 0.8rem;
    letter-spacing: 0.1rem;
  }
 }

 @media (max-width: 300px) {
  .navbar-brand {
    display: none;
  }
 }
</style>