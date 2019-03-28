<template>
  <div class="hello">
    <h3>只读，不显示数字：</h3>
    <my-rate :score="1.5" :disabled="true"/>
    <h3>只读，显示数字：</h3>
    <my-rate :score="3.6" :disabled="true" showText/>
    <h3>鼠标点击评分,显示数字：</h3>
    <my-rate :score.sync="curScore" showText/>
  </div>
</template>

<script>
import MyRate from './rater'
export default {
  name: 'HelloWorld',
  components: {
    MyRate
  },
  data () {
    return {
      curScore: 0
    }
  },
  methods: {
    // 提交显示分数
    submit () {
      alert(this.curScore)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
