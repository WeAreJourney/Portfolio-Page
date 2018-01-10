<template>
  <div class="main">
    <div class="about-wrapper">
      <section class="about">
        <div class="image">
          <b-img src="../../static/images/tonyLesPaull.png" thumbnail fluid rounded="circle" width="200" height="200" />
        </div>
        <div class="name">
          <h1>Tony Oliver-Paull</h1>
        </div>
        <div class="about-para">
          <p>Full-stack web developer</p>
        </div>
      </section>
      <section class="about-me container">
        <b-row class="justify-content-center">
          <div class="col-lg-5 col-md-12 col-sm-12">
            <div class="about-me-heading">
              <h1>About me</h1>
            </div>
            <div class="about-me-p">
              <p>
              <!-- I am a person who enjoys being challanged.  Music was my first major challege.  Afte years of working with music the time came for to find a challege outside of music.  This lead me to start learning how to code.  Since then I have grown very passinate about coding have grown to have a continual desire to learn more.  I​ ​enjoy​ ​being​ ​challenged​ ​by​ ​new,​ ​complex​ ​problems and​ ​working​ ​on​ ​projects​ ​that​ ​require​ ​me​ ​to​ ​extend​ ​myself​ ​outside​ ​of​ ​my​ ​comfort​ ​zone​ ​and knowledge​ ​set.  For more info check out my projects and resume.  Also, don't hesitate to send me a message.​​ -->
              I am a full-stack web-developer who has experince with many different technologies.  These technologies include Javascript, HTML, CSS, Vue.js, Node.js, PHP, Python, Mongo DB, and MySQL.  Ever since I started to learn development I have grown very passionate about it.  I have a continual desire to learn more.  I enjoy working on projects that require me to extend myself to outside of my comfort zone an knowledge set.  Check out my <b-link to="/resume">resume</b-link> and <b-link to="projects">project</b-link> pages.
              </p>
            </div>
          </div>
          <div class="media col-lg-2 col-md-12 col-sm-12">
            <div class="about-me-heading">
              <h1>Contact</h1>
            </div>
            <div>
              <b-link class="row media-item" 
                      href="https://www.linkedin.com/in/tony-oliverpaull-62b21434/" 
                      target="_blank" >
                <i class="fa fa-linkedin-square fa-2x" aria-hidden="true"></i>
                <p class="media-name">LinkedIn</p> 
              </b-link>
            </div>
            <div>
              <b-link class="row media-item"
                      href="https://github.com/tonyOP1985"
                      target="_blank">
                <i class="fa fa-github-square fa-2x" aria-hidden="true"></i>
                <p class="media-name">GitHub</p>
              </b-link>
            </div>
            <div>
              <b-link class="row media-item"
                      href="https://www.facebook.com/TonyOliverPaull"
                      target="_blank">
                <i class="fa fa-facebook-square fa-2x" aria-hidden="true"></i>
                <p class="media-name">Facebook</p>
              </b-link>
            </div>
            <div>
              <b-link to="/contact" class="row media-item">
                <i class="fa fa-envelope-square fa-2x" aria-hidden="true"></i>
                <p class="media-name">Contact</p>
              </b-link>
            </div>
          </div>
        </b-row>
      </section>
    </div>
  </div>
</template>

<script>
 /* eslint-disable */
export default {
  name: 'About'
}
</script>

<style scoped>
  .about-wrapper {
    min-height: 100%;
    padding-bottom: 46px;
  }

  .about {
    background-color: #f5f8fa; 
    padding-bottom: 10px;
    border-bottom: 1px solid rgba(0, 0, 0, 0.125);
  }

  img {
    margin: 20px;
  }

  .name > h1 {
    font-family: montserrat, sans-serif;
    text-transform: uppercase;
    letter-spacing: 1px;
    font-weight: 900;
  }

  .about-para > p {
    font-family: montserrat, sans-serif;
    font-size: 1.4rem;
  }

  .about-me {
    margin: 0 auto;
    padding: 40px 0;
    color: #2e2e2e;
  }

  .about-me-heading, .about-me-p {
    width: 100%;
    margin: 0 auto;
    color: rgba(0, 0, 0, 0.8);
  }

  .about-me-heading > h1 {
    font-size: 2rem;
    text-align: left;
  }

  .about-me-heading {
    margin-bottom: 20px;
  }

  .about-me-p {
    font-family: 'Merriweather', serif;
    line-height: 1.75rem; 
    text-align: left;
    font-size: 1rem;
    letter-spacing: 0.01rem;
  }

  p > a {
    color: rgb(0, 123, 255);
  }

  .media {
    display: flex;
    flex-direction: column;
    margin-left: 10px;
  }
  
  a {
    text-decoration: none;
    color: rgb(0, 0, 0);
  }

  .media-name {
    padding: 4px 0 0 5px;
  }

  a:hover {
    color: rgb(0, 86, 179);
  }
  
  .row {
    margin: 0 auto;
  }

  @media (max-width: 768px) {
    .about-me  {
      margin: 0 1px;
    }

    .media {
      margin: 0;
    }
  }

  @media (max-width: 500px) {
    .about-me {
      width: 100%;
    }

    .about-me-p > p {
      font-size: 0.8rem;
    }
 
    .name > h1 {
      font-size: 1.2rem;
    }

    .about-para > p {
      font-size: 1.1rem;
    }
  }
</style>