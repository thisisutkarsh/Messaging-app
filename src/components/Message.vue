<template>
  <div class="main-header">
    <div class="info">
      <div class="name">Anna Smith</div>
      <div class="time">May 12, 2020</div>
    </div>
  </div>
  <div class="other">
    <div class="avatar"></div>
    <div class="main-content">
      <div class="msg-box">
        <p>Hello Everyone, Good Morning</p>
      </div>
      <div class="msg-box">
        <p>
          Lorem Ipsum is simply dummy text of the printing and typesetting
          industry. Lorem Ipsum has been the industry's standard dummy text ever
          since the 1500s, when an unknown printer took a galley of type and
          scrambled it to make a type specimen book. It has survived not only
          five centuries.
        </p>
      </div>
      <div class="sent">2 min ago</div>
    </div>
  </div>
  <div class="self">
    <div class="main-content">
      <div class="msg-box">
        Hello Everyone, Good Morning
      </div>
      <div class="sent">1 min ago</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Message",
};
</script>

<style scoped>
.main-header {
  display: flex;
  align-items: center;
  color: #43434b;
  padding: 20px;
  font-size: 20px;
  border-bottom: 1px solid #43434b;
  height: 64px;
  margin-bottom: 40px;
}

.info {
  display: flex;
  align-items: flex-start;
  justify-content: center;
  flex-direction: column;
}
.name {
  font-size: 18px;
  font-weight: bold;
}
.time {
  font-size: 12px;
  margin-top: 4px;
  font-weight: 400;
}

.other,
.self {
  display: flex;
  margin-bottom: 35px;
}
.avatar {
  border-radius: 50%;
  height: 35px;
  min-width: 35px;
  background-color: #e5e5e5;
  margin-right: 15px;
}

.msg-box {
  color: #fff;
  font-size: 14px;
  line-height: 30px;
  padding: 15px;
  width: fit-content;
  border-radius: 0 10px;
  background-color: #1d7bc0;
  margin-bottom: 16px;
}

.sent {
  display: flex;
  justify-content: flex-end;
  margin-top: -5px;
  font-size: 12px;
  color: #2d3545;
}

.self {
  justify-content: flex-end;
}

.self .msg-box {
  background-color: #fff;
  color: #000;
  border: 1px solid #e5e5e5;
}

.main-content {
  max-width: 75%;
}
</style>
