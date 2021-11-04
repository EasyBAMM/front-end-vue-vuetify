<!-- 컴포넌트 UI 정의 -->
<template>
  <v-app>
    <v-app-bar app hide-on-scroll>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>Title</v-toolbar-title>
      <v-spacer></v-spacer
      ><v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>
      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" absolute temporary>
      <v-list nav dense>
        <v-list-item>
          <v-list-item-content>
            <v-list-item-title class="text-h6"> Application </v-list-item-title>
            <v-list-item-subtitle>Vue + Vuetify</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
        <v-divider></v-divider>

        <v-list-item-group active-class="deep-purple--text text--accent-4">
          <v-list-item to="/">
            <v-list-item-icon>
              <v-icon>mdi-home</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>Home</v-list-item-title>
            </v-list-item-content>
          </v-list-item>

          <v-list-item to="/about">
            <v-list-item-icon>
              <v-icon>mdi-help-box</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>About</v-list-item-title>
            </v-list-item-content>
          </v-list-item>

          <v-list-group :value="false" prepend-icon="mdi-palette-outline" >
            <template v-slot:activator>
              <v-list-item-content>
                <v-list-item-title>Styles</v-list-item-title>
              </v-list-item-content>
            </template>
            <v-list-item to="/styles/textandtypography" >
              <v-list-item-title >Text and Typography</v-list-item-title>
            </v-list-item>
            <v-list-item to="/styles/spacing">
              <v-list-item-title>Margin and Padding</v-list-item-title>
            </v-list-item>
          </v-list-group>

          <v-list-item to="/gridsystem">
            <v-list-item-icon>
              <v-icon>mdi-view-grid-outline</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>Grid System</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <v-container fluid>
        <router-view></router-view>
      </v-container>
    </v-main>
    <v-footer color="secondary" dark> <div class="mx-auto">H.J.B</div></v-footer>
  </v-app>
</template>

<script>
export default {
  // 컴포넌트의 대표이름(devtools에 나오는 이름)
  name: "App",
  // 추가하고 싶은 컴포넌트 등록(import something from "/path")
  components: {},
  // 컴포넌트 데이터 정의
  data() {
    return { drawer: false };
  },
  // 컴포넌트 메소드 정의
  methods: {},
};
</script>

<!-- 컴포넌트 스타일 정의 -->
<style scoped>
/* scoped: 전역 범위X, 컴포넌트 범위 */
</style>