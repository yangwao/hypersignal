<template>
  <div class="page">
    <p>
      <a href="http://hypersignal.xyz">hypersignal.xyz</a>
    </p>
    <div id="map">
      <simple></simple>
    </div>
  </div>

</template>

<script>
import Counter from 'components/Counter'
import Simple from 'components/Simple'

export default {
  name: 'app',
  components: {
    Counter,
    Simple
  },
  data () {
    return {
      currentView: 'simple'
    }
  }
}
</script>

<style>
#map {
  display: table;
  margin: 0 auto;
  width: 50%;
}

#map-inner {
  position: absolute;
  width: 400px
}
</style>
