# 🚀 Lộ Trình Tự Học Kỹ Sư Hệ Thống Nhúng (Embedded Systems Roadmap)

Chào mừng bạn đến với lộ trình tự học trở thành **Kỹ sư Hệ thống Nhúng** từ con số 0. Repo này được thiết kế nhằm cung cấp một chương trình học bài bản, chi tiết, đi từ gốc đến ngọn tương đương (hoặc sâu hơn) chương trình đại học, giúp bạn có đủ kiến thức thực tế để làm việc tại các doanh nghiệp mà không cần qua trường lớp chính quy.

---

## 🗺️ Bản Đồ Lộ Trình Tổng Quan

Lộ trình được chia làm **3 Khối kiến thức lớn** bao gồm **9 Học phần biệt lập**. Để không bị ngợp, bạn nên học cuốn chiếu theo thứ tự từ Học phần 1 đến Học phần 9. Mỗi học phần sẽ có một Repo con chi tiết chứa tài liệu, video bài giảng và bài tập thực hành riêng được tụi mình tổng hợp từ nhiều nguồn.

[Khối 1: Nền Tảng Cốt Lõi]

├── Học phần 1: Kỹ thuật Điện tử Cơ bản & Linh kiện 🔌

├── Học phần 2: Kiến trúc Máy tính & Hệ thống số 💻

└── Học phần 3: Lập trình C chuyên sâu cho Embedded 🦀

👇

[Khối 2: Lập Trình Vi Điều Khiển]

├── Học phần 4: Vi điều khiển & Lập trình Bare-Metal (STM32) 📑

├── Học phần 5: Giao tiếp Ngoại vi & Giao thức Truyền thông 📡

└── Học phần 6: Cấu trúc dữ liệu & Giải thuật ứng dụng 📊

👇

[Khối 3: Hệ Điều Hành & Nâng Cao]

├── Học phần 7: Hệ điều hành thời gian thực (RTOS) ⏱️

├── Học phần 8: Linux nhúng (Embedded Linux) 🐧

└── Học phần 9: Dự án Tốt nghiệp / Portfolio 🏆

---

## 📚 Chi Tiết Các Học Phần & Liên Kết Lớp Học

| Học Phần | Nội Dung Trọng Tâm | Trạng Thái | Liên Kết Repo Con |
| :--- | :--- | :---: | :--- |
| **HP 1: Điện Tử Cơ Bản** | Định luật Ohm, Đọc Schematic, Transistor, ADC, Mạch nguồn, Cách dùng Vạn năng kế/Oscilloscope. | 🟢 Sẵn sàng | [Xem chi tiết tại đây (Đang cập nhật link)](#) |
| **HP 2: Kiến Trúc Máy Tính** | Hệ nhị phân/Hex, Cổng logic, Thanh ghi dịch, Kiến trúc CPU (ARM/Harvard), Tổ chức bộ nhớ RAM/Flash. | 🟢 Sẵn sàng | [Xem chi tiết tại đây (Đang cập nhật link)](#) |
| **HP 3: Lập Trình C Nhúng** | Thao tác Bit, Con trỏ nâng cao, Từ khóa `volatile`/`static`, Struct/Union, Quy trình biên dịch (Makefile). | 🟢 Sẵn sàng | [Xem chi tiết tại đây (Đang cập nhật link)](#) |
| **HP 4: Bare-Metal (STM32)** | Đọc Datasheet/Reference Manual, Cấu hình thanh ghi GPIO, Ngắt (Interrupt), Timer/PWM (Không dùng thư viện HAL). | 🟡 Đang soạn | [Xem chi tiết tại đây (Đang cập nhật link)](#) |
| **HP 5: Giao Thức Truyền Thông** | Tìm hiểu bản chất và lập trình driver cho các chuẩn: UART, I2C, SPI, cơ chế DMA. | 🟡 Đang soạn | [Xem chi tiết tại đây (Đang cập nhật link)](#) |
| **HP 6: DSA Trong Nhúng** | Quản lý bộ nhớ Stack/Heap, Hàng đợi vòng (Ring Buffer), Mô hình trạng thái (FSM), Bộ lọc nhiễu tín hiệu. | 🟡 Đang soạn | [Xem chi tiết tại đây (Đang cập nhật link)](#) |
| **HP 7: FreeRTOS** | Tư duy đa nhiệm (Multi-tasking), Task, Semaphore, Mutex, Queue, Quản lý tài nguyên tránh Deadlock. | 🔴 Chờ duyệt | [Xem chi tiết tại đây (Đang cập nhật link)](#) |
| **HP 8: Linux Nhúng** | Hệ điều hành Linux (CLI), Bootloader (U-Boot), Linux Kernel, RootFS, Lập trình Driver cơ bản. | 🔴 Chờ duyệt | [Xem chi tiết tại đây (Đang cập nhật link)](#) |
| **HP 9: Capstone Project** | Hướng dẫn làm sản phẩm thực tế (IoT Gateway, Trạm cảm biến...) để làm đẹp CV xin việc. | 🔴 Chờ duyệt | [Xem chi tiết tại đây (Đang cập nhật link)](#) |

*Chú thích trạng thái: 🟢 Đã hoàn thành | 🟡 Đang cập nhật nội dung | 🔴 Lộ trình dự kiến.*

---

## 🧰 Bộ Phần Cứng Khuyến Nghị (Hardware Kit)

Để học Nhúng, bạn **bắt buộc phải thực hành trên phần cứng**. Đừng chỉ đọc lý thuyết! Dưới đây là các linh kiện rẻ, phổ biến mà bạn nên chuẩn bị dần:

1. **Khối 1 (Điện tử):** 
   * 1 x Đồng hồ vạn năng số (Digital Multimeter - loại rẻ khoảng 150k-200k).
   * 1 x Breadboard (Bo test mạch) + Dây cắm (Đực-Đực, Cái-Cái).
   * Combo linh kiện cơ bản: Điện trở (100, 1k, 10k Ohm), Đèn LED, Biến trở, Transistor NPN (2N3904 hoặc C1815).
2. **Khối 2 & 3 (Vi điều khiển & RTOS):**
   * 1 x Kit phát triển **STM32F401RE Nucleo** hoặc **STM32F103C8T6 (Blue Pill)**. *Khuyến nghị dùng dòng STM32F4 Nucleo vì có sẵn mạch nạp ST-Link và rất chuẩn công nghiệp.*
   * 1 x Mạch nạp ST-Link V2 (Nếu dùng Blue Pill).
   * Module ngoại vi: 1 x Cảm biến nhiệt độ độ ẩm (DHT11 hoặc TMP102 giao tiếp I2C), 1 x Màn hình OLED I2C/SPI 0.96 inch.
3. **Khối Linux Nhúng:**
   * 1 x Máy tính nhúng **Raspberry Pi 3 Model B+** hoặc **Raspberry Pi 4** (kèm thẻ nhớ MicroSD tối thiểu 16GB).

---

## 🤝 Cách Đóng Góp (Contribution)

Dự án này là hoàn toàn miễn phí và vì cộng đồng. Nếu bạn là một Kỹ sư Nhúng có kinh nghiệm và muốn chia sẻ:
1. Hãy mở một **Issue** nếu phát hiện sai sót kiến thức hoặc link tài liệu bị hỏng.
2. **Fork** repo này, bổ sung các nguồn tài liệu chất lượng (Video, Sách, Bài viết) và tạo **Pull Request**.


