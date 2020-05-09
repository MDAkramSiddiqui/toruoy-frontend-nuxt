<template>
  <div>
    <nav>
      <el-menu
        class="el-menu-demo"
        mode="horizontal"
        background-color="#545c64"
        text-color="#fff"
        active-text-color="#ffd04b"
      >
        <el-menu-item index="1">Create UserID</el-menu-item>
        <el-menu-item index="2">Create Room</el-menu-item>
        <el-menu-item index="3" @click="joinDisplay = !joinDisplay">
          Join Room
        </el-menu-item>
      </el-menu>
    </nav>
    <div class="join-room">
      <el-card>
        <el-form ref="form">
          <el-form-item label="ChatRoom Name">
            <el-input></el-input>
          </el-form-item>
          <el-form-item label="ChatRoom Password">
            <el-input placeholder="Password"></el-input>
          </el-form-item>
        </el-form>
        <el-button type="primary" round>Submit</el-button>
        <el-button type="success" native-type="reset" round>Reset</el-button>
      </el-card>
    </div>
    <nuxt />
  </div>
</template>

<script>
export default {
  data() {
    return {
      joinDisplay: false
    };
  }
};
</script>

<style>
html {
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI",
    Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

body {
  overflow: hidden;
}

.join-room {
  position: absolute;
  display: block;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 400px;
}
</style>
