<template>
    <div id="index-page-box"  class="index-page-box clear-fix">


      <div id="index-center-part" class="index-center-part float-left">
        <div class="loop-box default-border-radius" >
          <div  style="display: inline-block;width:600px;min-height: 300px" >
            <template >
              <el-carousel :interval="5000" arrow="always" height="300px">
                <el-carousel-item v-for="(item,index) in loops" :key="'info_1'+index">
                  <img :src="item.imageUrl" style="object-fit: cover; width:600px; border-radius: 5px;max-height: 300px" lazy>
                </el-carousel-item>
              </el-carousel>
            </template>
          </div>
          <div  style=" display:inline-block;height:300px;" >
            <div class="topArticleContent" style="border-radius: 5px;" >
              <div class="topArticle"style=" position: relative;">
                <img class="topImage" src="https://blog.guoz.top/usr/uploads/2020/07/2992293730.jpg" >
                <div class="topTitle" style=" width: 260px;height: 40px; position:absolute; left:0;bottom:7px;background: linear-gradient(to bottom, rgba(6,6,6,0), rgba(6,6,6,0.7));">
                  <h3 style="margin-top: 0;margin-bottom: 0">
                    <svg t="1612862741151" class="icon" viewBox="0 0 2852 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="2682" width="200" height="200"><path d="M1491.788301 556.211699h305.203342v41.359332h-305.203342v-41.359332z m0 144.044568h305.203342v42.785516h-305.203342v-42.785516z m0-213.927576h305.203342v41.359331h-305.203342v-41.359331z m0 142.618384h305.203342v41.359332h-305.203342v-41.359332z m248.155989-376.512535h98.406685v54.194986h-98.406685V252.43454z m-148.32312 0h104.111421v54.194986h-104.111421V252.43454z m-141.192201 0h98.406686v54.194986h-98.406686V252.43454z" p-id="2683" fill="#d81e06"></path><path d="M2702.618384 0h-2551.442897c-82.718663 0-149.749304 67.030641-149.749303 149.749304v723.075209c0 82.718663 67.030641 149.749304 149.749303 149.749303h2551.442897c82.718663 0 149.749304-67.030641 149.749304-149.749303v-723.075209c0-82.718663-67.030641-149.749304-149.749304-149.749304z m-1607.309192 988.345404h-944.133705c-62.752089 0-114.094708-51.342618-114.094707-114.094708v-723.075209c0-62.752089 51.342618-114.094708 114.094707-114.094707h944.133705v951.264624z m1166.618385-767.286908h333.727019v45.637883h-145.470752c-1.426184 24.245125-4.278552 47.064067-8.557103 68.456824h132.635097v312.334262h-47.064066V380.791086h-199.665739v269.548747h-45.637883v-313.760446h112.668524c4.278552-22.818942 7.130919-45.637883 8.557103-68.456824h-139.766017l-1.426183-47.064067z m-323.743733 560.490251h-589.013928v-38.506964h95.554318V452.100279h159.732591c2.852368-12.835655 4.278552-25.671309 7.130919-37.08078h-251.008357v-35.654596h255.286908l4.278552-38.506964h-215.353761v-122.651811h476.345404v122.651811h-213.927576l-4.278552 38.506964h262.417827v35.654596h-266.696378c-2.852368 12.835655-4.278552 25.671309-7.13092 37.08078h191.108635v290.941504h95.554318v38.506964z m221.058496-52.768803c0 38.506964-18.54039 58.473538-57.047354 58.473538h-74.16156l-9.983287-44.211699c24.245125 1.426184 47.064067 2.852368 68.456825 2.852367 15.688022 0 24.245125-9.983287 24.245125-28.523676V266.696379h-101.259053v-45.637883h229.615599v45.637883h-78.440111l-1.426184 462.083565z m288.089136-192.534819c-1.426184 69.883008-18.54039 125.504178-52.768802 166.86351-32.802228 38.506964-85.571031 68.456825-158.306407 91.275766l-25.671309-39.933148c69.883008-19.966574 119.799443-47.064067 146.896936-81.292479 27.097493-34.228412 39.933148-79.866295 41.359332-136.913649v-116.947075h47.064066v116.947075h1.426184z m118.373259 260.991644c-28.523677-35.654596-67.030641-74.16156-118.373259-114.094708l32.802229-29.94986c47.064067 37.08078 86.997214 72.735376 119.799443 109.816156l-34.228413 34.228412z" p-id="2684" fill="#d81e06"></path><path d="M338.005571 560.490251l52.768802 51.342618 156.880223-158.306407v350.841226h72.735376v-349.415042l159.732591 158.306407 51.342618-52.768802-251.008356-246.729805-242.451254 246.729805z m-47.064067-340.857939h584.735376v72.735376h-584.735376v-72.735376z" p-id="2685" fill="#d81e06"></path></svg>
                    <span class="tip_product-buyer-name"  v-text="topArticles[1].summary" style="color:#FFFFFF;"></span>
                  </h3>
                </div>
              </div>

            </div>
            <div class="topArticleContent" style="border-radius: 5px" >
              <div class="topArticle"style=" position: relative;">
                <img class="topImage" src="https://blog.guoz.top/usr/uploads/2020/08/1024394967.jpg" style="object-fit: cover;width: 260px;height: 145px;border-radius: 5px">
                <div class="topTitle" style=" width: 260px;height: 40px; position:absolute; left:0;bottom:7px;background: linear-gradient(to bottom, rgba(6,6,6,0), rgba(6,6,6,0.7));">
                  <h3 style="margin-top: 0;margin-bottom: 0">
                    <svg t="1612862741151" class="icon" viewBox="0 0 2852 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="2682" width="200" height="200"><path d="M1491.788301 556.211699h305.203342v41.359332h-305.203342v-41.359332z m0 144.044568h305.203342v42.785516h-305.203342v-42.785516z m0-213.927576h305.203342v41.359331h-305.203342v-41.359331z m0 142.618384h305.203342v41.359332h-305.203342v-41.359332z m248.155989-376.512535h98.406685v54.194986h-98.406685V252.43454z m-148.32312 0h104.111421v54.194986h-104.111421V252.43454z m-141.192201 0h98.406686v54.194986h-98.406686V252.43454z" p-id="2683" fill="#d81e06"></path><path d="M2702.618384 0h-2551.442897c-82.718663 0-149.749304 67.030641-149.749303 149.749304v723.075209c0 82.718663 67.030641 149.749304 149.749303 149.749303h2551.442897c82.718663 0 149.749304-67.030641 149.749304-149.749303v-723.075209c0-82.718663-67.030641-149.749304-149.749304-149.749304z m-1607.309192 988.345404h-944.133705c-62.752089 0-114.094708-51.342618-114.094707-114.094708v-723.075209c0-62.752089 51.342618-114.094708 114.094707-114.094707h944.133705v951.264624z m1166.618385-767.286908h333.727019v45.637883h-145.470752c-1.426184 24.245125-4.278552 47.064067-8.557103 68.456824h132.635097v312.334262h-47.064066V380.791086h-199.665739v269.548747h-45.637883v-313.760446h112.668524c4.278552-22.818942 7.130919-45.637883 8.557103-68.456824h-139.766017l-1.426183-47.064067z m-323.743733 560.490251h-589.013928v-38.506964h95.554318V452.100279h159.732591c2.852368-12.835655 4.278552-25.671309 7.130919-37.08078h-251.008357v-35.654596h255.286908l4.278552-38.506964h-215.353761v-122.651811h476.345404v122.651811h-213.927576l-4.278552 38.506964h262.417827v35.654596h-266.696378c-2.852368 12.835655-4.278552 25.671309-7.13092 37.08078h191.108635v290.941504h95.554318v38.506964z m221.058496-52.768803c0 38.506964-18.54039 58.473538-57.047354 58.473538h-74.16156l-9.983287-44.211699c24.245125 1.426184 47.064067 2.852368 68.456825 2.852367 15.688022 0 24.245125-9.983287 24.245125-28.523676V266.696379h-101.259053v-45.637883h229.615599v45.637883h-78.440111l-1.426184 462.083565z m288.089136-192.534819c-1.426184 69.883008-18.54039 125.504178-52.768802 166.86351-32.802228 38.506964-85.571031 68.456825-158.306407 91.275766l-25.671309-39.933148c69.883008-19.966574 119.799443-47.064067 146.896936-81.292479 27.097493-34.228412 39.933148-79.866295 41.359332-136.913649v-116.947075h47.064066v116.947075h1.426184z m118.373259 260.991644c-28.523677-35.654596-67.030641-74.16156-118.373259-114.094708l32.802229-29.94986c47.064067 37.08078 86.997214 72.735376 119.799443 109.816156l-34.228413 34.228412z" p-id="2684" fill="#d81e06"></path><path d="M338.005571 560.490251l52.768802 51.342618 156.880223-158.306407v350.841226h72.735376v-349.415042l159.732591 158.306407 51.342618-52.768802-251.008356-246.729805-242.451254 246.729805z m-47.064067-340.857939h584.735376v72.735376h-584.735376v-72.735376z" p-id="2685" fill="#d81e06"></path></svg>
                    <span class="tip_product-buyer-name"  v-text="topArticles[0].summary" style="color:#FFFFFF;"></span>
                  </h3>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="article-box default-border-radius ">
          <div class="article" v-for="(item,index) in topArticles" :key="'info_2'+index">
            <div class="article-title">
              <span class="top-tips  "> 置顶</span>
              <a :href="'/article/'+item.id">
                <span class="title"  v-text="item.title" ></span>
              </a>
            </div>
            <div class="summary">
              <span v-text="item.summary"></span>
              <span>.....</span>
              <el-tag size="mini" style="cursor: pointer" ><a :href="'/article/'+item.id">阅读原文</a></el-tag>
          </div>
            <div class="label" >
              <el-tag
                v-for="(label,index) in item.labels"
                :key="'info_3'+index"
                effect="plain"
                size="mini">
                <a :href="'/search?keyword='+label" target="_blank">
                  {{label}}
                </a>

              </el-tag>
            </div>
          </div>
          <div class="article clear-fix" v-for="(item,index) in listArticle" :key="'info_4'+index">
            <div class="article-left  float-left ">
              <div class="article-img ">
                <el-image :src="'http://47.103.216.205:2020/admin/image/'+item.cover" style="object-fit: cover" lazy></el-image>
              </div>
            </div>
            <div class="article-right  float-left">
              <div class="article-title">
                <a :href="'/article/'+item.id">
                <span class="title"  v-text="item.title"></span>
                </a>
              </div>
              <div class="summary">
                <span v-text="item.summary"></span>
                <span>.....</span>
                <el-tag size="mini" style="cursor: pointer" ><a :href="'/article/'+item.id">阅读原文</a></el-tag>
              </div>
              <div class="FFFFFF"  >
                <el-tag
                  v-for="(label,index) in item.labels"
                  :key="'info_5'+index"
                  effect="plain"
                  size="mini">
                  <a :href="'/search?keyword='+label" target="_blank">
                    {{label}}
                  </a>
                </el-tag>
              </div>
            </div>
          </div>
        </div>
        <div class="article-navigation">
          <el-pagination
            background
            layout="prev, pager, next"
            @current-change="onPageChang"
            :pageSize="pageNavigation.pageSize"
            :total="pageNavigation.totalCount"
            :current-page="pageNavigation.currentPage"
            >
          </el-pagination>
        </div>
      </div>
      <div class="index-right-part float-left">
        <div class="content-search" >
        <el-input
          @keyup.enter.native="toSearch()"
          placeholder="请输入内容"
          prefix-icon="el-icon-search"
          v-model="keyword">
        </el-input>
      </div>
        <div id="index-left-part"class="index-left-part " >
          <div class="user-avatar">
            <img :src="userInfoText.avatar">
          </div>
          <div class="user-name">
            <a v-if="userInfoText.userName==='未登录'"  :href="'/login'">
              <span v-text="userInfoText.userName" ></span>
            </a>
            <a v-else>
              <span v-text="userInfoText.userName" ></span>
            </a>
          </div>
          <div class="user-sign">
            <span v-text="userInfoText.sign" ></span>
          </div>
          <div class="left-user-self-links">
            <el-tooltip class="item" effect="dark" content="退出登录" placement="top-start">
              <span class="sob_blog sobtuichu ; " @click="doLogout"></span>
            </el-tooltip>
            <el-tooltip class="item" effect="dark" content="bibi" placement="top-start">
              <span class="sob_blog sobbilibili-line   "></span>
            </el-tooltip>
            <el-tooltip class="item" effect="dark" content="CSDN" placement="top-start">
              <a href="https://blog.csdn.net/Ahhjhhj?spm=1010.2135.3001.5113">
                <span class="sob_blog sobview "></span>
              </a>
            </el-tooltip>



          </div>
          <div class="list-categories">
            <div :class="categoryId===item.id?'categories-item-active':'categories-item'"
                 v-for="(item,index) in categories" :key="index">
              <span v-text="item.name" @click="listArticleByCategoryId(item)"></span>
            </div>
          </div>

        </div>
        <br>
        <PopularCard></PopularCard>
        <br>
        <CountDown></CountDown>
        <br>
        <AdvertisementLoop></AdvertisementLoop>
      </div>

    </div>

