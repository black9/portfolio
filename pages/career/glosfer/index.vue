<template>
  <section>
    <section class="flex flex-jc-center flex-ai-center section-main">
      <div class="col-m-12 col-p-12">
        <h1>GLOSFER</h1>
        <h2>Blockchain in everyday life</h2>
      </div>
    </section>
    <section class="container section-info">
      <div class="col-m-12 col-p-12">
        <h1>회사 소개</h1>
        <p>㈜글로스퍼(Glosfer)는 한국의 블록체인 기술 개발 및 상용화를 위한 사업과 핀테크 사업 전문 업체</p>
      </div>
      <div class="div-wrapper col-m-12 col-p-12">
        <h1>서비스</h1>
        <h2>hycon</h2>
        <p>- 하이콘은 하이퍼커넥티드 코인(Hyperconnected Coin)의 줄임말로 신속하고 확장성이 뛰어난 블록체인에 기반을 둔 디지털 자산</p>
        <p>- <a href="https://hycon.io"> hycon.io </a></p><br/>
      </div>
        <div class="div-wrapper col-m-12 col-p-12">
        <h1>기획</h1>
           <p> - 회사 기밀 검토 후 작성하겠습니다 <br/> </p>
        </div>
    </section>
    </section>
</template>

<script>

export default {
  name: 'index',
  layout: 'noFooter'
}
</script>

<style lang="less" scoped>
@import '~assets/css/color.less';

.section-main {
  height: 400px;
  background-color: #02c1f7;
  color: #ffffff;
  text-align: center;
  h1 {
    font-size: 4rem;
  }
}

.div-wrapper {
  margin: 40px 0px 0px 0px;
  video {
    padding: 10px 0px;
  }
}

.section-info {
  padding-top: 40px;
  h1 {
    padding-bottom: 10px;
  }
  div {
    margin-bottom: 20px;
  }
  p {
    line-height: 2;
  }
}

.div-info {
  margin: 10px 0px 0px 0px;
  p {
    font-size: 16px;
    line-height: 1.8;
  }
}

@media only screen and ( min-width : 768px ){
}
</style>
