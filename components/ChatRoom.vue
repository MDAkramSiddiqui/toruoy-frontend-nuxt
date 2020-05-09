<template>
  <div>
    <el-card class="box-card">
      <div slot="header" class="clearfix">
        <span>ChatRoom Name</span>
        <el-button
          style="float: right;"
          margin="15px"
          type="danger"
          round
          size="mini"
        >
          Delete
        </el-button>
      </div>
      <div class="msger">
        <main class="msger-chat">
          <div v-for="o in 40" :key="o" class="text item">
            <div class="msg left-msg" v-if="parseInt(o) > 10">
              <div class="msg-bubble">
                <div class="msg-info">
                  <div class="msg-info-name">BOT</div>
                  <div class="msg-info-time">12:45</div>
                </div>

                <div class="msg-text">
                  Hi, welcome to SimpleChat! Go ahead and send me a message. 😄
                </div>
              </div>
            </div>

            <div class="msg right-msg" v-else>
              <div class="msg-bubble">
                <div class="msg-info">
                  <div class="msg-info-name">Sajad</div>
                  <div class="msg-info-time">12:46</div>
                </div>

                <div class="msg-text">
                  You can change your name in JS section!
                </div>
              </div>
            </div>
          </div>
        </main>
      </div>

      <div>
        <form class="msger-inputarea">
          <input
            type="text"
            class="msger-input"
            placeholder="Enter your message..."
          />
          <button type="submit" class="msger-send-btn">Send</button>
        </form>
      </div>
    </el-card>
  </div>
</template>

<script>
export default {};
</script>
<style>
.text {
  font-size: 14px;
}

.item {
  margin: 18px 0;
}

.clearfix:before,
.clearfix:after {
  display: table;
  content: "";
}
.clearfix:after {
  clear: both;
}

.msger {
  display: flex;
  flex-flow: column wrap;
  justify-content: space-between;
  width: 100%;
  height: 55vh;
}

.msger-chat {
  flex: 1;
  overflow-y: scroll;
  padding: 10px;
}

.msger-chat::-webkit-scrollbar {
  width: 6px;
}
.msger-chat::-webkit-scrollbar-track {
  background: #ddd;
}
.msger-chat::-webkit-scrollbar-thumb {
  border-radius: 100px;
  background: #bdbdbd;
}
.msg {
  display: flex;
  align-items: flex-end;
  margin-bottom: 10px;
}
.msg:last-of-type {
  margin: 0;
}

.msg-bubble {
  max-width: 450px;
  padding: 15px;
  border-radius: 15px;
  background: rgb(118, 221, 118);
}
.msg-info {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 10px;
}
.msg-info-name {
  margin-right: 10px;
  font-weight: bold;
}
.msg-info-time {
  font-size: 0.85em;
}

.left-msg .msg-bubble {
  border-bottom-left-radius: 0;
}

.right-msg {
  flex-direction: row-reverse;
}
.right-msg .msg-bubble {
  background: rgb(107, 183, 235);
  color: #fff;
  border-bottom-right-radius: 0;
}

.right-msg .msg-img {
  margin: 0 0 0 10px;
}

.msger-inputarea {
  display: flex;
  padding: 10px;

  background: #eee;
}

.msger-inputarea * {
  padding: 10px;
  border: none;
  border-radius: 3px;
  font-size: 1em;
}
.msger-input {
  flex: 1;
  background: #ddd;
}
.msger-send-btn {
  margin-left: 10px;
  background: rgb(0, 196, 65);
  color: #fff;
  font-weight: bold;
  cursor: pointer;
  transition: background 0.23s;
}
.msger-send-btn:hover {
  background: rgb(0, 180, 50);
}
</style>
