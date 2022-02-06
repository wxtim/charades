<template>
  <div class="charades">
    <button v-on:click="get_charade">Get a new Charade</button>
    <p>
    {{verb}} {{noun}}
    </p>
  </div>
</template>

<script>
export default {
  name: 'Charades',
  data: function() {
    return {
      verb: 'Charade: ',
      noun: '',
      films: require('../assets/films.json'),
      books: require('../assets/books.json')
    }
  },
  methods: {
    get_charade: function() {
      const nouns = this.films.concat(this.books)
      const verbs = ["Charade: ", "Sketch: ", "Sculpt: "]
      this.noun = nouns[Math.floor(Math.random() * nouns.length)]
      this.verb = verbs[Math.floor(Math.random() * verbs.length)]

    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
