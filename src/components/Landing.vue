<template>
  <div class="landing">
    <h1>{{ msg }}</h1>
    
    <section class="about">
      <h2>About Me</h2>
        <ul>
          <li>Avid Traveler</li>
          <li>Based out of Denver, Colorado, USA</li>
          <li>Enjoys
            <span class="emoji">{{ randomEmoji }}</span>
          </li>
        </ul>
    </section>

  </div>
</template>

<script>
export default {
  name: 'Landing',
  props: {
    msg: String
  },
  data() {
    return {
      emojis: ["🍕", "🎸", "🎮"],
      randomEmoji: ""
    }
  },
  mounted() {
    this.randomize();
  },
  methods: {
    randomize() {
      this.randomEmoji = this.emojis[Math.floor(Math.random() * this.emojis.length)];
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
  padding: 0;
}
li {
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
