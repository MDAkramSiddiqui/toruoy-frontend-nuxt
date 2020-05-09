<template>
  <el-container>
    <el-aside width="250px"><ChatRoomList /></el-aside>
    <el-container>
      <el-main><ChatRoom /></el-main>
      <el-footer></el-footer>
    </el-container>
  </el-container>
</template>

<script>
import ChatRoom from "./../../../components/ChatRoom";
import ChatRoomList from "./../../../components/ChatRoomList";
export default {
  components: {
    ChatRoom,
    ChatRoomList
  }
};
</script>
