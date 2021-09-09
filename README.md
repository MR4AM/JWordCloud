# JWordCloud
- 3D JavaScript 词云,可自定义词云词语颜色和自带3d环绕效果
- 欢迎使用JWordCloud, 如果觉得好用，给个star！

## 如何使用JWordCloud
- 1.引入JWordCloud.js
- 2.在词云区域实例化JWordCloud
  
## JWordCloud 使用示例代码
- use in broswer
```
<script type="text/javascript" src="./src/js/JWordCloud.js"></script>
<script>
      var words = {
          'JWordCloud': 101,
          '3d':42,
          'JavaScript': 23,
          'CSS3':45,
          'Animation': 109,
          'React': 56,
          'Vue': 78,
          'Jvue': 107,
          'App': 118,
          'Web': 109,
          'Html5': 67,
          'Java': 69
      }
      var wordCloud = new JWordCloud('.content', words, {
          // 词云渲染区域大小
          radius: 300,
          // 词云动画速度模式 slow, normal, fast
          maxSpeed: 'normal',
          initSpeed: 'normal',
          // 词云颜色板
          colors: ['red','blue','orange','green','purple', 'yellow','skyblue','#673ab7','#3f51b5','#ff5722','#607d8b'],
          // 词云标准值字体大小
          fontSize: 28
      });
  </script>
```

- Use in Vue
- npm i jwordcloud --save --dev
```
<template>
  <div class="content"></div>
</template>
<script>
import JWordCloud from "jwordcloud";
import Vue from "vue";
Vue.use(JWordCloud);
export default {
  /*
    变量装载
  */
  data() {
    return {
      isVisible: false
    };
  },
  /*
    组件声明
  */
  components: {
    // BstCanlendar
  },
  /*
    页面挂载
  */
  mounted() {
    var words = {
      JWordCloud: 101,
      "3d": 42,
      JavaScript: 23,
      CSS3: 45,
      Animation: 109,
      React: 56,
      Vue: 78,
      Jvue: 107,
      App: 118,
      Web: 109,
      Html5: 67,
      Java: 69
    };
    new JWordCloud(".content", words, {
      // 词云渲染区域大小
      radius: 300,
      // 词云动画速度模式 slow, normal, fast
      maxSpeed: "normal",
      initSpeed: "normal",
      // 词云颜色板
      colors: [
        "red",
        "blue",
        "orange",
        "green",
        "purple",
        "yellow",
        "skyblue",
        "#673ab7",
        "#3f51b5",
        "#ff5722",
        "#607d8b"
      ],
      // 词云标准值字体大小
      fontSize: 28
    });
  },
  /*
    页面摧毁
  */
  destroyed() {},
  /*
    执行方法
  */
  methods: {}
};
</script>
<style scoped>
  .content {
    background: rgba(0,0,0,0.9);
    height: 100%;
    display: flex; 
    align-items: center;
    justify-content: center;
  }
</style>

```
[最终效果](http://www.jasonlee.top/public/webs/wordCloud.gif)