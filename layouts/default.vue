<template>
  <div id="blog-box">
    <div id="blog-header" class="blog-header clear-fix default-border-radius" >
      <div class="logo-box float-left">
        <div class="logo">
          黄豆芽博客
        </div>
      </div>
      <div class="login-tips-text-box float-right" v-if="isShow==='noLogin'" >
        <a :href="'/login'+redirectPath">
          <span><i class="sob_blog sobfingermap "></i> 登录</span>
        </a>
        <a :href="'/register?keyword=register'">
          <span><i class="sob_blog sobmembers-add "></i> 注册</span>
        </a>
      </div>
      <div class="login-tips-text-box float-right" v-if="isShow==='login'" >
        <a :href="'/userInfo/'">
          <span>个人中心</span>
        </a>
        |
        <a href="http://mp.huangdouya.group/#/dashboard" v-if="roles==='role_admin'">
          <span>后台管理</span>
        </a>
        <a  v-else>
          <span style="color: #8A8A8A">后台管理</span>
        </a>
      </div>
      <div class="navigation-box float-right">
          <a href="/">
            <span><i class="sob_blog sobhome "></i> 首页</span>
          </a>
          <a href="/link">
            <span><i class="sob_blog soblink "></i> 友链</span>
          </a>
          <a href="/about">
            <span><i class="sob_blog sobabout_line  "></i> 关于</span>
         </a>
      </div>
    </div>
    <!-- 中间部分-->
    <Nuxt/>
    <div class="blog-footer">
      <div>
        <a href="/about">
          <span>关于我们</span>
        </a>
        |
        <a href="/about">
          <span>联系我们</span>
        </a>
        |
        <a href="/link">
          <span>友情链接</span>
        </a>
        |
        <a href="http://www.beian.gov.cn/portal/registerSystemInfo?recordcode=44060502002344" target='_BLANK'>
          <span>粤ICP备2020117959号</span>
        </a>
      </div>
      <div class="copy-right-box">
        <p>
          Copyright @
          <a href="https:www.sunofbeach.net" target="_blank">
            阳光沙滩
          </a>
          （2019-2020）本网站仅供学习所用
        </p>
      </div>
    </div>
    <div id="g-to-top" style="display: none" @click="toTop()">
      <div class="el-icon-caret-top" ></div>
      <div>回到<br>顶部</div>
    </div>
    <div class="deng-box">
      <div class="deng">
        <div class="xian"></div>
        <div class="deng-a">
          <div class="deng-b"><div class="deng-t">新年</div></div>
        </div>
        <div class="shui shui-a"><div class="shui-c"></div><div class="shui-b"></div></div>
      </div>
    </div>
    <div class="deng-box1">
      <div class="deng">
        <div class="xian"></div>
        <div class="deng-a">
          <div class="deng-b"><div class="deng-t">快乐</div></div>
        </div>
        <div class="shui shui-a"><div class="shui-c"></div><div class="shui-b"></div></div>
      </div>
    </div>
  </div>
</template>