</template>

<script>
  import * as api from '../api/api'
  import * as utils from '../api/utils'

  export default {
    data(){
      return {
        keyword:'',
        margin:{top: 0, right: 0, bottom: 0, left: 0 },
        rotate:{from: -20, to: 40, numOfOrientation: 8 },
        fontSize:[20, 50],
        wordPadding:3,
        defaultWords: [],
        categoryId:'',
        isLogin:true,
        userInfoText:{
          avatar:'https://cdn.sunofbeaches.com/images/default_avatar.png',
          userName:"未登录",
          sign:"登录才能够看到哦"
        }
      }
    },
    created() {

    },

    mounted() {
      this.listLabel();
      this.onWindowScroll();
      this.textLogin();
      let that=this;
      window.onresize=function () {
        that.onWindowScroll()
      }
      // 监听滑动
      window.addEventListener('scroll',this.onWindowScroll)
    },
    beforeDestroy() {

      //销毁监听，释放资源
      window.removeEventListener('scroll',this.onWindowScroll);
    },
    methods:{
      doLogout(){
        if(!this.isLogin){
         return
        }
        api.doLogout().then(result=>{
          console.log(result.code)
        if(result.code===20000){
          this.$message.success(result.message)
          location.href='/';
        }else {
          this.$message.error(result.message)
          this.isLogin=false
        }
      })
      },
      textLogin(){
        api.textLogin().then(result=>{
          if(result.code===20000){

            this.userInfoText=result.data;
            if(result.data.sign===null){
              this.userInfoText.sign='暂时没有签名，该用户似乎很懒~'
              this.isLogin=true;
              // location.reload()
            }
          }else{
            console.log(result.message)
          }
        })
      },
      listArticleByCategoryId(item){
        this.categoryId=item.id;
        //页数重置为第一页
        this.pageNavigation.currentPage=1;
        api.listArticle(this.categoryId,this.pageNavigation.currentPage,this.pageNavigation.pageSize).then(result=>{
            this.handleResult(result);
        })

      },
      toSearch(){
        this.keyword=this.keyword.trim()
        if(this.keyword===''){
          return
        }else {
          //todo:
          this.$router.push({
            path:'/search',
            query:{
              keyword:encodeURIComponent(this.keyword),
              text:'text'
            }
          })
          // location.href='/search/'+encodeURIComponent(this.keyword);
        }

      },
      onWindowScroll(){
        let scrolledTop=document.documentElement.scrollTop;
        let scrolledLeft=document.documentElement.scrollLeft;
        let centerPart=document.getElementById('index-center-part');
        let leftPart=document.getElementById('index-left-part');
        let parentPart=document.getElementById('index-page-box');
        // console.log("centerPart--->"+centerPart+"    leftPart--->"+leftPart)


        if(centerPart||leftPart||scrolledLeft){
          let baseTop=centerPart.offsetTop;
          console.log(baseTop)
          if(scrolledTop<=baseTop){
            leftPart.style.top=(baseTop-scrolledTop)+'px'
          }else{
            leftPart.style.top='5px'
          }
          if(scrolledLeft>0){
            leftPart.style.left=-scrolledLeft+'px';
          }else{
            leftPart.style.left=parentPart.offsetLeft+'px'
          }
        }
        //右边悬浮

        let taobaoPart=document.getElementById('taobao-loop-testscroll');
        let cardPart=document.getElementById('always-used-cards');

        if(taobaoPart){
          let baseTop=taobaoPart.offsetTop+taobaoPart.offsetHeight
          if (scrolledTop >= baseTop) {

            cardPart.style.position='fixed';
            cardPart.style.top='10px';
            cardPart.style.width='230px';
          }else{

            cardPart.style.position='';
            cardPart.style.top='';
          }
          if(scrolledLeft>0){
            cardPart.style.left=parentPart.offsetWidth-scrolledLeft-cardPart.offsetWidth+parentPart.offsetLeft+'px'
          }else{
            cardPart.style.left=parentPart.offsetWidth-cardPart.offsetWidth+parentPart.offsetLeft+'px'
          }
        }

      },
      listLabel(){
        let listLabel=utils.testSessionStorage("listLabel")
        if(listLabel!==null){
          this.defaultWords=listLabel;
          return;
        }
        api.listLabel(8).then(result=>{
          if(result.code===20000){
            this.defaultWords=result.data.content;
            console.log("我是请求")
            sessionStorage.setItem("listLabel",JSON.stringify(result.data.content));
          }
        })
      },

      wordClickHandler(name, value, vm) {
        // location.target="_blank";
        location.href='/search?keyword='+name
      },
      handleResult(result){
        if(result.code===20000){
          this.listArticle=result.data.content;
          //切换页面回到顶部
          let topHeader=document.getElementById('blog-header');
          if(topHeader){
            topHeader.scrollIntoView({
              block:'start',
              behavior:"smooth"
            })
          }
            this.pageNavigation.currentPage=result.data.number+1,
            this.pageNavigation.totalCount=result.data.totalElements,
            this.pageNavigation.pageSize=result.data.size
        }else{
          this.$message.error(result.message);
        }
      },
      onPageChang(page){
          api.listArticle(this.categoryId,page,this.pageNavigation.pageSize).then(result=>{
            this.handleResult(result);
          })
      }
    },
    async asyncData({params}){
      let userInfo=await api.getAdminInfo();
      let categories=await api.getCategories();
      let loops=await api.getLoops();
      let topArticles=await api.getTopArticle();
      let listArticle=await api.listArticle('',1,5);
      let allCategory=[];
      allCategory.push({
        name:'全部分类',
        id:''
      });
      allCategory=allCategory.concat(categories.data);
      let  pageNavigation={
          currentPage:listArticle.data.number+1,
          totalCount:listArticle.data.totalElements,
          pageSize:listArticle.data.size
        };

        return {
          userInfo:userInfo.data,
          categories:allCategory,
          loops:loops.data,
          topArticles:topArticles.data,
          listArticle:listArticle.data.content,
          pageNavigation:pageNavigation,

      };
    }
  }
