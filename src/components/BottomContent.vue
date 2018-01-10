<template>
  <footer class="subnavigation">
    <p>2017 Tony Oliver-Paull</p>
    <div>
      <a href="https://www.linkedin.com/in/tony-oliverpaull-62b21434/" target="_blank">
        <i class="fa fa-linkedin-square" aria-hidden="true"></i>
      </a>
      <a href="https://github.com/tonyOP1985" target="_blank">
        <i class="fa fa-github-square" aria-hidden="true"></i>
      </a>
      <a href="https://www.facebook.com/TonyOliverPaull" target="_blank">
        <i class="fa fa-facebook-square" aria-hidden="true"></i>
      </a>
    </div>
  </footer>
</template>

<script>
  export default {
    name: 'bottomContent'
  }
</script>

<style scoped>
  footer {
    border-top: 1px solid rgba(0, 0, 0, 0.125);
    font-family: 'Merriweather', serif;
    color: rgba(0, 0, 0, 0.4);
    display: flex;
    justify-content: space-between;
    padding: 10px 10px 0 10px;
    margin-top: 20px;
  }

  footer > p {
    font-size: 0.8rem;
  }
</style>