<script>
  import * as api from "../api/api"
  export default {
    data(){
      return{
        isShow:'noLogin',
        roles:'role_normal',
        redirectPath:'',
        userInfo:[]
      }
    },
    mounted() {
      this.textLogin()

      if(this.redirectPath!=='?redirect='+location.href&&
         this.$route.path!=='/' &&
         this.$route.path!=='/login'&&
        this.$route.path!=='/register'){
        this.redirectPath='?redirect='+location.href;
      }

      window.addEventListener('scroll',this.onWindowScroll)




      !function() {
          function n(n, e, t) {
            return n.getAttribute(e) || t
          }
          function e(n) {
            return document.getElementsByTagName(n)
          }
          function t() {
            var t = e("script"),
              o = t.length,
              i = t[o - 1];
            return {
              l: o,
              z: n(i, "zIndex", -1),
              o: n(i, "opacity", .5),
              c: n(i, "color", "0,0,0"),
              n: n(i, "count", 99)
            }
          }
          function o() {
            a = m.width = window.innerWidth || document.documentElement.clientWidth || document.body.clientWidth,
              c = m.height = window.innerHeight || document.documentElement.clientHeight || document.body.clientHeight
          }
          function i() {
            r.clearRect(0, 0, a, c);
            var n, e, t, o, m, l;
            s.forEach(function(i, x) {
              for (i.x += i.xa, i.y += i.ya, i.xa *= i.x > a || i.x < 0 ? -1 : 1, i.ya *= i.y > c || i.y < 0 ? -1 : 1, r.fillRect(i.x - .5, i.y - .5, 1, 1), e = x + 1; e < u.length; e++) n = u[e],
              null !== n.x && null !== n.y && (o = i.x - n.x, m = i.y - n.y, l = o * o + m * m, l < n.max && (n === y && l >= n.max / 2 && (i.x -= .03 * o, i.y -= .03 * m), t = (n.max - l) / n.max, r.beginPath(), r.lineWidth = t / 2, r.strokeStyle = "rgba(" + d.c + "," + (t + .2) + ")", r.moveTo(i.x, i.y), r.lineTo(n.x, n.y), r.stroke()))
            }),
              x(i)
          }
          var a, c, u, m = document.createElement("canvas"),
            d = t(),
            l = "c_n" + d.l,
            r = m.getContext("2d"),
            x = window.requestAnimationFrame || window.webkitRequestAnimationFrame || window.mozRequestAnimationFrame || window.oRequestAnimationFrame || window.msRequestAnimationFrame ||
              function(n) {
                window.setTimeout(n, 1e3 / 45)
              },
            w = Math.random,
            y = {
              x: null,
              y: null,
              max: 2e4
            };
          m.id = l,
            m.style.cssText = "position:fixed;top:0;left:0;z-index:" + d.z + ";opacity:" + d.o,
            e("body")[0].appendChild(m),
            o(),
            window.onresize = o,
            window.onmousemove = function(n) {
              n = n || window.event,
                y.x = n.clientX,
                y.y = n.clientY
            },
            window.onmouseout = function() {
              y.x = null,
                y.y = null
            };
          for (var s = [], f = 0; d.n > f; f++) {
            var h = w() * a,
              g = w() * c,
              v = 2 * w() - 1,
              p = 2 * w() - 1;
            s.push({
              x: h,
              y: g,
              xa: v,
              ya: p,
              max: 6e3
            })
          }
          u = s.concat([y]),
            setTimeout(function() {
                i()
              },
              100)
        } ()
    },
    beforeDestroy() {

      window.removeEventListener('scroll',this.onWindowScroll);
    },
    methods:{
      toTop(){
        document.documentElement.scrollTo({
          top:0,
          behavior:'smooth'
        })
      },
      onWindowScroll(){
        let scrolledTop=document.documentElement.scrollTop;
        console.log(scrolledTop)
        if(scrolledTop>370){
          document.getElementById('g-to-top').style.display='block'
        }else {
          document.getElementById('g-to-top').style.display='none'
        }
      },
      textLogin(){
        api.textLogin().then(result=>{
          if(result.code===20000){
            this.isShow='login'
            this.roles=result.data.roles
            this.userInfo=result.data
          }
        })
      }
    }
  }
