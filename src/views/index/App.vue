<!-- index -->
<template>
  <div class="index">
    <sicon name="welcome" scale="8.0"></sicon>
    <p>hello world</p>
    <p @click="change">测试vuex</p>
    <p>vuex中state的值：{{test.count}}</p>
    <ivew-test></ivew-test>
    <vuex-test></vuex-test>
  </div>
</template>

<script>
import { mapState, mapMutations   } from 'vuex'
import ivewTest from './components/iviewTest'
import vuexTest from './components/vuexTest'
export default {
  data () {
    return {
    };
  },

  components: {
    ivewTest,
    vuexTest
  },

  computed: {
    ...mapState([
      'test'
    ])
  },
  methods: {
    ...mapMutations ({
      change: 'changState'
    }),
  }

}

</script>

<style scoped lang="less">
.index{
  padding: 80px;
  text-align: center;
}
</style>