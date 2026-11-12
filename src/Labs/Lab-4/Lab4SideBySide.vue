<template>
  <div class="container mt-4 mb-5">
    <div class="text-center mb-4">
      <h3 class="fw-bold text-primary">Mô phỏng 2 View trực quan theo đúng 2 ảnh đề bài</h3>
      <p class="text-muted">Chế độ hiển thị song song 2 trạng thái Trước và Sau thao tác (Before & After) có mũi tên minh họa</p>
    </div>

    <!-- View 1: Theo ảnh 2 đề bài (Luồng Thêm Sách - Bài 1 & 2) -->
    <div class="card p-4 shadow-sm mb-5 border">
      <h4 class="card-title text-success border-bottom pb-2 mb-4">
        1. View Ảnh 1 (Đề bài phần I): Thêm sách mới vào thư viện
      </h4>
      <div class="row align-items-center">
        <!-- Cột trước khi thêm -->
        <div class="col-md-5">
          <div class="p-3 border rounded bg-light">
            <h5 class="fw-bold mb-3">Thêm sách mới vào thư viện</h5>
            <div class="mb-3">
              <label class="form-label">Tiêu đề</label>
              <input type="text" class="form-control" value="Đắc Nhân Tâm" readonly />
            </div>
            <div class="mb-3">
              <label class="form-label">Tác giả</label>
              <input type="text" class="form-control" value="Dale Carnegie" readonly />
            </div>
            <div class="mb-3">
              <label class="form-label">Thể loại</label>
              <select class="form-select" disabled>
                <option selected>Phát triển bản thân</option>
              </select>
            </div>
            <button class="btn btn-primary">Thêm sách</button>
          </div>
        </div>

        <!-- Mũi tên xanh -->
        <div class="col-md-2 text-center my-3 my-md-0">
          <div class="d-inline-block p-2 bg-primary text-white rounded-circle shadow">
            <span class="fs-4">➔</span>
          </div>
          <div class="small text-muted mt-1 fw-bold">Nhấn Thêm sách</div>
        </div>

        <!-- Cột sau khi thêm -->
        <div class="col-md-5">
          <div class="p-3 border rounded bg-light">
            <h5 class="fw-bold mb-3">Thêm sách mới vào thư viện</h5>
            <div class="mb-3">
              <label class="form-label">Tiêu đề</label>
              <input type="text" class="form-control" placeholder="Nhập tiêu đề" readonly />
            </div>
            <div class="mb-3">
              <label class="form-label">Tác giả</label>
              <input type="text" class="form-control" placeholder="Nhập tác giả" readonly />
            </div>
            <div class="mb-3">
              <label class="form-label">Thể loại</label>
              <select class="form-select" disabled>
                <option selected>Chọn thể loại</option>
              </select>
            </div>
            <button class="btn btn-primary mb-3">Thêm sách</button>

            <h5 class="fw-bold">Danh sách</h5>
            <div class="card p-3 border">
              <h6 class="fw-bold mb-1">Đắc Nhân Tâm</h6>
              <p class="mb-1 text-muted">Tác giả: Dale Carnegie</p>
              <p class="mb-0 text-muted">Thể loại: Phát triển bản thân</p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- View 2: Theo ảnh 1 đề bài (Luồng Cập Nhật Sách - Bài 4) -->
    <div class="card p-4 shadow-sm border">
      <h4 class="card-title text-warning border-bottom pb-2 mb-4">
        2. View Ảnh 2 (Đề bài phần II): Cập nhật sách (Chỉnh sửa thông tin)
      </h4>
      <div class="row align-items-center">
        <!-- Cột trạng thái ban đầu -->
        <div class="col-md-5">
          <div class="p-3 border rounded bg-light">
            <h5 class="fw-bold mb-3">Thêm sách mới vào thư viện</h5>
            <div class="mb-3">
              <label class="form-label">Tiêu đề</label>
              <input type="text" class="form-control" placeholder="Nhập tiêu đề" readonly />
            </div>
            <div class="mb-3">
              <label class="form-label">Tác giả</label>
              <input type="text" class="form-control" placeholder="Nhập tác giả" readonly />
            </div>
            <div class="mb-3">
              <label class="form-label">Thể loại</label>
              <select class="form-select" disabled>
                <option selected>Chọn thể loại</option>
              </select>
            </div>
            <div class="mb-3">
              <label class="form-label">Số lượng</label>
              <input type="number" class="form-control" value="1" readonly />
            </div>
            <button class="btn btn-primary mb-3">Thêm sách</button>

            <h5 class="fw-bold">Danh sách sách</h5>
            <div class="card p-3 border d-flex flex-row justify-content-between align-items-center">
              <div>
                <h6 class="fw-bold mb-1">Đắc Nhân Tâm</h6>
                <p class="mb-1 small">Tác giả: Dale Carnegie</p>
                <p class="mb-1 small">Thể loại: Phát triển bản thân</p>
                <p class="mb-0 small">Số lượng: 10</p>
              </div>
              <div>
                <button class="btn btn-sm btn-warning me-1">Sửa</button>
                <button class="btn btn-sm btn-danger">Xóa</button>
              </div>
            </div>
          </div>
        </div>

        <!-- Mũi tên xanh -->
        <div class="col-md-2 text-center my-3 my-md-0">
          <div class="d-inline-block p-2 bg-primary text-white rounded-circle shadow">
            <span class="fs-4">➔</span>
          </div>
          <div class="small text-muted mt-1 fw-bold">Nhấn nút Sửa</div>
        </div>

        <!-- Cột trạng thái khi nhấn Sửa -->
        <div class="col-md-5">
          <div class="p-3 border rounded bg-light">
            <h5 class="fw-bold mb-3 text-primary">Cập nhật sách</h5>
            <div class="mb-3">
              <label class="form-label">Tiêu đề</label>
              <input type="text" class="form-control" value="Đắc Nhân Tâm" readonly />
            </div>
            <div class="mb-3">
              <label class="form-label">Tác giả</label>
              <input type="text" class="form-control border-primary" value="Dale Carnegie" readonly />
            </div>
            <div class="mb-3">
              <label class="form-label">Thể loại</label>
              <select class="form-select" disabled>
                <option selected>Phát triển bản thân</option>
              </select>
            </div>
            <div class="mb-3">
              <label class="form-label">Số lượng</label>
              <input type="number" class="form-control" value="10" readonly />
            </div>
            <div class="mb-3">
              <button class="btn btn-primary me-2">Cập nhật sách</button>
              <button class="btn btn-secondary">Hủy</button>
            </div>

            <h5 class="fw-bold">Danh sách sách</h5>
            <div class="card p-3 border d-flex flex-row justify-content-between align-items-center">
              <div>
                <h6 class="fw-bold mb-1">Đắc Nhân Tâm</h6>
                <p class="mb-1 small">Tác giả: Dale Carnegie</p>
                <p class="mb-1 small">Thể loại: Phát triển bản thân</p>
                <p class="mb-0 small">Số lượng: 10</p>
              </div>
              <div>
                <button class="btn btn-sm btn-warning me-1">Sửa</button>
                <button class="btn btn-sm btn-danger">Xóa</button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
