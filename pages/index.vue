<template>
  <section>
    <section id="home" class="flex flex-wrap flex-jc-center flex-ai-center">
      <div class="col-m-12 col-p-12">
        <h1>김현구</h1>
        <h2>Kim Hyeon-gu Lifetime Web Portfolio</h2>
      </div>
    </section>
    <div class="container">
      <section id="about" class="col-m-12 col-p-12">
        <h1><span>About</span></h1>
        <div>
          <p>
            안녕하세요 김현구입니다. <br/>
          </p>
            평범한 가정에서 태어나 아버지가 컴퓨터를 종사하여 어렸을 때 컴퓨터를 빨리 접하게 되었습니다.<br/>
            그 덕에 컴퓨터를 잘 다뤄 초등학교 때부터 컴퓨터를 잘 다루는 애로 알려졌고, 선생님들의 컴퓨터에 문제가 발생하면 해결함으로써 보람을 느끼고 좋아한다는 결론에 이르렀습니다.<br/>
            <br/>
            후에 사이버보안 학과를 진학한 후, 보안과 블록체인에 관심이 생겨 병행하여 공부하였고<br/>
            블록체인 SI 업체에서 신규 서비스 기획 및 개발을 하는 동안 블록체인 기술으로는 보안을 대체 할 수 없다는 한계를 깨닫고 문제점을 해결하기 위해 보안 공부를 준비하고 있습니다.<br/> 
          
          <div class="flex flex-ai-center div-more-infomation">
            <a class="btn btn-primary btn-resume" href="https://naver.com/">이력서 보러가기 <i class="fas fa-arrow-right"></i></a>
          </div>
        </div>
      </section>
      <section id="career" class="col-m-12 col-p-12">
        <h1><span>My Career</span></h1>
        <div class="flex flex-wrap row">
          <div class="col-m-12 col-p-6" v-for="card in CareerCards" :key="card.id">
            <career-card
              :logoImg="card.img"
              :cardStyle="card.style"
              :imgResponsive="card.imgResponsive"
              :link="card.link"
            ></career-card>
          </div>
        </div>
      </section>
      <section id="pa" class="col-m-12 col-p-12">
        <h1><span>My Activities</span></h1>
        <div class="flex flex-wrap flex-jc-center row">
          <div class="col-m-12 col-p-4" v-for="card in paCards" :key="card.id">
            <pa-card
              :date="card.date"
              :title="card.title"
              :img="card.img"
              :contents="card.contents"
            ></pa-card>
          </div>
        </div>
      </section>
    </div>
  </section>
</template>

<script>
import CareerCard from '~/components/index/CareerCard.vue'
import PaCard from '~/components/index/PaCard.vue'

