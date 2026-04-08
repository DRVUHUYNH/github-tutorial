# Hướng dẫn clone repository của người khác về máy và đẩy lên repository private của bản thân

## Mục tiêu

Tài liệu này hướng dẫn cách:

1. lấy code từ một repository GitHub của người khác về máy,
2. tạo một repository mới của riêng mình trên GitHub,
3. đặt repository đó ở chế độ private,
4. đẩy toàn bộ code lên repository private của mình.

Cách này không phải là fork.  
Đây là cách sao chép code về máy trước, sau đó đưa nó sang repository riêng của mình.

---

## Khi nào nên dùng cách này

Nên dùng cách này khi bạn muốn:

- lưu một bản riêng của code trên GitHub cá nhân,
- để repository ở chế độ private,
- chỉnh sửa và phát triển theo mục đích riêng,
- không muốn dùng fork công khai trên GitHub.

---

## Những khái niệm cần hiểu trước

### 1. Repository là gì

Repository, thường gọi ngắn là repo, là thư mục chứa code và lịch sử thay đổi của code.

Có thể hiểu đơn giản:
- thư mục bình thường chỉ chứa file,
- repo là thư mục có thêm khả năng theo dõi lịch sử chỉnh sửa bằng Git.

### 2. Git là gì

Git là công cụ quản lý phiên bản code.

Git giúp:
- lưu lại từng lần sửa,
- quay lại bản cũ nếu cần,
- đẩy code lên GitHub.

### 3. GitHub là gì

GitHub là nơi lưu repository trên mạng.

Có thể hiểu:
- Git là công cụ làm việc,
- GitHub là nơi chứa repo online.

### 4. Clone là gì

`git clone` nghĩa là tải một repository từ GitHub về máy tính của bạn.

Clone chỉ tải repo về máy.  
Clone không tạo repo mới trên GitHub của bạn.

### 5. Remote là gì

Remote là đường dẫn kết nối giữa repo trên máy và repo trên GitHub.

Thường có tên:
- `origin`: repo chính mà máy đang liên kết tới,
- `upstream`: repo gốc ban đầu, thường dùng khi muốn theo dõi repo của người khác.

---

## Điều kiện cần trước khi làm

Trước khi bắt đầu, cần có:

1. tài khoản GitHub của bạn,
2. Git đã được cài trên máy,
3. VS Code hoặc Terminal để thao tác,
4. đã đăng nhập GitHub,
5. nếu dùng SSH để push, cần SSH key đã cấu hình.

---

## Kiểm tra Git đã cài chưa

Mở Terminal và chạy:

```bash
git --version