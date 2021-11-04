<template>
  <div class="about">
    <h1>This is an about page</h1>
    <v-btn depressed @click="handleBtn"> 요청 보냄 시작 </v-btn>
    <v-btn depressed color="error" @click="handleBtn2"> 요청 보냄 종료 </v-btn>
  </div>
</template>

<script>
import axios from "axios";
export default {
  // 컴포넌트의 대표이름(devtools에 나오는 이름)
  name: "App",
  // 추가하고 싶은 컴포넌트 등록(import something from "/path")
  components: {},
  // 컴포넌트 데이터 정의
  data() {
    return { startInterval: null };
  },
  // 컴포넌트 메소드 정의
  methods: {
    handleBtn() {
      this.startInterval = setInterval(async () => {
        try {
          const respone = await axios.get(
            "https://www.google.com",
          );
          console.log(respone);
        } catch (error) {
          console.log(error);
        }
      }, 3000);
    },
    handleBtn2() {
      clearInterval(this.startInterval);
    },
  },
};
</script>