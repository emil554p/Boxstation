<template>
  <div id="app">


      <nav class="navbar navbar-expand-lg navbar-dark bg-dark p-3 mb-5">
          <a class="h2 navbar-brand" href="#">Boxstation</a>

          <div class="collapse navbar-collapse justify-content-end" id="navbarSupportedContent">
              <ul class="navbar-nav d-flex">
                  <li class="nav-item align-self-center active">
                      <a class="nav-link h4 pr-5" href="#">Betaling<span class="sr-only">(current)</span></a>
                  </li>
                  <li class="nav-item align-self-center ">
                      <a class="nav-link h4 pr-5" href="#">Kapacitet</a>
                  </li>
                  <li class="nav-item align-self-center ">
                      <a class="nav-link h4 pr-5" href="#">Kunder</a>
                  </li>
                  <li>
                      <a class="nav-link h1 pr-5"><i class="nav item far fa-user text-light"></i></a>
                  </li>
                  <li>
                      <a class="nav-link h1 pr-5"><i class="nav item fas fa-search text-light"></i></a>
                  </li>


              </ul>
          </div>
      </nav>

      <div class="row p-5">
          <ul class="nav nav-tabs mt-5 col-8">
              <li class="nav-item">
                  <a class="nav-link bg-dark text-light" href="#">Nordhavn</a>
              </li>
              <li class="nav-item">
                  <a class="nav-link active" href="#">Herlev</a>
              </li>
              <li class="nav-item">
                  <a class="nav-link bg-dark text-light" href="#">Odense</a>
              </li>
          </ul>

          <div class="col-4 flex-column">
                  <div class="card mb-5 ">
                      <div class="card-header bg-dark text-light">
                          Statistik - Odense
                      </div>
                      <div class="row">
                      <ul class="list-group list-group-flush col-5">
                          <li class="list-group-item border-0">Udlejet</li>
                          <li class="list-group-item border-0">Reserveret</li>
                          <li class="list-group-item border-0">Opsagte</li>
                          <li class="list-group-item border-0">Ledige</li>
                      </ul>
                          <ul class="list-group list-group-flush col-4">
                              <li class="list-group-item border-0 w-100 bg-dark mt-3"> </li>
                              <li class="list-group-item border-0 w-100 bg-dark mt-3"></li>
                              <li class="list-group-item border-0 w-100 bg-dark mt-3"></li>
                              <li class="list-group-item border-0 w-100 bg-dark mt-3"></li>
                          </ul>
                          <ul class="list-group list-group-flush col-3">
                              <li class="list-group-item border-0">60%</li>
                              <li class="list-group-item border-0">10%</li>
                              <li class="list-group-item border-0">15%</li>
                              <li class="list-group-item border-0">15%</li>
                          </ul>
                     </div>
                  </div>
                  <div class="card">
                      <div class="card-header bg-dark text-light">
                          Samlet statistik
                      </div>
                      <div class="row">
                          <ul class="list-group list-group-flush col-5">
                              <li class="list-group-item border-0">Udlejet</li>
                              <li class="list-group-item border-0">Reserveret</li>
                              <li class="list-group-item border-0">Opsagte</li>
                              <li class="list-group-item border-0">Ledige</li>
                          </ul>
                          <ul class="list-group list-group-flush col-4">
                              <li class="list-group-item border-0 w-100 bg-dark mt-3"></li>
                              <li class="list-group-item border-0 w-100 bg-dark mt-3"></li>
                              <li class="list-group-item border-0 w-100 bg-dark mt-3"></li>
                              <li class="list-group-item border-0 w-100 bg-dark mt-3"></li>
                          </ul>
                          <ul class="list-group list-group-flush col-3">
                              <li class="list-group-item border-0">60%</li>
                              <li class="list-group-item border-0">10%</li>
                              <li class="list-group-item border-0">15%</li>
                              <li class="list-group-item border-0">15%</li>
                          </ul>
                      </div>
                  </div>
          </div>
      </div>


  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
  },
  data() {
    return {
      form: {
        email: '',
        name: '',
        food: null,
        checked: []
      },
      foods: [{ text: 'Select One', value: null }, 'Carrots', 'Beans', 'Tomatoes', 'Corn'],
      show: true
    }
  },
  methods: {
    onSubmit(evt) {
      evt.preventDefault()
      alert(JSON.stringify(this.form))
    },
    onReset(evt) {
      evt.preventDefault()
      // Reset our form values
      this.form.email = ''
      this.form.name = ''
      this.form.food = null
      this.form.checked = []
      // Trick to reset/clear native browser form validation state
      this.show = false
      this.$nextTick(() => {
        this.show = true
      })
    }
  }


}
</script>

<style>

</style>
