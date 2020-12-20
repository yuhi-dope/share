<template>
  <div class="flex">
    <div class="left">
      <SideNavi />
    </div>
    <div class="right">
      <div class="title">
        <p>プロフィール</p>
      </div>
      <div class="profile">
        <div class="flex-profile">
          <p class="profile-name">{{name}}</p>
          <div @click="edit">
            <button>変更する</button>
          </div>
        </div>
        <p class="text" v-if="active">{{profile}}</p>
        <input type="text" v-model="profile" v-else />
      </div>
      <Message />
    </div>
  </div>
</template>

<script>
import SideNavi from "../components/SideNavi";
import Message from "../components/Message";
export default {
  data() {
    return {
      active: true,
      name: "taro",
      profile: "私は太郎です"
    };
  },
  components: {
    SideNavi,
    Message
  }
}
</script>

<style scoped>
.flex{
  display: flex;
}
.left{
  width: 20%;
  height: 100vh;
}
.right{
  width: 80%;
  height: 100vh;
}
.profile {
  padding: 20px;
  border-bottom: solid 1px white;
  border-left: solid 1px white;
}
.flex-profile {
  display: flex;
  justify-content: space-between;
}
.profile-name{
  font-size: 24px;
}
.title{
  border-bottom: 1px solid white;
}
.title p {
  font-size: 20px;
  font-weight: bold;
}
button{
  width: 100px;
  color: white;
  background-color: #5419da;
  border-radius: 15px;
  display: block;
  margin: 0 0 0 auto;
}
</style>