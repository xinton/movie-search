<template>
  <div>
    <span>aq</span>
    <img :src="movie.Poster" alt="Movie Poster">
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
      const response = await this.$http.get('', {params: {t: queryText, apikey: '1bdf27a'}})
      return response.data
    }
  },
  async mounted () {
    this.movie = await this.query()
  }
}
</script>
<style lang="scss">
</style>