</script>
<!--1140px分为 240 660 240-->
<style scoped>
.float-left{
  float: left;
}
  #index-left-part{
    /*position: fixed;*/
    /*text-align: center;*/
  }
  .article-title a{

    color: black;
  }
  .summary .el-tag a{
    color: #535353;
  }
  .summary .el-tag a:hover,.article-title a:hover{
    color: #FF4500;
  }
  .loop-box .el-carousel__container {
    height: 250px;
  }
  .wordCloud .text{
    cursor:pointer;
  }
  .index-right-part{
    width: 230px;
    margin-left: 10px;
  }
  .index-right-part .content-search{
    margin-bottom: 10px;
    background: #FFFFFF;
  }
  .index-right-part .always-used-cards{

    margin-bottom: 10px;
    background: #FFFFFF;
    font-weight: 600;

  }
  .label-list-box .wordCloud{
    height: 200px;
  }
  .index-right-part .advertisement{
    margin-bottom: 10px;
    background: #FFFFFF;
    font-weight: 600;
  }
  .always-used-cards .title, .advertisement .title{
    font-size: 15px;
    color: #8A8A8A;
    padding: 5px;
  }


  .article-navigation{
    margin-top: 10px;
  }
  .article-navigation .el-pagination.is-background .el-pager li{
    background-color: #FFFEFF;
  }
  .article-left{
    margin-right: 10px;
  }
  .article .article-left .article-img img{
    width: 100px;
    height: 100px;
    display: flex;
    justify-content: center;
    border-radius:5px

  }
  .summary{
    font-size: 12px;
  }
  .label{
    margin-top: 10px;
  }
  .label .el-tag{
    margin-right: 8px;
    cursor: pointer;
  }
  .label .el-tag a,.article-right .el-tag a{
    color: #8A8A8A;
  }
  .label .el-tag a:hover,.article-right .el-tag a:hover{
    color: #222222;
  }
  .article{
    margin-top: 10px;
    padding: 10px;
    background: #FFFEFF;
  }
  .article-title{
    margin-bottom: 10px;
  }
  .article .top-tips {
    padding: 3px;
    background: orangered;
    font-size: 10px;
    color: #F2F2FA;
    border-radius: 3px;
  }

