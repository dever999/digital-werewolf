<template>
  <section class="container">
    <div class="extension">
      <p>SOCIAL</p>
      <div>
        <img src="../assets/images/aside-icons/add-friend.png" />
        <img src="../assets/images/aside-icons/add-folder.png" />
        <img src="../assets/images/aside-icons/options.png" />
        <img src="../assets/images/aside-icons/search.png" />
      </div>
    </div>
    <div class="extension-group">
      <ul>
        <li class="group-flag">
          <img src="../assets/images/aside-icons/main-group-flag.png" />
        </li>
        <li class="group-sign">XXXX</li>
        <li class="group-name">Group Name</li>
      </ul>
      <ul>
        <li class="group-flag">
          <img src="../assets/images/aside-icons/group-flag.png" />
        </li>
        <li class="group-sign">XXXX</li>
        <li class="group-name">Group Name</li>
      </ul>
      <ul>
        <li class="group-flag">
          <img src="../assets/images/aside-icons/group-flag.png" />
        </li>
        <li class="group-sign">XXXX</li>
        <li class="group-name">Group Name</li>
      </ul>
    </div>
    <p class="extension-general">
      {{
        `GENERAL (${this.$store.state.activeFriend}/${this.$store.state.totalFriend})`
      }}
    </p>
    <div class="near-contact">
      <ul v-for="index in totalFriend" :key="index">
        <li>
          <img
            src="https://opgg-static.akamaized.net/images/profile_icons/profileIcon4770.jpg?image=q_auto:best&v=1518361200"
          />
          <div class="near-contact-statusIcon"></div>
          <div>
            <span class="near-contact-name">{{ index.name }}</span>
            <span class="near-contact-statusLabel">Online</span>
          </div>
        </li>
      </ul>
    </div>
    <div class="function-tool">
      <div class="chat">
        <img src="../assets/images/aside-icons/chat.png" alt="chat" />
      </div>
      <div class="mission">
        <img src="../assets/images/aside-icons/missions.png" alt="mission" />
      </div>
      <div class="voice">
        <img src="../assets/images/aside-icons/voice.png" alt="voice" />
      </div>
      <div class="version">
        <h4><a href="https://github.com/digital-werewolf">V2.0</a></h4>
      </div>
      <div class="bug">
        <img src="../assets/images/aside-icons/bug.png" alt="bug" />
      </div>
    </div>
  </section>
</template>

<script>
import totalFriend from "../data/totalFriend.json";
export default {
  data() {
    return {
      totalFriend,
    };
  },
};
</script>

<style scoped>
ul {
  list-style: none;
}
.container {
  position: absolute;
  right: 0;
  width: 232px;
  max-height: 100%;
  background: rgba(0, 0, 30, 0.75);
  padding: 0;
}
.extension {
  width: 100%;
  height: 30px;
  display: flex;
  align-items: center;
  background: rgba(252, 204, 211, 0.125);
  padding: 0;
  grid-gap: 50px;
  font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
  font-weight: bold;
  letter-spacing: 1px;
  position: fixed;
}
.extension > div {
  display: flex;
  grid-gap: 10px;
}
.extension > div > img {
  width: 16px;
  height: 11px;
  cursor: pointer;
}
.extension-group {
  padding: 0;
  margin-top: 30px;
  height: 150px;
}
.extension-group:hover {
  overflow-y: auto;
}
.extension-group > ul {
  width: 100%;
  height: 40px;
  display: flex;
  align-items: center;
  grid-gap: 10px;
  font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
  margin: 0;
  padding: 7px 0;
  transition: 0.3s;
}
.extension-group > ul:hover,
.function-tool > div:hover,
.near-contact > ul > li:hover {
  cursor: pointer;
  background: rgba(255, 255, 255, 0.212);
}
.extension-group-flag > img {
  width: 30px;
  height: 30px;
}
.extension-general {
  text-align: start;
  background: rgba(252, 204, 211, 0.125);
}
.near-contact {
  height: 250px;
  padding: 7px 0;
  margin: 0;
  overflow-y: auto;
}
.near-contact > ul {
  padding: 7px 0;
  margin: 0;
}
.near-contact > ul > li {
  display: flex;
  grid-gap: 7px;
}
.near-contact > ul > li > img {
  width: 37px;
  height: 37px;
  border-radius: 50%;
  border: 2px solid #c5a971;
}
.near-contact > ul > li > div {
  display: grid;
  text-align: start;
}
.near-contact-name {
  color: gray;
  font-weight: bold;
  font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
}
.near-contact-statusLabel {
  color: rgb(0, 209, 0);
}
.function-tool {
  position: fixed;
  height: 50px;
  width: 100%;
  display: flex;
}
.function-tool .version {
  color: gray;
  border: none;
}
.function-tool .version > h4 > a {
  color: gray;
  text-decoration: none;
}
.function-tool > div {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 10px 13px;
  border: 1px solid #c5a971;
}
.function-tool > div > img {
  width: 16px;
}
::-webkit-scrollbar {
  width: 4px;
}
::-webkit-scrollbar,
::-webkit-scrollbar-track {
  background: transparent;
}
::-webkit-scrollbar-thumb {
  background: #785a28;
  border-radius: 300px;
}
</style>
