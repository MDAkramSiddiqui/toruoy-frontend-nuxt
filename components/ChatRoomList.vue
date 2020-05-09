<template>
  <div>
    <el-row class="tac" style="margin-top:20px;">
      <el-col>
        <el-menu class="el-menu-vertical">
          <el-submenu index="1">
            <template slot="title">
              <i class="el-icon-chat-line-square"></i>
              <span>ChatRooms Created</span>
            </template>
            <el-menu-item-group>
              <el-menu-item index="1-1">
                <el-row style="width:85%;">
                  <el-col> item one</el-col>
                  <el-button size="mini" margin=" 0 15px" type="danger" round>
                    Del
                  </el-button>
                </el-row>
              </el-menu-item>
            </el-menu-item-group>
          </el-submenu>
          <hr />
          <el-submenu index="2">
            <template slot="title">
              <i class="el-icon-chat-line-square"></i>
              <span>ChatRooms Joined</span>
            </template>
            <el-menu-item-group>
              <el-menu-item index="2-1">
                <el-row style="width:85%;">
                  <el-col> item one</el-col>
                  <el-button size="mini" margin=" 0 15px" type="primary" round>
                    Leave
                  </el-button>
                </el-row>
              </el-menu-item>
            </el-menu-item-group>
          </el-submenu>
        </el-menu>

        <hr />

        <div class="button-center">
          <el-button type="danger" plain style="margin-top: 20px;">
            Delete Everything
          </el-button>
        </div>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  methods: {
    handleOpen(key, keyPath) {
      console.log(key, keyPath);
    },
    handleClose(key, keyPath) {
      console.log(key, keyPath);
    }
  }
};
</script>

<style>
.button-center {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
</style>
