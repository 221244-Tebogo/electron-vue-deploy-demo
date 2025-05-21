<script setup>
import { ref, onMounted } from 'vue'

const selectedImage = ref('https://cdn.pixabay.com/photo/2024/05/09/04/11/flamingo-8749724_1280.jpg')
const MessageTo = ref('Michaela')
const Message = ref('We’re on the last lap! Let’s cruise through the bugs, and vibe through the chaos')
const MessageFrom = ref('Tebogo')

</script>

<template>
  <div class="fullscreen-message" :style="`background-image: url('${selectedImage}');`">
    <div class="message-content">
      <h4>To {{ MessageTo }},</h4>
      <h2>
        {{ Message }}
      </h2>
      <h5>Sincerely,<br/>{{ MessageFrom }}</h5>
    </div>
  </div>

</template>


<style scoped>
body {
  color: black;
}

.fullscreen-message {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 2rem;
  z-index: 0;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}


.message-content {
  z-index: 2;
  font-family: sans-serif;
  font-size: 2rem;
  line-height: 1.5;
  color: white;
}

.fullscreen-message::before {
  content: '';
  position: absolute;
  inset: 0;
  background-color: rgba(0, 0, 0, 0.6);
  z-index: 0;
  color: white;
}
</style>
