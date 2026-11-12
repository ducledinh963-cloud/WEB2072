<script setup>
import { ref } from "vue";
import Bai1 from "./Labs/Lab-4/Bai1-BookForm.vue";
import Bai2 from "./Labs/Lab-4/Bai2.vue";
import Bai3 from "./Labs/Lab-4/Bai3.vue";
import Bai4 from "./Labs/Lab-4/Bai4.vue";
import Lab4SideBySide from "./Labs/Lab-4/Lab4SideBySide.vue";

// Biến điều khiển hiển thị bài đang chọn (1, 2, 3, 4, 'side-by-side' hoặc 'all')
const currentTab = ref(1);
</script>

<template>
  <div id="app" class="bg-white min-vh-100 d-flex flex-column">
    <!-- Thanh chọn bài tối giản, nền trắng hoàn toàn -->
    <div class="border-bottom py-2 bg-white sticky-top shadow-sm">
      <div class="container d-flex justify-content-center gap-2">
        <button
          class="btn btn-sm"
          :class="currentTab === 1 ? 'btn-primary' : 'btn-outline-secondary'"
          @click="currentTab = 1"
        >
          Bài 1
        </button>
        <button
          class="btn btn-sm"
          :class="currentTab === 2 ? 'btn-primary' : 'btn-outline-secondary'"
          @click="currentTab = 2"
        >
          Bài 2
        </button>
        <button
          class="btn btn-sm"
          :class="currentTab === 3 ? 'btn-primary' : 'btn-outline-secondary'"
          @click="currentTab = 3"
        >
          Bài 3
        </button>
        <button
          class="btn btn-sm"
          :class="currentTab === 4 ? 'btn-primary' : 'btn-outline-secondary'"
          @click="currentTab = 4"
        >
          Bài 4
        </button>
        <button
          class="btn btn-sm"
          :class="currentTab === 'side-by-side' ? 'btn-primary' : 'btn-outline-secondary'"
          @click="currentTab = 'side-by-side'"
        >
          View 2 ảnh đề bài
        </button>
        <button
          class="btn btn-sm"
          :class="currentTab === 'all' ? 'btn-primary' : 'btn-outline-secondary'"
          @click="currentTab = 'all'"
        >
          Xem tất cả
        </button>
      </div>
    </div>

    <!-- Khu vực hiển thị nội dung từng bài -->
    <main class="py-4 flex-grow-1">
      <div v-if="currentTab === 1 || currentTab === 'all'" class="mb-5">
        <div v-if="currentTab === 'all'" class="container border-bottom pb-2 mb-3">
          <h4 class="text-secondary">Bài 1</h4>
        </div>
        <Bai1 />
      </div>

      <div v-if="currentTab === 2 || currentTab === 'all'" class="mb-5">
        <div v-if="currentTab === 'all'" class="container border-bottom pb-2 mb-3">
          <h4 class="text-secondary">Bài 2</h4>
        </div>
        <Bai2 />
      </div>

      <div v-if="currentTab === 3 || currentTab === 'all'" class="mb-5">
        <div v-if="currentTab === 'all'" class="container border-bottom pb-2 mb-3">
          <h4 class="text-secondary">Bài 3</h4>
        </div>
        <Bai3 />
      </div>

      <div v-if="currentTab === 4 || currentTab === 'all'" class="mb-5">
        <div v-if="currentTab === 'all'" class="container border-bottom pb-2 mb-3">
          <h4 class="text-secondary">Bài 4</h4>
        </div>
        <Bai4 />
      </div>

      <div v-if="currentTab === 'side-by-side'">
        <Lab4SideBySide />
      </div>
    </main>

    <!-- Thông tin sinh viên ở chân trang -->
    <footer class="text-center py-3 text-muted border-top mt-auto bg-light">
      <small>Sinh viên thực hiện: <strong>Lê Đình Đức</strong> - MSSV: <strong>PA00493</strong> | Lab 4 - WEB2072</small>
    </footer>
  </div>
</template>

<style scoped>
button {
  min-width: 80px;
}
</style>
