## 1. Tổng quan hệ thống

Tên dự án: Meeting Room Booking System

#### Mục tiêu:

- Giúp user đặt / hủy / chỉnh sửa lịch phòng họp.

- Admin quản lý toàn bộ phòng, thiết bị, người dùng

- Thông báo (email) + đồng bộ với calendar cá nhân

#### Phân vai:

- User (nhân viên): Đăng nhập, đặt phòng, hủy, xem lịch

- Admin: Quản lý danh sách phòng, thiết bị, user, thống kê

## 2. Cấu trúc Site

### User site:

| Page           | Chức năng chính                                          |
| -------------- | -------------------------------------------------------- |
| `/login`       | Đăng nhập qua SSO/Google                                 |
| `/dashboard`   | Trang chính, hiển thị tổng quan các phòng và trạng thái  |
| `/rooms`       | Danh sách phòng họp (lọc theo tầng, sức chứa, thiết bị)  |
| `/rooms/:id`   | Chi tiết 1 phòng (lịch trống/đã đặt, thiết bị, sức chứa) |
| `/book-room`   | Form đặt phòng (chọn thời gian, người tham dự, nội dung) |
| `/my-bookings` | Danh sách cuộc họp đã đặt, cho phép sửa/hủy              |
| `/calendar`    | Xem lịch cá nhân (tuần/tháng)                            |
| `/profile`     | Thông tin người dùng, đồng bộ Google/Outlook calendar    |

### Admin site

| Page               | Chức năng chính                                      |
| ------------------ | ---------------------------------------------------- |
| `/admin/login`     | Đăng nhập quản trị                                   |
| `/admin/dashboard` | Thống kê số phòng, lượt đặt, tỷ lệ sử dụng           |
| `/admin/rooms`     | Quản lý danh sách phòng (thêm/sửa/xóa)               |
| `/admin/rooms/:id` | Cập nhật chi tiết phòng (vị trí, thiết bị, sức chứa) |
| `/admin/users`     | Quản lý người dùng (phân quyền, active/inactive)     |
| `/admin/settings`  | Cấu hình tích hợp (Slack/Email/Calendar API)         |

## Kiến trúc tổng quan

![Diagram](./Untitled%20diagram-2025-10-21-022257.png)

## Danh sách task
