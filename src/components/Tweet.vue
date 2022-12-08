
<template>
  <div class="tweet" v-for="tweet in tweets">
    <ProfileImage :image="tweet.user.image"/>
    <div class="body">
      <div class="top">
        <User :name="tweet.user.name" :handle="tweet.user.handle"/>
        <TimeStamp :time="tweet.timestamp"/>
      </div>
      <Message :message="tweet.message"/>
     <Action/>
    </div>
    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<script>
  import ProfileImage from './ProfileImage.vue'; 
  import TimeStamp from './TimeStamp.vue';
  import User from './User.vue';
  import Message from './Message.vue';
  import Action from './Action.vue';
  export default {
    props:["tweets"],
    components:{ ProfileImage, TimeStamp, User, Message, Action },
  };

</script>
<style scoped>
a {
  color: #42b983;
}
</style>
