<template>
  <!-- Material form login -->
  <form>
    <br><br><br><br><br><br><br><br>
    <p class="h4 text-center mb-4">KCB OK-NAME Admin Login</p>
    <div class="grey-text" style="height:auto; width:30%; margin:auto;">
      <mdb-input label="Your ID" icon="envelope" type="email" v-model="id"/>
      <mdb-input label="Your password" icon="lock" type="password" v-model="password"/>
      <input type="text" placeholder="Enter sms number.." v-model="otpCode"  name="otpCode"> 
      
      <!--
      v-validate="'min:5'"
      <p class="alert" v-if="errors.has('otpCode')">{{ errors.first('otpCode') }}</p>
      -->
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
/*
만약 jquery 였다면 ?
<input type="text" placeholder="Enter sms number.." name="otpCode" onkeypress="onKeyPressLengthCheck(this, 5)""> 
<p class="alert" id ="alertMsg">5글자 이상 입력해 주세요 </>

//키 이벤트에 대한 조작필요 => v-model
function onKeyPressLengthCheck(_this, maxLen) {
	var val = $("#"+_this.id).val();
	var keyCode = event.keyCode;
	// Backsapce, Delete
	if(keyCode == 8 || keyCode == 46) {
		return;	
  }
  //알럿 메세지에 대한 show and hide 필요 = => v-if
	if(val.length > maxLen) { 
    $("#alertMsg").show();
		event.returnValue = false;
	}else{
    $("#alertMsg").hide();
  }
}

문제 1. 단순 기능에 코드가 너무 많다
문제 2. 비슷한 기능의 함수 관리

*/
</script>





