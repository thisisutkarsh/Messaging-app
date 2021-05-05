<template>
  <div class="chat">
    <div class="side">
      <div class="side-header">
        <p>All Messages</p>
      </div>
      <div class="scroll">
        <ChatContent></ChatContent>
        <ChatContent></ChatContent>
        <ChatContent></ChatContent>
        <ChatContent></ChatContent>
        <ChatContent></ChatContent>
        <ChatContent></ChatContent>
        <ChatContent></ChatContent>
        <ChatContent></ChatContent>
        <ChatContent></ChatContent>
        <ChatContent></ChatContent>
        <ChatContent></ChatContent>
        <ChatContent></ChatContent>
        <ChatContent></ChatContent>
        <ChatContent></ChatContent>
        <ChatContent></ChatContent>
      </div>
    </div>
    <div class="main">
      <Message></Message>

      <div class="write-area">
        <input
          type="text"
          class="write-input"
          placeholder="Type message here"
        />
        <div class="btn">
          <i class="material-icons">send</i>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ChatContent from "./components/ChatContent.vue";
import Message from "./components/Message";

export default {
  name: "App",
  components: {
    ChatContent,
    Message,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Comfortaa:wght@400;500;600;700&display=swap");
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: "Comfortaa", cursive;
}

#app {
  background-color: #fff;
}

.chat {
  display: grid;
  grid-template-columns: 300px 1fr;
  grid-template-rows: 1fr;
  grid-column-gap: 10px;
  grid-template-areas: "side main";
  height: 100vh;
  width: 100%;
}

.side {
  grid-area: side;
  font-weight: 600;
  border-right: 1px solid #f1f1f1;
}
.main {
  grid-area: main;
}

.side-header {
  display: flex;
  align-items: center;
  font-size: 20px;
  color: #43434b;
  border-bottom: 1px solid #43434b;
  padding: 20px;
}

.scroll {
  /* overflow-y: scroll; */
}

.write-area {
  width: 100%;
  padding: 0 20px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.write-input {
  border: 1px solid #f1f1f1;
  outline: 0;
  padding: 24px 20px;
  flex-grow: 1;
}

.btn {
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
  height: 30px;
  min-width: 30px;
  border-radius: 50%;
  background-color: #1d7bc0;
  color: #fff;
}
</style>
