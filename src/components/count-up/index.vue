<template>
  <div id='card'>
    <div id='title' :style='titleStyle' @click="change">{{ title }}</div>
    <div id='number' :style='numberStyle'>
      <ICountUp
        :delay='delay'
        :endVal='endVal'
        :options='options'
      />
    </div>
  </div>
</template>

<script>
import ICountUp from 'vue-countup-v2'
export default {
  name: 'countup',
  components: {
    ICountUp
  },
  props: {
    title: {
      type: String,
      required: false,
      default: 'Countup'
    },
    delay: {
      type: Number,
      required: false,
      default: 1000
    },
    endVal: {
      type: Number,
      required: false,
      default: 100
    },
    options: {
      type: Object,
      required: false,
      default: function () {
        return {
          useEasing: true,
          useGrouping: true,
          separator: ',',
          decimal: '.',
          prefix: '',
          suffix: ''
        }
      }
    },
    mainTheme: {
      type: Object,
      require: false,
      default: function () {
        return ({
          hue: Math.floor(Math.random() * 360),
          sat: 20,
          ligh: 60
        })
      }
    }
  },
  methods: {
    change: function () {
      this.mainTheme.hue = (this.mainTheme.hue + Math.floor(50 + Math.random() * 50)) % 360
    },
    getColor: function ({ hue, sat, ligh }, offset) {
      return 'hsl(' + hue + ',' + (sat + offset) + '%,' + (ligh - offset) + '%)'
    }
  },
  data () {
    return ({
      color: '#4d63bc',
      titleColor: 'red',
      numberColor: 'green'
    })
  },
  computed: {
    titleStyle: function () {
      return {
        color: this.getColor(this.mainTheme, 10)
      }
    },
    numberStyle: function () {
      return {
        color: this.getColor(this.mainTheme, 0)
      }
    }
  }
}
</script>

<style>
.iCountUp {
  font-size: 5em;
  margin: 0;
  color: #4d63bc;
}
.div {
    background: #4d63bc;
}
#title {
  text-align: center;
}
#number {
  text-align: center;
  padding-top: 0.618em;
  font-size: 1.5em;
}
</style>