.head_article .top-tips {
    padding: 3px;
    background: orangered;
    font-size: 10px;
    color: #F2F2FA;
    border-radius: 3px;
  }
.tip .product-buyer-name {
  display:inline-block;
  max-width: 200px;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.tip_product-buyer-name {
  display:inline-block;
  max-width: 150px;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
  .article .title{
    font-size: 18px;
    font-weight: 600;

    display:inline-block;
    max-width: 400px;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .loop-box{
    padding: 10px;
    background: #FFFEFF;
  }

  .loop-box .el-carousel__button{
    width: 10px;
    height: 10px;
    border-radius: 50%;
  }
  .list-categories{
    margin-top: 15px;
  }
  .list-categories .categories-item  {
    padding: 15px;
    border-radius: 5px;
  }
  .list-categories .categories-item-active{
    padding: 15px;
    color:#535353;
    border-radius: 5px;
    background: #D4D4D4;
  }
  .list-categories .categories-item span{
    font-size: 16px;
    font-weight: 600;
    color: #8A8A8A;
    cursor: pointer;
    text-align: center;

  }
  .list-categories .categories-item span:hover{
    color:#535353;
  }
  .index-left-part .user-avatar img{
    width: 80px;
    height: 80px;
    border-radius: 50%;
    margin-top: 10px;
  }
  .index-left-part .user-name span{
    margin-top: 10px;
    color: #8A8A8A;
    font-size:25px ;
  }
  .index-left-part .user-sign span{
    color: #D4D4D4;
    font-size:13px ;
  }
  .user-name{
    margin-top: 15px;
  }
  .user-sign{
    margin-top: 15px;

    display:inline-block;
    max-width: 220px;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .left-user-self-links{
    margin-top: 15px;

  }
  .index-left-part .left-user-self-links span{
    font-size: 30px;
    font-weight: 600;
    margin-right: 15px;
    margin-left: 10px;
    color: #8A8A8A;
    cursor: pointer;
  }
  .left-user-self-links span:hover{
    color:#535353 ;
  }
  .index-page-box{
    margin-bottom: 10px;
    margin-top: 10px;
  }
  .index-left-part{
    margin-right: 10px;
    text-align: center;
  }
  .index-center-part{
    margin-left: 0px;
    margin-right: 10px;
    width:890px;
  }

  .index-left-part{
    width: 230px;
    background: #FFFFFF;

  }
.topArticleContent{

}
.topArticleContent .topArticle img{
  object-fit: cover;
  width: 260px;
  height: 145px;
  border-radius: 5px
}

.topArticleContent .topArticle .topTitle h3 .icon {
  fill: black;
  width: 40px;
  height: 40px;
  margin-right: 8px;
}
.topArticleContent .topArticle .topTitle h3 {
  display: flex;
  align-items: center;
  border-bottom: 1px solid #EBEEF5;
  font-size: 16px;
  font-weight: 500;
  height: 45px;
  line-height: 45px;
  padding: 0 15px;
  color: black;
}

</style>
