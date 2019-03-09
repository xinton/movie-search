<template>
  <div class="vertical-center">
    <div class="container">
      <div>
        <h1 class="display-3">Sallve Movies</h1>
      </div>
      <form>
        <div class="form-row align-items-center">
          <div class="col-md-10 col-sm-12">
            <input v-model="queryText" type="text" class="form-control" id="queryText" placeholder="Find a movie">
          </div>
          <div class="col-md-2 col-sm-12">
            <router-link :to="{path: '/search', query:{text: this.queryText}}">
              <button class="btn btn-primary">Search</button>
            </router-link>
          </div>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Index',
  data () {
    return {
      queryText: ''
    }
  }
}
</script>
<style lang="scss">

.container {
  text-align: center;
};

@media (max-width: 576px) {
  .col-sm-12 {
    margin-top: 20px;
  }

  .display-3 {
    font-size: 50px;
  }
};
</style>
