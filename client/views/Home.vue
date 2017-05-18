<template>
  <div class="page">
    <vue-markdown> ## Want to learn 🔭 </vue-markdown>
    <vue-markdown>  ES7, ES8, ES9...
                    GraphQL
                    Serverless frameworks ( i.e. https://stdlib.com/ )
                    NLP, Tensorflow
                    More distributed technologies (SSB, Kappa Arch, Hyperlog, IPFS,...)
                    MerkleDag approach, Hyperlog
                    GoLang
    </vue-markdown>
    <vue-markdown> ## 💬 Reach & follow me 🐈 </vue-markdown>

    <vue-markdown> My Scuttlebutt/Patchwork true name is @NaDXehMSIgk08W5RXZJ0p+7m+19iIWEuAtD7FRESJX8=.ed25519
                   [twitter.com/yangwao](https://twitter.com/yangwao)
                   [github.com/yangwao](https://github.com/yangwao)
                   [facebook.com/matej.wao.nemcek](https://www.facebook.com/matej.wao.nemcek)
                   [linkedin.com/in/mnemcek](https://sk.linkedin.com/in/mnemcek)
                   [instagram.com/yangwao/](https://www.instagram.com/yangwao)
                   My miniLock ID: 2A8Y2hLRMYgMWxJ9rqFeMsTMn8ppCUzA4TQCumvG9CuQr8 (learn at minilock.io)
                   ⫸  emojilock
                   ⚽️🐋👉🔋🔮💰👆⭐️✂️📌🐗🚡🎮⌛️😭🍇🐚🚧🍫😎🚥💉🎨🔉👰➡️👫🌽🔨📼🏀👽
                   I'm no longer using PGP.
    </vue-markdown>
    <p>
      <a href="http://hypersignal.xyz">hypersignal.xyz</a>
    </p>
    <p>
      Site was born
      {{ moment(born).fromNow() }}
    </p>
    <div id="map">
      <leafletbratislava></leafletbratislava>
    </div>
  </div>

</template>

<script>
import Counter from 'components/Counter'
import leafletbratislava from 'components/leaflet-bratislava'
import moment from 'moment'
import VueMarkdown from 'vue-markdown'

const now = new Date().getTime()
const born = [2017, 0, 23, 23, 59]
const time = now - 300000

export default {
  name: 'app',
  components: {
    Counter,
    leafletbratislava,
    VueMarkdown
  },
  data () {
    return {
      currentView: 'simple',
      currentLang: 'en-US',
      moment: moment,
      born
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
