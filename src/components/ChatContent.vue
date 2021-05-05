<template>
  <div
    class="chat-content"
    @click="toggleClass()"
    :class="{ 'active-chat': isActive }"
  >
    <div
      class="avatar"
      @click="toggleClass()"
      :class="{ 'active-avatar': isActive }"
    ></div>

    <div class="info">
      <div class="info-header">
        <div
          class="name"
          @click="toggleClass()"
          :class="{ 'active-name': isActive }"
        >
          Anna Smith
        </div>
        <div class="time">
          Now
        </div>
      </div>
      <div class="message">
        Lorem ipsum dolor sit amet
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ChatContent",
  data() {
    return {
      isActive: false,
    };
  },

  methods: {
    toggleClass() {
      this.isActive = !this.isActive;
    },
  },
};
</script>

<style scoped>
.chat-content {
  display: flex;
  align-items: center;
  padding: 20px;
  border-bottom: 1px solid #f1f1f1;
  cursor: pointer;
  font-weight: 600;
  border-right: 4px solid #f1f1f1;
}

.avatar {
  border-radius: 50%;
  height: 35px;
  min-width: 35px;
  background-color: #e5e5e5;
  margin-right: 15px;
}

.info-header {
  display: flex;
  justify-content: space-between;
}

.name {
  font-size: 16px;
  color: #2c3e50;
}
.time {
  font-size: 12px;
  color: #2d3545;
}
.message {
  font-size: 12px;
  color: #2c3e50;
  margin-top: 12px;
}

.active-chat {
  border-right: 4px solid #1d30df;
  color: #2d3545;
  font-weight: bold;
}

.active-name {
  color: #1d30df;
  font-weight: bold;
}

.active-avatar {
  background-color: #707070;
}
</style>