</script>
<style>
  body{
    font-family: "modeng";
  }
  #blog-box{
    width: 1140px;
    margin: 0 auto;
  }
    .blog-header{
      background: #Fff;
     }
      .logo-box{
        margin-left: 10px;
      }
      .logo-box .logo{
        margin-top: 5px;
        color: #737F90;
        font-size: 24px;
        font-weight: 600;
      }
      .login-tips-text-box{
        margin-right: 10px;
        padding: 10px;
        font-size: 16px;
      }
      .login-tips-text-box span{
        margin-right: 5px;
        cursor: pointer;
      }
      .navigation-box{
        margin-right: 10px;
        padding: 10px;
      }
      .navigation-box span:hover,.login-tips-text-box span:hover{
        color: orangered;
      }
      .navigation-box span{
        margin-right: 40px;
        color:#737F90;
        font-size:18px ;
        cursor: pointer;
      }
      .navigation-box i{
        font-size: 20px;
        font-weight: 600;
      }
    .blog-footer{
      margin-top: 10px;
      line-height: 30px;
      text-align: center;
      color: #909090;
    }
    #g-to-top{
      position: fixed;
      right: 100px;
      bottom: 10px;
      text-align: center;
      cursor: pointer;
      border:1px solid #8A8A8A;
      padding: 0px 5px 0px 5px;
    }
    #g-to-top .el-icon-caret-top{
    font-size: 30px;
  }

  .clear-fix{
    overflow: hidden;
    zoom:1;
  }
  .float-right{
    float: right;
  }
  .float-left{
    float: left;
  }
  .default-border-radius{
    border-radius: 5px;
  }
  a{
    text-decoration: none;
    color: #222222;
  }
  body{
    background: #F2F2FA;
  }


  @media only screen and (max-width: 760px) {
    .deng-box, .deng-box1 {
      display:none;
    }
  }
  @media only screen and (min-width: 768px) and (max-width: 1024px) {
    .right {
      float: left!important;
    }
  }
  .deng-box {
    position: fixed;
    top: -29px;
    left: 160px;
    z-index: 3;
  }
  .deng-box1 {
    position: fixed;
    top: -29px;
    right: 160px;
    z-index: 3;
  }
  .deng-box1 .deng {
    position: relative;
    width: 120px;
    height: 90px;
    margin: 50px;
    background: #d8000f;
    background: rgba(216, 0, 15, 0.8);
    border-radius: 50% 50%;
    -webkit-transform-origin: 50% -100px;
    -webkit-animation: swing 5s infinite ease-in-out;
    box-shadow: -5px 5px 30px 4px rgba(252, 144, 61, 1);
  }
  .deng {
    position: relative;
    width: 120px;
    height: 90px;
    margin: 50px;
    background: #d8000f;
    background: rgba(216, 0, 15, 0.8);
    border-radius: 50% 50%;
    -webkit-transform-origin: 50% -100px;
    -webkit-animation: swing 3s infinite ease-in-out;
    box-shadow: -5px 5px 50px 4px rgba(250, 108, 0, 1);
  }
  .deng-a {
    width: 100px;
    height: 90px;
    background: #d8000f;
    background: rgba(216, 0, 15, 0.1);
    margin: 12px 8px 8px 10px;
    border-radius: 50% 50%;
    border: 2px solid #dc8f03;
  }
  .deng-b {
    width: 45px;
    height: 90px;
    background: #d8000f;
    background: rgba(216, 0, 15, 0.1);
    margin: -4px 8px 8px 26px;
    border-radius: 50% 50%;
    border: 2px solid #dc8f03;
  }
  .xian {
    position: absolute;
    top: -20px;
    left: 60px;
    width: 2px;
    height: 20px;
    background: #dc8f03;
  }
  .shui-a {
    position: relative;
    width: 5px;
    height: 20px;
    margin: -5px 0 0 59px;
    -webkit-animation: swing 4s infinite ease-in-out;
    -webkit-transform-origin: 50% -45px;
    background: #ffa500;
    border-radius: 0 0 5px 5px;
  }
  .shui-b {
    position: absolute;
    top: 14px;
    left: -2px;
    width: 10px;
    height: 10px;
    background: #dc8f03;
    border-radius: 50%;
  }
  .shui-c {
    position: absolute;
    top: 18px;
    left: -2px;
    width: 10px;
    height: 35px;
    background: #ffa500;
    border-radius: 0 0 0 5px;
  }
  .deng:before {
    position: absolute;
    top: -7px;
    left: 29px;
    height: 12px;
    width: 60px;
    content: " ";
    display: block;
    z-index: 999;
    border-radius: 5px 5px 0 0;
    border: solid 1px #dc8f03;
    background: #ffa500;
    background: linear-gradient(to right, #dc8f03, #ffa500, #dc8f03, #ffa500, #dc8f03);
  }
  .deng:after {
    position: absolute;
    bottom: -7px;
    left: 10px;
    height: 12px;
    width: 60px;
    content: " ";
    display: block;
    margin-left: 20px;
    border-radius: 0 0 5px 5px;
    border: solid 1px #dc8f03;
    background: #ffa500;
    background: linear-gradient(to right, #dc8f03, #ffa500, #dc8f03, #ffa500, #dc8f03);
  }
  .deng-t {
    font-family: 华文行楷;
    font-size: 26px;
    color: #dc8f03;
    font-weight: bold;
    line-height: 44px;
    text-align: center;
  }
  .night .deng-t,
  .night .deng-box,
  .night .deng-box1 {
    background: transparent !important;
  }
  @-moz-keyframes swing {
    0% {
      -moz-transform: rotate(-10deg)
    }
    50% {
      -moz-transform: rotate(10deg)
    }
    100% {
      -moz-transform: rotate(-10deg)
    }
  }
  @-webkit-keyframes swing {
    0% {
      -webkit-transform: rotate(-10deg)
    }
    50% {
      -webkit-transform: rotate(10deg)
    }
    100% {
      -webkit-transform: rotate(-10deg)
    }
  }











</style>
