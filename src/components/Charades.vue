<template>
  <div class="charades" v-on:click="get_charade">
    <b>{{verb}}</b><br>{{noun}}
  </div>
</template>

<script>
export default {
  name: 'Charades',
  data: function() {
    return {
      verb: 'Click to pick a card',
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
.charades {
  background-color: #FF7;
  height: 350px;
  width: 250px;
  border-radius: 20px;
  display: table-cell;
  vertical-align: middle;
  border-width: 10px;
  border-color: #FF8E66;
  border-style: double;
  font-size: 1.5em;
}
</style>
