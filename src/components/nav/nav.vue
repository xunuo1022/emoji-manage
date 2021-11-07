<template>
  <div>
    <el-radio-group
      v-model="isCollapse"
      style="margin-bottom: 20px"
    ></el-radio-group>
    <el-menu
      default-active="1-4-7"
      class="el-menu-vertical-demo"
      @open="handleOpen"
      @close="handleClose"
      :collapse="isCollapse"
    >
      <el-submenu :index="index1">
        <template slot="title">
          <i class="el-icon-user"></i>
          <span slot="title">Emoji和动物</span>
        </template>
        <el-menu-item-group>
          <el-menu-item :index="index1_1" ref="index1_1" @click="getIndex1_1">
            <i class="el-icon-s-grid"></i>
            <span slot="title">Emoji</span>
          </el-menu-item>
          <el-menu-item :index="index1_2" ref="index1_2" @click="getIndex1_2">
            <i class="el-icon-star-off"></i>
            <span slot="title">动物</span>
          </el-menu-item>
        </el-menu-item-group>
      </el-submenu>
      <el-submenu :index="index2">
        <template slot="title">
          <i class="el-icon-fork-spoon"></i>
          <span slot="title">食物和植物</span>
        </template>
        <el-menu-item-group>
          <el-menu-item :index="index2_1" ref="index2_1" @click="getIndex2_2">
            <i class="el-icon-coffee"></i>
            <span slot="title">食物</span>
          </el-menu-item>
          <el-menu-item :index="index2_2" ref="index2_2" @click="getIndex2_1">
            <i class="el-icon-headset"></i>
            <span slot="title">植物</span>
          </el-menu-item>
        </el-menu-item-group>
      </el-submenu>
      <el-submenu :index="index3">
        <template slot="title">
          <i class="el-icon-shopping-cart-2"></i>
          <span slot="title">交通地点和天气</span>
        </template>
        <el-menu-item-group>
          <el-menu-item :index="index3_1" ref="index3_1" @click="getIndex3_1">
            <i class="el-icon-shopping-cart-2"></i>
            <span slot="title">交通</span>
          </el-menu-item>
          <el-menu-item :index="index3_2" ref="index3_2" @click="getIndex3_2">
            <i class="el-icon-price-tag"></i>
            <span slot="title">地点</span>
          </el-menu-item>
          <el-menu-item :index="index3_3" ref="index3_3" @click="getIndex3_3">
            <i class="el-icon-umbrella"></i>
            <span slot="title">天气</span>
          </el-menu-item>
        </el-menu-item-group>
      </el-submenu>
      <el-submenu :index="index4">
        <template slot="title">
          <i class="el-icon-shopping-cart-2"></i>
          <span slot="title">庆祝和物品</span>
        </template>
        <el-menu-item-group>
          <el-menu-item :index="index4_1" ref="index4_1" @click="getIndex4_1">
            <i class="el-icon-present"></i>
            <span slot="title">庆祝</span>
          </el-menu-item>
          <el-menu-item :index="index4_2" ref="index4_2" @click="getIndex4_2">
            <i class="el-icon-umbrella"></i>
            <span slot="title">物品</span>
          </el-menu-item>
        </el-menu-item-group>
      </el-submenu>
      <el-menu-item :index="index5" ref="index5" @click="getIndex5">
        <i class="el-icon-female"></i>
        <span slot="title">人</span>
      </el-menu-item>
    </el-menu>
  </div>
</template>

<style scoped>
.el-menu-vertical-demo:not(.el-menu--collapse) {
  width: 200px;
  min-height: 1224px;
  border-top: 1.5px solid #f5f5f5;
  transition: 0.5s;
  position: fixed;
  margin-top: 70px;
}

.el-menu {
  border-right: none;
}

div {
  float: left;
}
</style>

<script>
import bus from "../eventBus.js";

export default {
  data() {
    return {
      isCollapse: false,
      index1: "1",
      index1_1: "1-1",
      index1_2: "1-2",
      index2: "2",
      index2_1: "2-1",
      index2_2: "2-2",
      index3: "3",
      index3_1: "3-1",
      index3_2: "3-2",
      index3_3: "3-3",
      index4: "4",
      index4_1: "4-1",
      index4_2: "4-2",
      index5: "5",
    };
  },
  methods: {
    handleOpen(key, keyPath) {
      console.log();
    },
    handleClose(key, keyPath) {
      console.log();
    },
    getIndex1_1() {
      bus.$emit("share", this.$refs.index1_1.index);
    },
    getIndex1_2() {
      bus.$emit("share", this.$refs.index1_2.index);
    },
    getIndex2_1() {
      bus.$emit("share", this.$refs.index2_1.index);
    },
    getIndex2_2() {
      bus.$emit("share", this.$refs.index2_2.index);
    },
    getIndex3_1() {
      bus.$emit("share", this.$refs.index3_1.index);
    },
    getIndex3_2() {
      bus.$emit("share", this.$refs.index3_2.index);
    },
    getIndex3_3() {
      bus.$emit("share", this.$refs.index3_3.index);
    },
    getIndex4_1() {
      bus.$emit("share", this.$refs.index4_1.index);
    },
    getIndex4_2() {
      bus.$emit("share", this.$refs.index4_2.index);
    },
    getIndex5() {
      bus.$emit("share", this.$refs.index5.index);
    },
  },
};
</script>