export default {
  name: 'index',
  components: { CareerCard, PaCard },
  data () {
    return {
      CareerCards: [
        {
          img: '/image/companyLogo/logo-glo.png',
          imgResponsive: false,
          style: { 'background-color': '#CEECF5' },
          link: 'glosfer'
        },
      ],
      paCards: [
        {
          'date': '2019.11.29',
          'title': 'Blockchain-based credit rating system for online P2P loans',
          'img': '/pa/dcs-conference.png',
          'contents': [
            '<strong>온라인 P2P 대출, 블록체인기반 신용평가시스템</strong>',
            '- 학회명 : 2019년도 한국디지털콘텐츠학회 학술대회',
            '- 입상 : 금상 ',
            '- <a href="https://bit.ly/31GR3ms">논문 다운로드</a> &nbsp <a href="https://bit.ly/3jpieYQ"> 입상</a>'
          ]
        },
                {
          'date': '2019.06 - 2019.11',
          'title': 'BlockChain Loan P2P,WANT Project',
          'img': '/pa/want-project.png',
          'contents': [
            '<strong>블록체인 대출 P2P, WANT 프로젝트</strong>',
            '- 팀명: WANT / 팀 인원: 3명',
            '- 개발 기여도 : 100% (Front-End), 홍보 영상 제작',
            '- 입상 : 우수상 , 특별상',
            '- 개발툴 : React.js, Firebase, HyperLedger Composer, Node.js, ',
            '- <a href="https://github.com/WANT-BlockChain/want_ReactApp_Web">Github</a> &nbsp <a href="https://bit.ly/2QyPws6">PPT</a> &nbsp <a href="https://www.notion.so/hyeon9/P2P-5218dc29c5a2462f8cf18a71e9ddbc3e"> Notion</a>'
          ]
        },
        {
          'date': '2019.03 - 2019.06',
          'title': 'Licence acquisition solution',
          'img': '/pa/licence.png',
          'contents': [
            '<strong>자격층 취득 솔루션 어플리케이션(졸업작품) </strong>',
            '- 팀명 : Licence / 팀 인원 : 3명',
            '- 개발 기여도 : 100% (FullStack)',
            '- 사용언어 : (Android)JAVA, PHP, HTML, Firebase',
            '- <a href="https://github.com/black9/CapstonDesign">Github</a> &nbsp <a href="https://bit.ly/3gIFrTY"> PPT</a> &nbsp <a href="https://www.notion.so/hyeon9/4f3794b29f9a45e08486494366821351"> Notion</a>'
          ]
        },
        {
          'date': '2018.11.28',
          'title': 'Introduction of Block Chain for Software License Certification',
          'img': '/pa/ieie-conference.png',
          'contents': [
            '<strong>소프트웨어 라이센스 인증을 위한 블록체인 제안</strong>',
            '- 학회명 : 대한전자공학회 2018년도 정기총회 및 추계학술대회',
            '- <a href="http://conf.theieie.org/2018f/"> 2018 대한전자공학회 사이트</a> &nbsp <a href="https://bit.ly/3jxYrqp"> 논문 다운로드</a> ',
   
          ]
        },
        {
          'date': '2013.01 ~ 2014.04',
          'title': 'ThinkingBridge Mobile CustomRom',
          'img': '/pa/mobile-teamproject.png',
          'contents': [
            '<strong>안드로이드 스마트폰 커스텀 OS 프로젝트 </strong>',
            '- 팀명: ThinkingBridge / 팀 인원: 8명 ',
            '- 안드로이드 커스텀 OS 소스 관리 및 플랫폼 개발 담당',
            '- <a href="https://github.com/thinkingbridge"> Github</a> &nbsp <a href="https://bit.ly/2EHnvwf"> XDA</a> &nbsp <a href="https://bit.ly/2EHnvwf"></a> ',

          ]
        },
      ]
    }
  }
}
</script>

<style lang="less" scoped>
@import '~assets/css/color.less';

.container {
  margin-bottom: 60px;
  section {
    margin-top: 60px;
    line-height: 1.8;
  }
  h1 {
    margin-bottom: 15px;
    span {
      border-bottom: 5px solid @dark-black;
    }
  }
}
.row {
  margin: 0px -10px;
}
#home {
  width: 100%;
  height: 300px;
  text-align: center;
  padding: 0px 20px;
  h1 {
    color: #fff;
    font-size: 4rem;
  }
  h2 {
    color: #fff;
    font-size: 1.8rem;
    i {
      margin-right: 10px;
    }
  }
	background-color: #000000;
	background-image: url("https://images.unsplash.com/photo-1554034483-04fda0d3507b?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjExMzk2fQ&auto=format&fit=crop&w=1650&q=80");
	background-attachment: fixed;
	background-size: cover;
	background-position: center;
}
#about {
  .div-more-infomation {
    margin-top: 20px;
  }
  .btn-resume {
    color: #0B3861;
    transform: scale(1);
    transition: transform 0.35s;
  }
  .btn-resume:hover {
    transform: scale(1.1);
    transition: transform 0.35s;
  }
}

@media only screen and ( min-width : 768px ){
}
</style>
