<template>
  <div id="app" class="container">
    <!-- <h1></h1> -->

    <div>
      <!-- 直接获取状态 -->
      <!-- getters 更多的返回二次处理的状态 -->
      <MemoEditor v-if="$store.state.isMemoEditorVisibility" />
      <MemuBar />
      <ItemList />
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import MemuBar from "./components/MenuBar.vue";
import ItemList from "./components/ItemList.vue";
import MemoEditor from "./components/MemoEditor.vue";

@Component({
  components: {
    MemuBar,
    ItemList,
    MemoEditor,
  },
})
export default class App extends Vue {}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
