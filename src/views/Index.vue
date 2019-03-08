<template>
  <div class="vertical-center">
    <div class="container">
      <div>
        <h1 class="display-3">Sallve Movies</h1>
      </div>
      <form>
        <div class="form-row align-items-center">
          <div class="col-md-10 col-sm-12">
            <input type="text" class="form-control" id="queryText" placeholder="Find a movie">
          </div>
          <div class="col-md-2 col-sm-12">
            <button type="submit" class="btn btn-primary">Search</button>
          </div>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Index'
}
</script>

<style>
.vertical-center {
  min-height: 100%; /* Fallback for browsers do NOT support vh unit */
  min-height: 100vh; /* These two lines are counted as one :-)       */

  display: flex;
  align-items: center;
}
@media (max-width: 576px) {
  .col-sm-12 {
    margin-top: 20px;
  }

  .display-3 {
    font-size: 50px;
  }
}
</style>
