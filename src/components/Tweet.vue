
<template>
  <div class="tweet">
    <ProfileImage :image="tweets.user.image"/>

    <div class="body">
      <div class="top">
        <User :name="tweets.user.name" :handle="tweets.user.handle"/>
        <TimeStamp :time="tweets.timestamp"/>
      </div>

      <Message :message="tweets.message"/>

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
