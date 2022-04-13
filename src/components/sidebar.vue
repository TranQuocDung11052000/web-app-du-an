<template>
  <div class="content bg-white border-end">
    <!-- thanh tìm kiếm và title thanh chat -->
    <div class="topSidebar">
      <h3 class="text-start fw-bold p-2">Chat</h3>
      <form class="d-flex">
        <input
          class="form-control mx-2 mb-2 rounded-pill backgroung-input"
          type="search"
          placeholder="Search"
          aria-label="Search"
        />
      </form>
    </div>
    <!-- kết thúc thanh tìm kiếm và title thanh chat -->

    <!-- danh sách phòng chat và phòng chat -->
    <div class="listRooms">
        <!-- danh sách phòng chat -->
        <div class="roomChatShortcut px-2 d-flex my-2" v-for='index in 10' :key='index'>

          <!-- avatar  -->
          <div class="roomAvatar rounded-circle"></div>
          <!-- end avatar -->

          <!-- room name và tin nhắn gần nhất -->
          <div class="roomName text-start py-1 ps-3">
            <span class="fs-6">Vũ Văn Thắng</span>
            <p
              class="fw-ligher lastMessage"
              style="font-size: 0.8rem !important"
            >
              Bạn: Lorem ipsum dolor sit amet consectetur, adipisicing elit.
              Placeat itaque assumenda totam unde. Error officia ducimus
              assumenda sit adipisci, dicta libero. Beatae, corrupti? Nihil
              neque aut esse, vero deserunt perferendis.
            </p>
          </div>
          <!-- kết thúc room name và tin nhắn gần nhất -->
        </div>
        <!-- kết thúc danh sách phòng chat -->
    </div>
    <!-- kết thúc danh sách phòng chat và phòng chat -->
  </div>
</template>

<script>
export default {
  name: "SideBar",
  props: {
    msg: String,
  },
};
</script>

<style scoped>
.content {
  position: fixed;
  height: 100%;
  min-width: 27%;
  max-width: 27%;
}

.listRooms {
  max-height: 450px;
  overflow-y: scroll;
  /* border-top: 1px solid gray; */
}
/* width */

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: #555; 
}

.roomChatShortcut {
  height: 70px;
  width: 100%;
  box-sizing: border-box;
  cursor: pointer;

  /* display: inline-block;/ */
}

.roomAvatar {
  min-width: 70px;
  height: 70px;
  background-color: #777;
}

.roomName {
  width: calc(100% - 70px);
}
.roomName .lastMessage {
  display: block;
  display: -webkit-box;
  -webkit-line-clamp: 1; /* số dòng hiển thị */
  -webkit-box-orient: vertical;
  overflow: hidden;
  text-overflow: ellipsis;
}


</style>