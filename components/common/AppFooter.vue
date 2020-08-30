<template>
  <footer>
    <div class="container flex-ai-center flex-jc-center">
      <h3><i class="far fa-envelope"></i>E-mail : knight0930@gmail.com </h3>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'app-footer'
}
</script>

<style lang="less" scoped>
h1 {
  font-size: 22px;
}
i {
  margin-right: 10px;
}
.container {
  height: 250px;
}

@media only screen and ( min-width : 768px ){
  h1 {
    font-size: 36px;
  }
}
</style>
