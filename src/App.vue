<template>
  <KeDonThuoc  v-bind:class="{ 'd-none': DisplayKeDonThuoc}"/>
  <ComponentHeader/>
  <div class="mycontainer bg-white">
    <sidebar />
    <ChatRoom />
  </div>
</template>

<script>
import ComponentHeader from './components/Component.vue';
import sidebar from './components/sidebar.vue';
import ChatRoom from './components/chat-room.vue';
import KeDonThuoc from './components/KeDonThuoc.vue';
export default {
  name: 'App',
  components: {
    ComponentHeader,
    sidebar,
    ChatRoom,
    KeDonThuoc
  },
  data: function () {
    return {
      DisplayKeDonThuoc: true
    }
  },
  methods: {
    // prescriptions
  }
}
</script>

<style>
body, html {
  padding: 0;
  margin: 0;
  width: 100%;
  height: 100%;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  width: 100%;
  height: 100%;
}
.mycontainer {
  position: relative;
  /* padding: 70px 0 0 0 !important; */
  margin: 0 !important;
  height: calc(100% - 70px);
  box-sizing: border-box;
  width: 100%;
  display: flex;
}
.backgroung-input {
  background-color: #F0F2F5;
}
.form-control:focus {
  /* color: #212529; */
  background-color: #F0F2F5;
  outline: 0;
  box-shadow: unset;
}
::-webkit-scrollbar {
  width: 10px;
}

/* Track */
::-webkit-scrollbar-track {
  background: #f1f1f1; 
}
 
/* Handle */
::-webkit-scrollbar-thumb {
  background: #888; 
  border-radius: 10px;
}
.fontsize-07rem {
  font-size: 0.7rem;
}
.m-box-sizing {
  box-sizing: border-box;
}

</style>
