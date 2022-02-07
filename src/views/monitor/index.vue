<template>
  <div class="monitor">
    <button @click="clickHanld">click</button>
    <ul>
      <li v-for="item in liList" :key="item.id">{{ item.name }}</li>
    </ul>
  </div>
</template>

<script>
import hello from './testError.js'

export default {
  data() {
    return {
      a: 1,
      liList: [
        { id: 0, name: 'myy' },
        { id: 0, name: 'myy' }
      ]
    }
  },

  created() {
    hello()
  },
  computed: {
    str() {
      return this.a + 2
    }
  },

  methods: {
    clickHanld() {
      Promise.reject('test').then()
      // let script = document.createElement('script')
      // script.setAttribute('src', 'http://baidu.com/haha.js')
    }
  }
}
</script>