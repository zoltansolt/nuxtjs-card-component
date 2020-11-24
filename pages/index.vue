<template>
  <section class="cards">
    <Card 
    cover="/couch1.jpg"
    thumbnail="/couch1.jpg"
    title="Card 1"
    subTitle="Blablabla"
    text="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."
    footer="Card footer"
    @click.native="clicked"
    />

    <Card 
    cover="/couch2.jpg"
    thumbnail="/couch2.jpg"
    title="Card 2"
    @click.native="doNothing"
    />
    
    <Card 
    cover="/couch3.jpg"
    thumbnail="/couch3.jpg"
    title="Card 3"
    footer="footer"
    @click.native="redirect"
    />
    
    <Card 
    title="Card 4"
    subTitle="Blablabla"
    text="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."
    footer="Card footer"
    @click.native="doNothing"
    />
  </section>
</template>

<script>
import Card from '@/components/card';
export default {
  components: {
    Card
  },
  methods: {
    clicked: function(event) {
      console.log('hi!');
    },
    doNothing: function(event) {
    },
    redirect: function(event) {
      this.$router.push('1');
    }
  }
}
</script>

<style>

.cards {
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  align-items: center;
}

.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
