<template>
  <div class="parent">
    <div class="movie-name">
      <span>movie name</span>
    </div>
    <div class="back-button">
      <button>teste</button>
    </div>
    <div class="release-genre-infos">
      <span>release date - genre</span>
    </div>
    <div class="awards">
      <span>awards</span>
    </div>
    <div>
      <img :src="movie.Poster" alt="Movie Poster">
    </div>
  </div>
</template>
<script>
export default {
  name: 'Details',
  data () {
    return {
      movie: {}
    }
  },
  methods: {
    async query () {
      let queryText = this.$route.query.text
      const response = await this.$http.get('', {
        params: { t: queryText, apikey: '1bdf27a' }
      })
      return response.data
    }
  },
  async mounted () {
    this.movie = await this.query()
  }
}
</script>
<style>
.back-button, .movie-name, .release-genre-infos, .awards {
  width: 50%;
  display:inline-block;
}

.movie-name, .awards {
  float: left;
}

@media screen and (max-width: 576px) {
  .parent {
    display: flex;
    flex-flow: column;
  }

  .back-button {
    order: 12;
  }

  .movie-name {
    display: block;
  }
}
</style>
