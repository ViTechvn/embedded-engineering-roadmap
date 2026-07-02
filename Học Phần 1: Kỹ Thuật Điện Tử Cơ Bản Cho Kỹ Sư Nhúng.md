# 🔌 Học Phần 1: Kỹ Thuật Điện Tử Cơ Bản Cho Kỹ Sư Nhúng

Repo này chứa lộ trình chi tiết, tài liệu học tập, và các bài tập thực hành từ con số 0 của môn **Kỹ thuật Điện tử Cơ bản**. 

Mục tiêu của học phần này không phải biến bạn thành một nhà thiết kế mạch chuyên nghiệp, mà là cung cấp cho bạn **"đôi mắt" để đọc hiểu phần cứng** và **"tư duy" để cô lập lỗi (debug)** khi hệ thống nhúng gặp sự cố.

---

## 🛠️ Công Cụ Cần Chuẩn Bị Trước Khi Học

Để hoàn thành các bài thực hành trong học phần này, bạn cần chuẩn bị các công cụ sau:
*   **Phần mềm mô phỏng (Miễn phí):** [LTSpice](https://www.analog.com/en/resources/design-tools-and-calculators/ltspice-simulator.html) hoặc [Proteus](https://www.labcenter.com/) (Dùng để test mạch ảo trước khi cắm mạch thật).
*   **Phần cứng thực tế:** 1 x Breadboard, 1 x Đồng hồ vạn năng số (Digital Multimeter), Dây cắm, Hộp linh kiện cơ bản (LED, Điện trở nhiều trị số, Tụ điện, Transistor BJT C1815/A1015, Relay 5V, Biến trở 10k).

---

## 🗺️ Lộ Trình Chi Tiết Đến Từng Bài Học

### 📍 Chương 1: Đại Lượng Điện Học & Định Luật Nền Tảng (Bài 1 - Bài 3)

#### 📝 Bài 1: Bản chất của Dòng điện, Điện áp và Điện trở
*   **Mục tiêu:** Hiểu rõ điện áp là gì (hiệu điện thế), dòng điện chạy thế nào, và điện trở cản trở ra sao dưới góc nhìn trực quan (mô hình dòng nước). Phân biệt dòng một chiều (DC) và xoay chiều (AC).
*   **Từ khóa tra cứu:** *Voltage, Current, Resistance, Alternating Current vs Direct Current.*
*   **Tài liệu & Video bài giảng:**
    *   🎬 [Video: Bản chất điện áp và dòng điện - Kênh Việt Nam](#) *(Bạn tự điền link)*
    *   📖 [Bài viết: Khái niệm cơ bản về điện học - SparkFun](#) *(Bạn tự điền link)*
*   **Thực hành:** Sử dụng đồng hồ vạn năng (VOM) đo điện áp của cục pin 1.5V, viên pin 9V. Đo điện trở của một con trở bất kỳ và đọc vạch màu.

#### 📝 Bài 2: Định luật Ohm & Định luật Kirchhoff (KVL, KCL)
*   **Mục tiêu:** Làm chủ 3 công thức tối quan trọng để tính toán mạch điện: $U = I \times R$, tổng dòng tại một nút bằng 0 (KCL), và tổng áp trong một vòng kín bằng 0 (KVL). Biết cách tính điện trở tương đương khi mắc nối tiếp/song song.
*   **Từ khóa tra cứu:** *Ohm's Law, Kirchhoff's Voltage Law (KVL), Kirchhoff's Current Law (KCL).*
*   **Tài liệu & Video bài giảng:**
    *   🎬 [Video: Giải thích trực quan định luật Kirchhoff - Khan Academy](#)
*   **Thực hành:** Vẽ một mạch gồm 3 điện trở mắc hỗn hợp trên phần mềm mô phỏng. Tính toán lý thuyết dòng/áp qua mỗi trở rồi dùng que đo ảo để kiểm chứng xem có khớp không.

#### 📝 Bài 3: Ứng dụng Thực Tế - Mạch phân áp & Điện trở hạn dòng
*   **Mục tiêu:** Biết cách tính toán điện trở để bảo vệ LED không bị cháy. Biết cách thiết kế mạch phân áp để hạ điện áp tín hiệu một cách an toàn.
*   **Từ khóa tra cứu:** *Voltage Divider Circuit, LED Current Limiting Resistor.*
*   **Tài liệu & Video bài giảng:**
    *   🎬 [Video: Cách tính điện trở cho LED và Mạch phân áp](#)
*   **Thực hành:** 
    *   *Bài toán 1:* Tính điện trở hạn dòng cho LED đỏ ($V_f = 2V$, $I = 15mA$) khi dùng nguồn 5V. Cắm mạch thật trên Breadboard để kiểm chứng.
    *   *Bài toán 2:* Thiết kế mạch phân áp dùng 2 điện trở để hạ điện áp từ 5V xuống đúng 3.3V (Mức áp giao tiếp của STM32).

---

### 📍 Chương 2: Linh Kiện Thụ Động Nâng Cao (Bài 4 - Bài 6)

#### 📝 Bài 4: Tụ điện (Capacitor) & Hiện tượng nạp xả
*   **Mục tiêu:** Hiểu cách tụ điện tích trữ năng lượng. Phân biệt tụ gốm (không phân cực) và tụ hóa (phân cực). Hiểu công thức hằng số thời gian $\tau = R \times C$.
*   **Từ khóa tra cứu:** *Capacitor physics, RC Time Constant, Electrolytic vs Ceramic Capacitor.*
*   **Thực hành:** Mô phỏng mạch nạp xả tụ điện qua một điện trở. Vẽ biểu đồ đồ thị điện áp trên tụ theo thời gian để thấy đường cong nạp/xả.

#### 📝 Bài 5: Cuộn cảm (Inductor) & Biến áp
*   **Mục tiêu:** Hiểu hiện tượng cảm ứng điện từ. Cách cuộn cảm sinh ra dòng điện chống lại sự thay đổi của dòng điện qua nó. Khái niệm về hiện tượng quá áp do ngắt dòng đột ngột (Inductive Kickback) - nguyên nhân gây cháy chip hàng đầu.
*   **Từ khóa tra cứu:** *Inductor working principle, Inductive Kickback.*
*   **Thực hành:** Mô phỏng một mạch điện đóng cắt dòng qua cuộn cảm và quan sát đỉnh điện áp (voltage spike) sinh ra khi ngắt công tắc.

#### 📝 Bài 6: Ứng dụng Thực Tế - Mạch lọc nguồn & Mạch chống rung (Debouncing)
*   **Mục tiêu:** Hiểu tại sao luôn có tụ điện đặt cạnh chân nguồn của vi điều khiển (Tụ lọc nguồn - Decoupling Capacitor). Biết cách dùng mạch RC để chống rung cho nút nhấn bằng phần cứng.
*   **Từ khóa tra cứu:** *Decoupling/Bypass Capacitor, Hardware Button Debouncing circuit.*
*   **Thực hành:** Cắm mạch một nút nhấn nối vào đèn LED. Thêm một tụ điện $0.1\mu F$ song song với nút bấm để quan sát tín hiệu điện áp mượt mà hơn khi bấm, loại bỏ hiện tượng nhiễu gai.

---

### 📍 Chương 3: Linh Kiện Bán Dẫn & Mạch Động Lực (Bài 7 - Bài 10)

#### 📝 Bài 7: Diode Thường, Diode Zener & LED
*   **Mục tiêu:** Hiểu tính chất dẫn điện một chiều của diode (Van điện một chiều). Cách dùng Diode Zener để ghim áp cố định.
*   **Từ khóa tra cứu:** *PN Junction, Diode forward voltage, Zener Diode voltage regulation.*
*   **Thực hành:** Cắm mạch dùng Diode bảo vệ chống cắm ngược dòng. Thử cắm ngược nguồn và kiểm tra xem mạch phía sau có được bảo vệ an toàn không.

#### 📝 Bài 8: Transistor BJT (NPN & PNP) làm Công tắc điện tử
*   **Mục tiêu:** Hiểu cách dùng một dòng điện rất nhỏ ở chân Base (B) để đóng cắt một dòng điện lớn ở chân Collector (C) và Emitter (E). Nắm chắc điều kiện để BJT rơi vào trạng thái "Bão hòa" (Mở hoàn toàn) để làm công tắc.
*   **Từ khóa tra cứu:** *BJT Saturation, BJT as a switch, Transistor C1815.*
*   **Thực hành:** Tính toán điện trở chân Base ($R_B$) để dùng một dòng điện 5mA kích mở BJT, điều khiển bật một bóng đèn/quạt nhỏ 9V tiêu thụ 200mA.

#### 📝 Bài 9: Ứng dụng Thực Tế - Điều khiển Relay & Diode dập xung (Flyback Diode)
*   **Mục tiêu:** Hiểu cấu tạo của Relay (Rơ-le) cách ly cơ khí. **Bắt buộc:** Hiểu tại sao phải mắc một con Diode ngược chiều song song với cuộn dây của Relay để bảo vệ Transistor không bị đánh thủng.
*   **Từ khóa tra cứu:** *Relay driving circuit, Flyback Diode/Snubber Diode.*
*   **Thực hành:** Thiết kế hoàn chỉnh mạch dùng BJT để kích đóng/ngắt một Relay 5V. Đo điện áp tại chân C của Transistor lúc đóng và lúc ngắt để thấy giá trị của Diode dập xung.

#### 📝 Bài 10: Linh kiện MOSFET nâng cao
*   **Mục tiêu:** Phân biệt MOSFET (điều khiển bằng điện áp) và BJT (điều khiển bằng dòng điện). Tại sao mạch nhúng hiện đại lại dùng MOSFET để đóng cắt dòng lớn (động cơ, mạch sưởi) thay vì BJT. Khái niệm "Logic-Level MOSFET" (loại MOSFET mở hoàn toàn ở mức áp 3.3V/5V của vi điều khiển).
*   **Từ khóa tra cứu:** *MOSFET N-channel vs P-channel, Gate-Source Threshold Voltage, Logic-level MOSFET.*
*   **Thực hành:** Mô phỏng mạch dùng MOSFET IRF540 (hoặc tương đương) để điều khiển tốc độ động cơ bằng cách thay đổi điện áp kích vào chân Gate.

---

### 📍 Chương 4: Mạch Nguồn & Cách Ly Tín Hiệu (Bài 11 - Bài 12)

#### 📝 Bài 11: Mạch Nguồn Tuyến Tính (Linear Regulator)
*   **Mục tiêu:** Hiểu nguyên lý hoạt động của các IC nguồn hạ áp kinh điển như LM7805, AMS1117-3.3. Hiểu tại sao nguồn tuyến tính lại tỏa nhiều nhiệt và cách tính công suất tiêu tán nhiệt ($P = (V_{in} - V_{out}) \times I$).
*   **Từ khóa tra cứu:** *Linear Regulator, AMS1117 datasheet, Power dissipation.*
*   **Thực hành:** Tự lắp một mạch nguồn từ pin 9V hạ xuống 5V dùng IC 7805, sau đó tiếp tục hạ từ 5V xuống 3.3V dùng AMS1117. Đo điện áp đầu ra xem có ổn định không.

#### 📝 Bài 12: Mạch Cách Ly Quang (Optocoupler)
*   **Mục tiêu:** Hiểu cách truyền tín hiệu bằng ánh sáng để cách ly hoàn toàn phần mạch số nhạy cảm (Vi điều khiển) với phần mạch động lực điện lớn hoặc môi trường công nghiệp đầy nhiễu.
*   **Từ khóa tra cứu:** *Optocoupler PC817, Galvanic Isolation.*
*   **Thực hành:** Thiết kế mạch dùng chân IO mô phỏng kích mở LED bên trong Optocoupler PC817, để đóng cắt một đường nguồn 12V biệt lập ở phía bên kia Optocoupler.

---

### 📍 Chương 5: Đọc Bản Vẽ Nguyên Lý & Sửa Lỗi Thực Tế (Bài 13 - Bài 14)

#### 📝 Bài 13: Điện trở Kéo lên (Pull-up) / Kéo xuống (Pull-down) & Đọc Schematic
*   **Mục tiêu:** Hiểu tại sao chân của vi điều khiển không bao giờ được để "lơ lửng" (Floating) mà phải có trở kéo lên nguồn hoặc kéo xuống đất. Học cách đọc các ký hiệu chuẩn, cách tra cứu sơ đồ chân (Pinout) và thông số giới hạn dòng/áp trong Datasheet của linh kiện.
*   **Từ khóa tra cứu:** *Pull-up resistor, Pull-down resistor, Floating pin, How to read schematic.*
*   **Thực hành:** Đọc file sơ đồ nguyên lý của board mạch Arduino Uno hoặc STM32 Blue Pill. Chỉ ra khối nguồn nằm ở đâu, khối thạch anh ở đâu, và các tụ lọc nguồn được bố trí thế nào.

#### 📝 Bài 14: Bài tập tổng hợp - Phân tích & Sửa lỗi mạch (Hardware Troubleshooting)
*   **Mục tiêu:** Rèn luyện tư duy cô lập lỗi phần cứng. Khi một hệ thống nhúng không hoạt động, bạn sẽ dùng đồng hồ vạn năng kiểm tra theo trình tự nào để tìm ra nguyên nhân (Lỗi nguồn? Thủng transistor? Ngắn mạch? Hở mạch?).
*   **Bài tập thực tế:** Giảng viên/Người quản lý repo sẽ đưa ra 3 tình huống mạch bị lỗi trên sơ đồ (Ví dụ: Mạch thiết kế thiếu trở hạn dòng, mạch kích transistor sai vùng bão hòa, mạch thiếu diode dập xung). Nhiệm vụ của người học là phân tích, chỉ ra điểm sai và sửa lại cho đúng.

---

## 🏆 Tiêu Chuẩn Hoàn Thành Học Phần
Người học được coi là tốt nghiệp Học phần 1 khi:
1.  Vượt qua toàn bộ các bài thực hành cắm mạch/mô phỏng phía trên.
2.  Tự giải thích được chức năng của mọi linh kiện xuất hiện trong một sơ đồ nguyên lý vi điều khiển cơ bản mà không cần tra cứu lại lý thuyết.

---
[⬅️ Quay lại Lộ trình tổng thể](https://github.com/đoạn-này-điền-link-repo-mẹ-của-bạn)
