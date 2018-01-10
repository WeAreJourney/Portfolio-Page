<template>
  <div class="main">
    <header>
      <div class="title">
        <h1>Projects</h1>
      </div>
    </header>
      <div class="wrapper">
      <div class="projects" v-for="info in cardInfo">
        <b-card :title="info.title"
          :img-src="info.image"
          :img-alt="info.alt"
          img-top
          img-fluid
          tag="article"
          >
          <div>
            <p class="card-text">
              {{ info.text }}
            </p>
            <ul class="tech-list">
              <li v-for="tech in info.technology">
                <span>{{ tech }}</span>
              </li>
            </ul>
          </div>
          <b-button :href="info.projectLink" target="_blank" variant="primary">View Project</b-button>
          <b-button href="#" variant="primary">View Code</b-button>
        </b-card>
      </div>
    </div>
</div>

</template>

<script>
/* eslint-disable */
export default {
  name: 'projects',
  data () {
    return {
      cardInfo: [
        {
          image: '../../static/images/tonyProjectImg.png',
          title: 'Tony Oliver-Paull',
          text: 'Portfolio page.',
          alt: 'Tony Oliver-Paull',
          technology: ['Vue.js', 'Vue-router', 'Bootstrap-Vue', 'Nodemailer', 'Express.js'],
          projectLink: '#'
        },
        {
          image: '../../static/images/cloudy-day.svg',
          title: 'Weather App',
          text: 'Simple weather app.',
          alt: 'Weather App Cloud Icon',
          technology: ['Vue.js', 'Darksky API', 'Google Maps Geocoding API', 'Express.js'],
          projectLink: 'https://localweatherapp-tonyop.herokuapp.com/'
        },
        {
          image: '../../static/images/sailor-moon.jpg',
          title: 'Sailor Moon Game',
          text: 'Game based off of the Japanese anime.',
          alt: 'Sailor Moon',
          technology: ['Vue.js', 'Express.js'],
          projectLink: '#'
        },
        {
          image: '../../static/images/indecisionApp.png',
          title: 'Indecision App',
          text: 'Very first Vue.js app. Todo list that decides for you.',
          alt: 'Indecision App',
          technology: ['Vue.js'],
          projectLink: 'https://obscure-wave-95185.herokuapp.com/'
        },
        {
          image: '../../static/images/hangManThumbNail.png',
          title: 'Hang Man',
          text: 'Hang Man game with astronomy terms.',
          alt: 'Hang man image',
          technology: ['Javascript', 'jQuery', 'HTML', 'CSS', 'Express.js'],
          projectLink: 'https://ancient-journey-60616.herokuapp.com/'
        }
      ]
    }
  }
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

  img {
    width: 286px;
    height: 176.292px;
  }

  .title {
    width: 50%;
    margin: 0 auto;
    padding-top: 40px;
    text-align: center;
  }

  .title > h1 {
    color: #3A4145;
    font-family: montserrat, sans-serif;
    text-transform: uppercase;
    letter-spacing: 0.2rem;
    font-weight: 900;
  }

  article {
    height: 481.625px;
    width: 18rem;
    margin: 0;
  }

  img {
    height: 171px;
  }

  p {
    height: 50px;
    font-size: 1.1rem;
  }

  ul {
    height: 107px;
  }

  .wrapper {
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    margin: 0 auto;
  }

  .projects {
    width: 322px;
    margin-top: 20px;
  }

  .card {
    margin: 20px 0;
  }

  .btn {
    width: 113px;
  }

  .tech-list {
    text-align: left;
    font-size: 0.9rem;
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

    ul, p {
      height: auto;
    }

    article {
      width: 246px;
      height: auto;
    }

    .card {
      margin: 20px auto;
    }

    img {
      width: 246px;
      height: 150px;
    }

    .card-body {
      padding: 20px 0;
    }
  }
</style>