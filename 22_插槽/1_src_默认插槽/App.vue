<template>
  <div class="container">
    <Category title="美食">
      <img src="https://wx3.sinaimg.cn/mw690/007Zevv3ly1h0z3r1khzpj31900tzq7w.jpg" alt="">
    </Category>

    <Category title="游戏">
      <ul>
        <li v-for="(g, index) in games" :key="index">{{ g }}</li>
      </ul>
    </Category>

    <Category title="电影">
      <img src="https://wx2.sinaimg.cn/mw690/007Zevv3ly1h0z3r2tas4j31ht0u0ai3.jpg"></img>
    </Category>
  </div>
</template>

<script>
import Category from './components/Category'
export default {
  name:'App',
  components:{Category},
  data(){
    return {
      foods:['火锅', '烧烤', '小龙虾', '牛排'],
      games:['红色警戒', '穿越火线', '劲舞团', '超级玛丽'],
      films:['《教父》', '《拆弹专家》', '《你好，李焕英》', '《尚硅谷》']
    }
  }
}
</script>

<style>
  .container{
    display: flex;
    justify-content: space-around;
  }
</style>
