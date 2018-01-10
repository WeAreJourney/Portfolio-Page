<template>
  <div class="main">
    <header>
      <div class="title">
        <h1>Resume</h1>
        <a href="../../static/resume/AnthonyOliver-PaullResume.docx.pdf" class="btn btn-primary" target="_blank">Printable Resume</a>
      </div>
    </header>
    <h1 class="sub-title">Education</h1>
    <b-container>
      <div class="row">
        <div class="col-sm-6">
          <div class="card">
            <div class="card-body">
              <h4 class="card-title">Winthrop University</h4>
              <p>Rock Hill, SC | 2012-2014</p>
              <p>Master of Music</p>
            </div>
          </div>
        </div>
        <div class="col-sm-6">
          <div class="card">
            <div class="card-body">
              <h4 class="card-title">Winthrop University</h4>
              <p>Rock Hill, SC | 2003-2007</p>
              <p>Bachelor of Music</p>
            </div>
          </div>
        </div>
      </div>
      <h1 class="sub-title">Skills</h1>
      <div class="row justify-content-center icon-row">
        <div class="col-sm-12">
          <i class="devicon-html5-plain-wordmark colored"></i>
          <i class="devicon-css3-plain-wordmark colored"></i>
          <i class="devicon-bootstrap-plain-wordmark colored"></i>
          <i class="devicon-jquery-plain-wordmark colored"></i>
        </div>
      </div>
      <div class="row justify-content-center icon-row">
        <div class="col-sm-12">
          <i class="devicon-javascript-plain colored"></i>
          <i class="devicon-nodejs-plain colored"></i>
          <i class="devicon-mocha-plain colored"></i>
          <i class="devicon-vuejs-plain-wordmark colored"></i>
        </div>
      </div>
      <div class="row justify-content-center icon-row">
        <div class="col-sm-12">
          <i class="devicon-express-original-wordmark colored"></i>
            <i class="devicon-php-plain colored"></i>
            <i class="devicon-mysql-plain-wordmark colored"></i>
            <i class="devicon-visualstudio-plain colored"></i>            
        </div>
      </div>
      <div class="row justify-content-center icon-row">
        <div class="col-sm-12">             
          <i class="devicon-mongodb-plain-wordmark colored"></i>  
            <i class="devicon-python-plain-wordmark colored"></i>
            <i class="devicon-heroku-plain-wordmark colored"></i>
            <i class="devicon-github-plain-wordmark colored"></i>
        </div>
      </div>
    </b-container>  
  </div>
</template>

<script>
  export default {
    name: 'resume'
  }
</script>

<style scoped>
  header {
    width: 100%;
    height: 200px;
    background-color: #f5f8fa; 
    padding-bottom: 10px;
    border-bottom: 1px solid rgba(0, 0, 0, 0.125);
  }

  .title {
    width: 50%;
    margin: 0 auto;
    padding-top: 40px;
    text-align: center;
  }

  .title > h1, .sub-title {
    color: #3A4145;
    font-family: montserrat, sans-serif;
    text-transform: uppercase;
    letter-spacing: 0.2rem;
    font-weight: 900;
  }

  .sub-title {
    padding: 20px 0;
    font-size: 1.5rem;
  }

  .row {
    display: flex;
    justify-content: space-between;
    margin: 20px 0;
  }

  .card {
    font-family: 'Merriweather', serif;
  }

  i {
    font-size: 80px;
    padding: 0 50px 50px 50px;
    margin-bottom: 20px;
  }

  @media (max-width: 1000px) {
    i {
      font-size: 50px;
    }
  }

  @media (max-width: 768px) {
    i {
      padding: 20px;
    }
  }

  @media (max-width: 430px) {
    i {
      font-size: 30px;
      padding: 0;
    }
  }

  @media (max-width: 500px) {
    .title {
      width: 100%;
    }

    .title > h1 {
      font-size: 1.5rem;
    }

    header {
      height: 150px;
    }
  }

</style>