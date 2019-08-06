<template>
  <!-- Material form login -->
  <form>
    <br><br><br><br><br><br><br><br>
    <p class="h4 text-center mb-4">KCB OK-NAME Admin Login</p>
    <div class="grey-text" style="height:auto; width:30%; margin:auto;">
      <mdb-input id = "id" label="Your ID" icon="envelope" type="email" v-model="id"/>
      <mdb-input id = "passwd" label="Your password" icon="lock" type="password" v-model="password"/>
    </div>
    <div class="text-center">
      <mdb-btn v-on:click="proceedLogin">Login</mdb-btn>
    </div>
  </form>
  <!-- Material form login -->
</template>


<script>

  import { mdbInput, mdbBtn } from 'mdbvue';
  export default {
    name: 'Basic',
    data : function() {
      return {id :"", password :""}
    },
    components: {
      mdbInput,
      mdbBtn
    },
    methods : {
      proceedLogin : function(){
        console.log(this.password);
        if(this.password==="qwer!234") {
          alert("로그인 성공");
          this.goToPages();
        }else{
          alert("잘못된 정보 입니다");
        }
      },
      goToPages () {
      this.$router.push({
        name: 'Dashboard'
      })
    }
    }
  }
</script>
