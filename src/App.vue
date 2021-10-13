<template>
  <div id="app">
    <Header/>
    <Main :sections="sections" :serviceList="serviceList" :companyValues="companyValues" :companyProjects="companyProjects"/>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';

export default {
  name: 'App',
  components: {
    Header,
    Main
  },
  data() {
    return {
      sections: ['home', 'services', 'about', 'projects', 'results'],
      serviceList: [
        {
          name: 'Audit & Assurance',
          icon: 'svg-1.svg',
          info: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.'
        },
        {
          name: 'Financial Advisory',
          icon: 'svg-2.svg',
          info: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.'
        },
        {
          name: 'Analytics and M&A',
          icon: 'svg-3.svg',
          info: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.'
        },
        {
          name: 'Middle Marketing',
          icon: 'svg-4.svg',
          info: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.'
        },
        {
          name: 'Legal Consulting',
          icon: 'svg-5.svg',
          info: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.'
        },
        {
          name: 'Regular Risk',
          icon: 'svg-6.svg',
          info: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.'
        },
      ],
      companyValues: [
        {
          title: 'Tradition',
          icon: 'fas fa-award',
          info: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.'
        },
        {
          title: 'Security',
          icon: 'fas fa-lock',
          info: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.'
        },
        {
          title: 'Certificate',
          icon: 'far fa-edit',
          info: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.'
        },
        {
          title: 'Expertise',
          icon: 'fas fa-graduation-cap',
          info: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.'
        }
      ],
      companyProjects: [
        {
          title: 'Academic professional program in social media',
          image: 'project-1.jpg',
          paragraph: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.',
          category: 'social'
        },
        {
          title: 'President\'s speech at the annual meeteng',
          image: 'project-2.jpg',
          paragraph: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.',
          category: 'institutional'
        },
        {
          title: 'International buisness trip to Shangai',
          image: 'project-3.jpg',
          paragraph: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.',
          category: 'events'
        },
        {
          title: 'Technology workshop with education theme',
          image: 'project-4.jpg',
          paragraph: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.',
          category: 'thecnology'
        },
        {
          title: 'Donation of clothes and food to the partner NGO',
          image: 'project-5.jpg',
          paragraph: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.',
          category: 'enironment'
        },
        {
          title: 'Confraternization of the procurement team',
          image: 'project-6.jpg',
          paragraph: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.',
          category: 'innovation'
        }
      ]
    }
  }
}
</script>

<style lang="scss">
@import './assets/style/common.scss';
@import '~@fortawesome/fontawesome-free/css/all.css';

</style>
