<template>
  <v-card class="mx-auto my-12" max-width="374">
    <v-img src="@/assets/photos/photo3.jpg" height="250px" />
    <v-card-title>About</v-card-title>
    <v-card-subtitle>This is an about page.</v-card-subtitle>
    <v-divider />
    <v-card-text>
      The v-card component is a versatile component that can be used for anything from a panel to a
      static image.
    </v-card-text>
    <v-divider />
    <v-card-text
      >The card component has numerous helper components to make markup as easy as possible.
    </v-card-text>
    <v-card-actions class="justify-end">
      <v-btn color="success" text>Ok</v-btn>
      <v-btn color="info" text>Cancel</v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  // 컴포넌트의 대표이름(devtools에 나오는 이름)
  name: "About",
  // 추가하고 싶은 컴포넌트 등록(import something from "/path")
  components: {},
  // 컴포넌트 데이터 정의
  data() {
    return {};
  },
  // 컴포넌트 메소드 정의
  methods: {},
};
</script>