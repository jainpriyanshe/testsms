<template>
  <div class="container">
    <div>
      <Logo />
      <h1 class="title">
        sms
      </h1>
      <br />
      {{counter}} | {{counter123}}
      <button class="btn btn-sm btn-info" @click="storetest">Store test
      </button>

      </div>
    </div>
</template>

<script>
import { mapState,mapActions,mapGetters} from 'vuex'
export default {
  computed: {
    ...mapGetters('modules/crudAdmin',['counter','counter123']),

  },
  methods:{
    ...mapActions('modules/crudAdmin',['readdata']),
    storetest() {
      this.readData({test:'hello'})

    },
  },
  mounted() {
    
  },
}
</script>

<style>
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
