<template>
  <div class="chatRoom bg-white">
      <div class="headerOfChatRoom d-flex border-bottom">
        <div class="RoomChatAvatar">
          <div class="rounded-circle bg-secondary" style="height: 43px;"></div>
        </div>
        <div class="NameRoomChat text-start ">
          <span class="align-middle p-2 fw-bold" style="line-height: 65px;">Vũ Văn Thắng</span>
        </div>
      </div>
      <div class="bodyOfChatRoom" v-on:drag="loadChat">
        <!-- <div class="message"> -->
          <p class="send text-start mx-5 text-white">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Incidunt veritatis vitae aperiam quod iusto quibusdam recusandae quia perspiciatis corrupti iste explicabo velit minima officiis accusamus adipisci maiores, saepe vel in.</p>
          <p class="receive text-start mx-5 text-black">Lorem ipsum do class="receive"or sit, amet consectetur adipisicing elit. Incidunt veritatis vitae aperiam quod iusto quibusdam recusandae quia perspiciatis corrupti iste explicabo velit minima officiis accusamus adipisci maiores, saepe vel in.</p>
          <p class="send text-start mx-5 text-white">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Incidunt veritatis vitae aperiam quod iusto quibusdam recusandae quia perspiciatis corrupti iste explicabo velit minima officiis accusamus adipisci maiores, saepe vel in.</p>
          <p class="send text-start mx-5 text-white">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Incidunt veritatis vitae aperiam quod iusto quibusdam recusandae quia perspiciatis corrupti iste explicabo velit minima officiis accusamus adipisci maiores, saepe vel in.</p>
          <p class="receive text-start mx-5 text-black">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Incidunt veritatis vitae aperiam quod iusto quibusdam recusandae quia perspiciatis corrupti iste explicabo velit minima officiis accusamus adipisci maiores, saepe vel in.</p>
          <p class="send text-start mx-5 text-white">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Incidunt veritatis vitae aperiam quod iusto quibusdam recusandae quia perspiciatis corrupti iste explicabo velit minima officiis accusamus adipisci maiores, saepe vel in.</p>
          <p class="receive text-start mx-5 text-black">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Incidunt veritatis vitae aperiam quod iusto quibusdam recusandae quia perspiciatis corrupti iste explicabo velit minima officiis accusamus adipisci maiores, saepe vel in.</p>
          <p class="send text-start mx-5 text-white">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Incidunt veritatis vitae aperiam quod iusto quibusdam recusandae quia perspiciatis corrupti iste explicabo velit minima officiis accusamus adipisci maiores, saepe vel in.</p>
          <p class="receive text-start mx-5 text-black">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Incidunt veritatis vitae aperiam quod iusto quibusdam recusandae quia perspiciatis corrupti iste explicabo velit minima officiis accusamus adipisci maiores, saepe vel in.</p>
          <p class="send text-start mx-5 text-white">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Incidunt veritatis vitae aperiam quod iusto quibusdam recusandae quia perspiciatis corrupti iste explicabo velit minima officiis accusamus adipisci maiores, saepe vel in.</p>
          <p class="send text-start mx-5 text-white">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Incidunt veritatis vitae aperiam quod iusto quibusdam recusandae quia perspiciatis corrupti iste explicabo velit minima officiis accusamus adipisci maiores, saepe vel in.</p>
          <p class="receive text-start mx-5 text-black" id="loadPlace">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Incidunt veritatis vitae aperiam quod iusto quibusdam recusandae quia perspiciatis corrupti iste explicabo velit minima officiis accusamus adipisci maiores, saepe vel in.</p>
        <!-- </div> -->
        
      </div>
      <div class="footerOfChatRoom">
          <form class="d-flex my-custom-input">
            <button class="btn bg-white circle-btn rounded-circle" v-on:click.prevent="$parent.DisplayKeDonThuoc = false" style="line-height: 38px" type="submit" title="Kê đơn thuốc">
              <i class="fa fa-wpforms fs-5" aria-hidden="true"></i>
            </button>
            <input
              class="form-control ms-1 rounded-pill backgroung-input"
              type="message"
              placeholder="Aa"
              aria-label="message"
            />
            <button class="btn bg-white circle-btn rounded-circle" type="submit">
              <i
                class="fa fa-paper-plane fs-5"
                aria-hidden="true"
                title="Gữi"
                style="color: #0084FF;"
              ></i>
            </button>
          </form>
      </div>
  </div>
</template>
<script>

export default {
  mounted() {
      this.loadChat()
    },
  name: 'ChatRoom',
  data() {
    return {

    };
  },
  methods: {
    loadChat: function() {
      document.getElementById("loadPlace").scrollIntoView();
      // console.log("Abc");
    },
    
  }
  // computed: {
  //   setDisplayKeDonThuoc: function() {
  //     console.log("abc")
  //   }
  // }
}
</script>

<style scoped>
.chatRoom {
  height: cale(100% - 70px) !important;
  margin-left: 27%;
  width: 73%;
}

.headerOfChatRoom {
  position: sticky;
  height: 65px;
  /* background-color: aqua; */
}
.bodyOfChatRoom {
  position: fixed;
  overflow: hidden scroll;
  height: calc(100% - 190px);
}
.footerOfChatRoom {
  height: 60px;
  position: fixed;
  bottom: 0;
  width: 73%;
  padding: 12px 0;
  box-sizing: border-box;
}
.send {
  width: 60%;
  float: right;
  border-radius: 18px;
  padding: 8px 12px !important;
  background-color: #0084FF !important;
}
.receive {
  width: 60%;
  float: left;
  border-radius: 18px;
  padding: 8px 12px !important;
  background-color: #E4E6EB !important;
}

.my-custom-input {
  height: 36px !important;
}
.sendd {
  position: relative;
  display: unset;
  bottom: 0px;
  
}

.RoomChatAvatar {
  width: 65px;
  height:65px;
  padding: 11px 6px 11px 16px;
}

.NameRoomChat {
  width: calc(100% - 65px);
}
.circle-btn {
  width: 36px;
  height: 36px;
  padding: 0px 9px;
  margin: 0 10px;
}

.circle-btn:hover {
  background-color: #F0F2F5 !important;
  width: 36px;
  height: 36xp;
}

</style>