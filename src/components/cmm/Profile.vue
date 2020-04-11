<template>
    <div>
        <link rel="stylesheet" type="text/css" href="/css/ladda-themeless.min.css">
        <link rel="stylesheet" type="text/css" href="/css/normalize.css">
        <link rel="stylesheet" type="text/css" href="/css/qbkl-grid.css">
        <link rel="stylesheet" type="text/css" href="/css/style-ko.css">
        <link rel="stylesheet" type="text/css" href="/css/font-awesome.min.css">
        <div class="top-decorations">
            <a href="" style="
				position: absolute;
				left: 15px;
				top: 20px;
				text-decoration: none;
				color: #ffffff;
			"></a>
        </div>
    <section id="intro" class="fx-backstretch" >
        <div class="info" style="position: relative; z-index: 0; background: none;">
            <div class="container" style="top: 357.5px;">
                <div class="row">
                    <div class="col-full"><h1>{{name}}</h1></div>
                </div>
                <div class="row"><div class="col-1-4 centered line"></div></div>
                <div class="row">
                    <div class="col-full"><h4>소프트웨어 엔지니어</h4></div>
                </div>
            </div>
            <div class="backstretch" style="left: 0px; top: 0px; overflow: hidden; margin: 0px; padding: 0px; height: 888px; width: 1903px; z-index: -999998; position: absolute;"><img id="profile_img" src="/img/backstretch.jpg" style="position: absolute; margin: 0px; padding: 0px; border: none; width: 1903px; height: 1070.44px; max-height: none; max-width: none; z-index: -999999; left: 0px; top: -91.2188px;"></div></div>
        <div id="nav-sticky-wrapper" :class=sticky style="height: 60px;"><nav id="nav" :style=fix>
            <ul class="clearfix">
                <li v-for="(navi,index) of navis" @click="tabSwitch(index)" :key="navi.id" :class={current:navi.switch}><a :href=navi.id>{{navi.title}}</a></li>

            </ul>
        </nav></div>
    </section>
    <section id="aboutme" class="section-alt">
        <div class="container">
            <div class="row">
                <div class="col-full">
                    <h2 class="section-title">introdution</h2>
                    <div class="centered line"></div>
                </div>
            </div>

            <div class="row section-content">
                <div id="comment" class="col-1-2" style="text-align: center;">
                    <img alt="접니다!" style="max-width: none !important; height: 444px;" src="/img/profile_pic.jpg">
                </div>
                <div class="col-1-2">
                  <h4>안녕하세요 {{name}}입니다!</h4><br>
                    <p>저의 사이트를 방문해 주셔서 감사합니다!</p>
                   <ul><li>개발을 무엇 보다 즐기며 열심히 하는 27살 청년입니다!</li>
                     <li>컴퓨터 공학을 전공했고 Java와 JavaScript, Spring Boot 와 Vue.js를 주로 사용하여 웹개발을 하고 있습니다</li>
                     <li>저에게 궁금한점이 있으시다면 <a href="#contact">연락처</a>로 연락주세요~ </li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <section id="skills" class="section">
        <div class="container">
            <div class="row">
                <div class="col-full">
                    <h2 class="section-title">Skill</h2>
                    <div class="centered line"></div>
                </div>
            </div>

            <div class="row section-content">
                <div class="skill-container">
                  <div class="col-full skill-container">
                    <h3 style="font-weight: bold !important;">Programming Language</h3>
                  </div>

                    <div v-for="language of languages" :key="language" class="col-1-5 skill">
                        <h4 style="color: #001F41 !important;font-weight: bold !important;">{{language}}</h4>
                    </div><br><br><br><br>

                </div>
              <div class="col-full skill-container">
                <h3 style="font-weight: bold !important;"><br><br><br><br><br></h3>
              </div>
              <div class="col-full skill-container">
                <h3 style="font-weight: bold !important;">Usage</h3>
              </div>
                <br>
                <div class="col-2-3 col-wrap centered skill-container">

                    <div class="col-1-3" style="text-align: center !important;">
                        <h4 style="font-weight: bold !important;">프레임워크</h4><br>
                        <ul><li v-for="framework of frameworks" :key="framework">{{framework}}</li></ul>
                    </div>
                    <div class="col-1-3" style="text-align: center !important;">
                        <h4 style="font-weight: bold !important;">소프트웨어</h4><br>
                        <ul><li v-for="software of softWares" :key="software">{{software}}</li></ul>
                    </div>
                    <div class="col-1-3" style="text-align: center !important;">
                      <h4 style="font-weight: bold !important;">데이터베이스</h4><br>
                      <ul><li v-for="database of databases" :key="database">{{database}}</li></ul>
                    </div>
                </div>
            </div>
        </div>
    </section>


    <section id="education" class="section-alt">
        <div class="container">
            <div class="row">
                <div class="col-full">
                    <h2 class="section-title">education</h2>
                    <div class="centered line"></div>
                </div>
            </div>

            <div class="row section-content">
                <div v-for="education of educations" :key="education.name"  class="row school">
                    <div class="col-full">
                        <h3>{{education.name}}</h3>
                        <div class="school-meta">{{education.major}}</div>
                    </div>

                    <div class="col-full text-center">
                        <p><strong>{{education.date}}</strong>
                        </p>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <section id="portfolio" class="section">
        <div class="container">
            <div class="row">
                <div class="col-full">
                    <h2 class="section-title">project</h2>
                    <div class="centered line"></div>
                </div>
            </div>
          <div class="youtube">
            <iframe width="1260" height="709" src="https://www.youtube.com/embed/4KwTx_3iyQA" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
          </div>
          <br>
          <a href="https://drive.google.com/file/d/1jAemPPuDKz3jK_7Lh8k-uBdhKBOaMb67/view?usp=sharing" target="_blank" style="padding-left: 0px !important; font-size: large">ppt 보러 가기</a>
          <p class="ex_text">아래 이미지를 누르시면 프로젝트 메인화면으로 이동합니다.</p><br>
                    <router-link to="/home" title="RPM" style="padding-left: 160px"><img src="@/assets/image/rpmlogoblack.png" alt="RPM"></router-link>
            </div>
    </section>

    <section id="contact" class="section">
        <div class="container">
            <div class="row">
                <div class="col-full">
                    <h2 class="section-title">contact</h2>
                    <div class="centered line"></div>
                </div>
            </div>

            <div class="row section-content">
                <div class="col-2-3 col-wrap centered text-center">
                    <div class="row">
                        <div class="col-full" style="margin-bottom: 25px;">
                            함께 일하고 싶으시거나 <br>연락을 원하신다면 아래로 연락 주세요!! <br> pn : {{pn}} <br>e-mail : {{email}} <br>

                        </div>
                    </div>


                </div>
            </div>
        </div>
    </section>


    </div>


