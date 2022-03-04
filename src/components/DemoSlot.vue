<template>
  <div class="demo-slot">
    <comp-tab title="Tieu de cua Tab">
      <ul class="tab-header">
        <li
          v-for="(item,index) in tabHeader"
          v-bind:key="index"
          v-on:click="setActiveTab(index)"> {{ item.text }}
        </li>
      </ul>

      <div class="tab-content" v-if="tabActive ===0">
        <li>
          Trước khi xem video và thực hiện bước này, hãy dành 1 ít thời gian thư giãn toàn thân. Hãy hít sâu và thở nhẹ,
          đều ra nhiều lần.
          Hãy mở video. Mục tiêu của bạn là nhìn tập trung vào dấu chấm đen nhỏ ở giữa màn hình càng lâu càng tốt.
          Nếu đầu óc bạn bắt đầu lang thang đâu đó, hãy dừng bài tập, thư giãn và tập trung lại từ đầu.
          Hãy lấy tờ giấy và cây viết ra để theo dõi thời gian bắt đầu cho đến thời gian mất tập trung mỗi lần để xem sự
          tiến bộ của bạn.
          Đừng ngạc nhiên khi mắt bạn cảm giác được những vầng hào quang xung quanh các vòng tròn màu. Đây cũng là cách
          để bạn thực tập nhận biết hào quang nhưng cố đừng để những tạp niệm phát sinh.
        </li>
      </div>
      <div class="tab-content" v-if="tabActive ===1">
        <li>
          Nếu bạn không có thời gian thì mỗi ngày chỉ cần thực tập từ 5-10 lần là được.
          Đối với người mới tập, đạt được 5 phút tập trung không có suy nghĩ phát sinh là tuyệt vời.
          Khi khả năng tập trung của bạn dần phát triển, bạn sẽ thấy thời gian 15 hay 30 phút trôi qua trong tích tắc.
        </li>
      </div>
      <div class="tab-content" v-if="tabActive ===2">
        <li>
          Luyện tập thường xuyên bước tập trung này cho đến khi bạn có thể duy trì việc tập trung suy nghĩ vào một điều
          duy nhất trong khoảng từ 5 phút trở lên, bạn có thể bước vào nhiều lĩnh vực khác như thiền định dễ dàng. Đây
          cũng là bước cần thiết cho chương trình thu hút tiền bạc, giàu có và thịnh vượng.
        </li>
      </div>
    </comp-tab>
  </div>
</template>

<script>
import compTab from "./CompTab";

export default {
  name: "DemoSlot",
  data() {
    return {
      tabHeader: [
        {text: 'Tab1'},
        {text: 'Tab2'},
        {text: 'Tab3'},
      ],
      tabActive: 1
    }
  },
  components: {
    compTab
  },
  methods: {
    setActiveTab(index) {
      this.tabActive = index;
    }
  }
}
</script>

<style scoped>
.demo-slot {
  margin-top: 10px;
  padding: 10px 30px;
  border: 1px solid blue;
}

.tab-content {
  display: flex;
  justify-content: space-between;
}

.tab-content li {
  display: flex;
  justify-content: center;
  padding: 20px;
}
</style>
