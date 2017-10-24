<template>
  <!-- 头部模块 -->
  <header>
    <div class="container">
      <!-- 公司图标 -->
      <h1>
        <a href="index.html" class="logo" title="亿嘉和科技股份有限公司,打造面向未来智慧的公司">
          亿嘉和科技股份有限公司
        </a>
      </h1>
      <!-- 导航菜单 -->
      <div class="menu-list">
        <div class="nav-box">
          <a href="index.html" class="firstmenu">首页</a>
        </div>
        <div class="nav-box toggle-nav">
          <a href="javascript:void(0);" class="firstmenu">
            关于亿嘉和
          </a>
          <!-- 二级菜单 -->
          <ul class="child">
            <li>
              <div class="container">
                <span v-for="item in aboutcom">
                  <a href="#">{{ item }}</a>
                </span>
              </div>
            </li>
          </ul>
        </div>
        <div class="nav-box toggle-nav">
          <a href="javascript:void(0);" class="firstmenu">智能机器人</a>
          <!-- 二级菜单 -->
          <ul class="child">
            <li>
              <div class="container">
                <dl v-for="arr in robot">
                  <dt>
                    {{ arr.name }}
                  </dt>
                  <dd v-for="list in arr.items">
                    <a href="#">{{ list }}</a>
                  </dd>
                </dl>
              </div>
            </li>
          </ul>
        </div>
        <div class="nav-box">
          <a href="javascript:void(0);" class="firstmenu">智能运维服务</a>
        </div>
        <div class="nav-box">
          <a href="javascript:void(0);" class="firstmenu">智能软件系统</a>
        </div>
        <div class="nav-box">
          <a href="javascript:void(0);" class="firstmenu">服务支持</a>
        </div>
        <div class="nav-box toggle-nav">
          <a href="javascript:void(0);" class="firstmenu cicon-sea">搜索</a>
          <!-- 二级菜单 -->
          <ul class="child">
            <li>
              <div class="container">
                <input type="text" class="stxt" placeholder="输入关键词搜索">
                <button class="sbtn">开始搜索</button>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
  export default {
    data() {
      return {
        aboutcom: ['公司介绍','组织架构','企业文化','资质荣誉','公司新闻','人才招聘','联系我们'],
        robot: [
          {
            name: '医疗行业',
            items: [
              '智能药柜',
              '快速发药系统',
              '康复/护理机器人'
            ]
          },
          {
            name: '电力行业',
            items: [
              '变电站、换流站巡检机器人',
              '配电站所巡检机器人',
              '电力清洁机器人',
              '智能巡检无人机'
            ]
          },
          {
            name: '先进制造',
            items: [
              '搬运、码垛机器人',
              '工业AGV产品',
              '智能仓储产品',
              '定制化智能设备'
            ]
          },
          {
            name: '石油、石化及市政工程',
            items: [
              '管道检测机器人',
              '房屋检测机器人',
              '隧道智能检测机器人',
              '消防机器人（火探）'
            ]
          },
          {
            name: '其他行业',
            items: [
              '餐厅、商超服务机器人',
              '核辐射环境下救援机器人',
              '战场救护机器人',
              '教育/科研机器人'
            ]
          }
        ]
      };
    },
  };
</script>

<style>
header{
  position: fixed;
  z-index: 999;
  height: 80px;
  background: #fff;
  width: 100%;
}
a{
  text-decoration: none;
}
.container{
  margin: 0 auto;
  padding: 0 12px;
  width: 100%;
  max-width: 1224px;
  min-width: 1024px;
}
.container h1{
  float: left;
  margin: 0;
  padding: 15px 0;
}
.container h1 a.logo{
  display: block;
  width: 140px;
  height: 50px;
  text-indent: -8889px;
  background: url(../../assets/menu/company-logo.png) no-repeat center;
  background-size: 140px 50px;
}
.menu-list{
  float: right;
}
.menu-list .nav-box{
  float: left;
  padding: 0 18px;
}
.menu-list .nav-box a:hover {
  color: #035cac;
}
.firstmenu{
  display: block;
  font-size: 110%;
  line-height: 80px;
  color: #121212;
  text-decoration: none;
}
.menu-list .nav-box ul{
  list-style: none;
  position: absolute;
  top: 63px;
  left: 0;
  width: 100%;
  height: auto;
  background: rgba(255,255,255,.98);
  border-top: 1px solid #f0f0f0;
}
.menu-list .nav-box ul li {
  float: left;
  width: 100%;
  text-align: center;
}
.menu-list .nav-box ul li span {
  display: inline-block;
  padding: 0 18px;
}
.nav-box ul li span a{
  display: inline-block;
  color: #666;
  font-size: 100%;
  line-height: 1.75;
  text-align: center;
}
.cicon-sea {
  margin: 18px 0;
  display: block;
  width: 44px;
  height: 44px;
  text-indent: -8889px;
  background: url(../../assets/menu/search.png) no-repeat 0px 0px;
  background-size: 44px;
  transition: background 0.5s;
  -moz-transition: background 0.5s; /* Firefox 4 */
  -webkit-transition: background 0.5s; /* Safari and Chrome */
  -o-transition: background 0.5s; /* Opera */
}
.cicon-sea:hover {
  background: url(../../assets/menu/search.png) no-repeat 0px -44px;
  background-size: 44px;
}
.child{
  display: none;
  transition: display 2s;
  -moz-transition: display 2s; /* Firefox 4 */
  -webkit-transition: display 2s; /* Safari and Chrome */
  -o-transition: display 2s; /* Opera */
}
.toggle-nav:hover .child{
  display: block;
}
.nav-box ul li {
  float: left;
  width: 100%;
  text-align: center;
  padding: 24px 0;
}
.nav-box ul li span {
    display: inline-block;
    padding: 0 18px;
}
.nav-box ul li dl {
  float: left;
  width: 20%;
  text-align: left;
  font-size: 14px;
}
.nav-box ul li dl dt {
  font-size: 110%;
  padding: 2px 12px;
  font-weight: 600;
  color: #035cac;
}
.nav-box ul li dl dd {
  padding: 2px 12px;
  margin-left: 0px;
}
.nav-box ul li dl dd a{
  display: inline-block;
  color: #666;
  font-size: 110%;
  line-height: 2.75;
  text-align: center;
}
.stxt {
  vertical-align: middle;
  padding: 12px;
  width: 55%;
  background: #fff;
  height: 50px;
  border: 1px solid #ccc;
  font-family: "Microsoft Yahei","Hiragino Sans GB",sans-serif;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
}
.sbtn {
  vertical-align: middle;
  border: 0;
  background: #035cac;
  color: #fff;
  padding: 0 30px;
  font-size: 110%;
  height: 50px;
  font-family: "Microsoft Yahei","Hiragino Sans GB",sans-serif;
}
</style>