</template>

<script>
  export default {
    name: "Profile",
    data(){
      return {
        name: '강성조',
        email:'kangsj24@naver.com',
        pn:'010-3075-1222',
        navis: [
          {title: 'INTRODUTION', id: '#aboutme',switch:false}, {title: 'SKILL', id: '#skills',switch:false}, {title: 'EDUCATION', id: '#education',switch:false},
          {title: 'PROJECT', id: '#portfolio',switch:false}, {title: 'CONTACT', id: '#contact',switch:false}
        ],
        fix:'',
        sticky:'',
        languages:['java','javascript','python','sql','html'],
        frameworks:['Spring Boot','전자정부','Spring 5','Vue.js','Hibernate'],
        softWares:['windows','git','Intellij','gitHub Desktop','STS','eclipse','pycharm'],
        databases:['mariadb','mysql','oracle'],
        educations:[{name:'충북대학교',major:'컴퓨터 공학과',date:'2012.03~2019.02'},
          {name:'bit camp',major:'java기반 웹&앱 개발자 양성과정',date:'2019.08~2020.02'}]
      }
    },
    methods: {
      tabSwitch(i){
        this.navis[i].switch = true
        for (let a = 0; a < this.navis.length; a++) {
          if (a != i) {
            this.navis[a].switch = false
          }
        }


      },
      handleScroll() {
        // console.log(scrollY)

        if (scrollY < 155) {
          this.sticky = 'sticky-wrapper'
          this.fix = 'z-index: 100; '
        } else {
          this.sticky = 'sticky-wrapper is-sticky'
          this.fix = 'z-index: 100; position: fixed; top: 10px;'
        }
        if(0<scrollY && scrollY<900){
          this.tabSwitch(0)
        }else if(900<=scrollY && scrollY<1598){
          this.tabSwitch(1)
        }else if(1598<=scrollY && scrollY<2236){
          this.tabSwitch(2)
        }else if(2236<=scrollY&& scrollY<2498){
          this.tabSwitch(3)
        }else if(2498<=scrollY){
          this.tabSwitch(4)
        }
      },


    },
    created() {
      window.addEventListener('scroll', this.handleScroll);
    },
    destroyed() {
      window.removeEventListener('scroll', this.handleScroll);
    }
  }

</script>

<style scoped>
    .container a{
       padding-left: 150px;
    }
    #portfolio{
        padding: 300px;
    }
    #contact{
        padding: 300px;
    }
    .col-1-2 {
      text-align: center !important;
    }
    #profile_img {
      max-width: 100% !important;
      max-height: 100% !important;
    }
    #nav ul li a {
      padding: 0px 45px 0px 45px !important;
    }
    .ex_text{
      text-align: center;
    }
    .container a {
      padding-left: 0;
    }
    h4,h3{
      font-weight: bold;
    }
    .youtube {

      position: relative;

      width: 100%;

      padding-bottom: 56.25%;

    }

    .youtube iframe {

      position: absolute;

      width: 100%;

      height: 100%;

    }

</style>
