<template>
    <div class="tweet">
        <ProfileImage :image="props.tweet.user.image" />
       
        <div class="body">
            <div class="top">
             
                <User :name="props.tweet.user.name" :hanfle="props.tweet.user.name" />
               
                
                <Timestamp :timestamp="props.tweet.timestamp" />
           
            </div>

                <Message :message="props.tweet.message" />


            <div class="actions">
                <!-- Font Awesome icons -->
                <i class="far fa-comment"></i>
                <i class="fas fa-retweet"></i>
                <i class="far fa-heart"></i>
                <i class="fas fa-share"></i>
            </div>
        </div>

        <i class="fas fa-ellipsis-h"></i>
    </div>
</template>
  
<script setup>

import {defineProps} from 'vue'

const props = defineProps({
    tweet: Object
  
})

</script>



<style scoped>
a {
    color: #42b983;
}
</style>