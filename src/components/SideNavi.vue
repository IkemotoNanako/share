<template>
<div>
    <div class="left-padding">
        <img class="logo" src="../assets/logo.png"/>
        <div class="flex icon-field"  @click="$router.push('/home')">
          <img class="icon" src="../assets/home.png" alt/>
          <p>ホーム</p>
        </div>
        <div class="flex icon-field" @click="$router.push('/profile')">
          <img class="icon" src="../assets/profile.png" alt/>
          <p>プロフィール</p>
        </div>
        <div class="flex icon-field"  @click="$store.dispatch('logout')">
          <img class="icon" src="../assets/logout.png" alt/>
          <p>ログアウト</p>
        </div>
        </div>
      <hr />
      <ShereMessage />
    </div>
</template>
<script>
import ShereMessage from "../components/ShareMessage"
export default {
    components: {
        ShereMessage
    }
}
</script>
<style scoped>
.left-padding {
  margin: 20px;
}
.flex {
    display: flex;
}
.logo {
  width: 100px;
}
.icon-field {
  margin-top: 15px;
  cursor: pointer;
}
.icon {
    width: 25px;
}
.icon-field p {
  font-size: 16px;
  padding-left: 15px;
}
@media screen and (max-width: 480px) {
  .logo {
   width: 150px;
  }
  .icon {
    width: 30px;
  }
}
</style>
