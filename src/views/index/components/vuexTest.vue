<!--  -->
<template>
  <div>
    <p>vuex测试：vuex中test的值{{test.count}}</p>
    <p></p>
  </div>
</template>

<script>
import { mapState   } from 'vuex'
export default {
  data () {
    return {
    };
  },

  components: {},

  computed: {
    ...mapState([
      'test'
    ])
  },

}

</script>

<style scoped>
</style>