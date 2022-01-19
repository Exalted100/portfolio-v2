<template>
  <Title title="Fawaz Haroun" />
  <p>
    I’m a web developer in Lagos, Nigeria, with a passion for smooth and easy to use UIs. Some things I like to do are reading, writing, drawing (bad art), and learning things that momentarily catch my interest. I strongly believe in growth - and putting yourself in positions that force growth. Much like learning to swim by jumping into water or learning to drive by grabbing a steering wheel, after preparing your best to avoid drowning or crashing. George Brecht said “the whole universe interests me”. I share the sentiment, except that I have realized building things interests me above all.
  </p>

  <Title title="Selected Works" />
  <SelectedList v-for="item in works" v-bind:item="item" v-bind:key="item.link" />

  <Title title="Selected Articles" />
  <SelectedList v-for="item in articles" v-bind:item="item" v-bind:key="item.link" />

  <Title title="Contact me" />
  <Contacts v-for="contact in contacts" v-bind:contact="contact" v-bind:key="contact.link" />

  <p id="copyright">
    &#169; Fawaz Haroun, {{ new Date().getFullYear() }}
  </p>
</template>

<script>
import Title from './components/Title.vue'
import SelectedList from './components/SelectedList.vue'
import Contacts from "./components/Contacts.vue"
import contacts from "./assets/contacts"
import works from "./assets/works"
import articles from "./assets/articles"

export default {
  name: 'App',
  components: {
    Title,
    SelectedList,
    Contacts
  },
  data() {
    return {
      works: works,
      articles: articles,
      contacts: contacts
    }
  }
}
</script>

<style>
*, *::before, *::after {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  box-sizing: border-box;
  padding: 0;
  margin: 0;
  max-width: 100%;
}

@font-face { font-family: Raleway; 
  src: url('./assets/Raleway/static/Raleway-Regular.ttf'); 
}

@font-face { font-family: Raleway-Bold; 
  src: url('./assets/Raleway/static/Raleway-Bold.ttf'); 
}

#app {
  font-family: Raleway, Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  background-color: #FFD2A8;
  padding: 0 50px;
}

p {
  font-size: 30px;
}

#copyright {
  margin-top: 100px;
}

@media only screen and (max-width: 600px) {
  #app {
    padding: 0 20px
  }
}
</style>
