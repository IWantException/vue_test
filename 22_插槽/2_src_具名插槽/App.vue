<template>
  <div class="container">
    <Category title="美食">
      <img slot="center" src="https://wx3.sinaimg.cn/mw690/007Zevv3ly1h0z3r1khzpj31900tzq7w.jpg" alt="">
      <a slot="footer" class="foot" href="http://atguigu.com">更多美食</a>
    </Category>

    <Category title="游戏">
      <ul slot="center">
        <li v-for="(g, index) in games" :key="index">{{ g }}</li>
      </ul>
      <div class="foot" slot="footer">
        <a href="http://atguigu.com">单击游戏</a>
        <a href="http://atguigu.com">网络游戏</a>
      </div>
    </Category>

    <Category title="电影">
      <img slot="center" src="https://wx2.sinaimg.cn/mw690/007Zevv3ly1h0z3r2tas4j31ht0u0ai3.jpg"></img>
      <template v-slot:footer>
        <div class="foot">
          <a href="http://atguigu.com">经典</a>
          <a href="http://atguigu.com">热门</a>
          <a href="http://atguigu.com">推荐</a>
        </div>
        <h4>欢迎前来观影</h4>
      </template>
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
  .container, .foot{
    display: flex;
    justify-content: space-around;
  }

  h4{
    text-align: center;
  }
</style>
