<template>
  <div id="wrapper">
    sdnofksod
    {{tableData[0].name}}
    <el-button type="primary">主要按钮</el-button>
    <el-table :data="tableData" style="width: 100% ;height: 100%">
      <el-table-column prop="date" label="日期" width="180"></el-table-column>
      <el-table-column prop="name" label="姓名" width="180"></el-table-column>
      <el-table-column prop="sex" label="性别" width="180"></el-table-column>
      <el-table-column prop="address" label="地址"></el-table-column>
    </el-table>

  </div>
</template>

<script>
  // "scripts": {
  //   "build": "node .electron-vue/build.js && electron-builder --platform=win32  --arch=ia32",
  //   "win32": "node .electron-vue/build.js && electron-builder --platform=win32  --arch=ia32",
  //   "mac": "node .electron-vue/build.js && electron-builder --platform=drwin ",
  //   "build:dir": "node .electron-vue/build.js && electron-builder --dir",
  //   "build:clean": "cross-env BUILD_TARGET=clean node .electron-vue/build.js",
  //   "build:web": "cross-env BUILD_TARGET=web node .electron-vue/build.js",
  //   "dev": "node .electron-vue/dev-runner.js",
  //   "e2e": "npm run pack && mocha test/e2e",
  //   "lint": "eslint --ext .js,.vue -f ./node_modules/eslint-friendly-formatter src test",
  //   "lint:fix": "eslint --ext .js,.vue -f ./node_modules/eslint-friendly-formatter --fix src test",
  //   "pack": "npm run pack:main && npm run pack:renderer",
  //   "pack:main": "cross-env NODE_ENV=production webpack --progress --colors --config .electron-vue/webpack.main.config.js",
  //   "pack:renderer": "cross-env NODE_ENV=production webpack --progress --colors --config .electron-vue/webpack.renderer.config.js",
  //   "test": "npm run unit && npm run e2e",
  //   "unit": "karma start test/unit/karma.conf.js",
  //   "postinstall": "npm run lint:fix"
  // },

  export default {
    data() {
      return {
        tableData: [{
          date: '2016-05-02',
          name: '王小虎',
          sex:"男",
          address: '上海市普陀区金沙江路 1518 弄'
        }, {
          date: '2016-05-04',
          name: '王小虎',
          sex:"女",
          address: '上海市普陀区金沙江路 1517 弄'
        }, {
          date: '2016-05-01',
          name: '王小虎',
          sex:"男",
          address: '上海市普陀区金沙江路 1519 弄'
        }, {
          date: '2016-05-03',
          name: '王小虎',
          sex:"女",
          address: '上海市普陀区金沙江路 1516 弄'
        }]
      }
    },



    methods: {
      open (link) {
        this.$electron.shell.openExternal(link)
      }
    }
  }
</script>

<style>
  @import url('https://fonts.googleapis.com/css?family=Source+Sans+Pro');

  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  body { font-family: 'Source Sans Pro', sans-serif; }

  #wrapper {
    background:
      radial-gradient(
        ellipse at top left,
        rgba(255, 255, 255, 1) 40%,
        rgba(229, 229, 229, .9) 100%
      );
    height: 100vh;
    padding: 60px 80px;
    width: 100vw;
  }

  #logo {
    height: auto;
    margin-bottom: 20px;
    width: 420px;
  }

  main {
    display: flex;
    justify-content: space-between;
  }

  main > div { flex-basis: 50%; }

  .left-side {
    display: flex;
    flex-direction: column;
  }

  .welcome {
    color: #555;
    font-size: 23px;
    margin-bottom: 10px;
  }

  .title {
    color: #2c3e50;
    font-size: 20px;
    font-weight: bold;
    margin-bottom: 6px;
  }

  .title.alt {
    font-size: 18px;
    margin-bottom: 10px;
  }

  .doc p {
    color: black;
    margin-bottom: 10px;
  }

  .doc button {
    font-size: .8em;
    cursor: pointer;
    outline: none;
    padding: 0.75em 2em;
    border-radius: 2em;
    display: inline-block;
    color: #fff;
    background-color: #4fc08d;
    transition: all 0.15s ease;
    box-sizing: border-box;
    border: 1px solid #4fc08d;
  }

  .doc button.alt {
    color: #42b983;
    background-color: transparent;
  }
</style>
