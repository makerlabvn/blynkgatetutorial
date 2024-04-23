# Hướng dẫn sử dụng Blynk-Gate

## I. Tổng quan
### 1. Giới thiệu về Blynk và phần cứng Blynk-gate

* Blynk là một nền tảng IoT cung cấp các công cụ để kết nối, quản lý và điều khiển các thiết bị IoT từ xa thông qua mạng Internet. Điểm nổi bật của Blynk là sự dễ dàng và nhanh chóng trong việc tạo và quản lý các ứng dụng IoT, phù hợp cho cả những người mới bắt đầu và những nhà phát triển chuyên nghiệp.
* Bằng cách sử dụng phần cứng **Blynk Gate** người dùng không cần phải code mà chỉ cần thao tác tùy chỉnh cơ bàn là đã có thể tạo ra 1 thiết bị điều khiển từ xa thông qua intermet.

### 2. Sơ đồ mạch Blynk-gate
![matduoi](https://github.com/ainguyn/blynkgatetutorial/assets/167832348/1507de73-6f29-4fd8-aa7c-7b45e1d4090c) 
![mattren](https://github.com/ainguyn/blynkgatetutorial/assets/167832348/5cc9af8d-e3fc-4ef9-b19e-165efc1bb5e4) 

### 3. Chức năng các chân trên mạch
* 5V: Chân cấp nguồn dương 5V
* GND: Chân cấp nguồn âm 0VDC
* SDA: Chân truyền nhận tín hiệu I2C  
* SCL: Chân tín hiệu xung nhịp I2C
* P1 -> P4: Chân OUTPUT điều khiển thiết bị 
* *Lưu ý: Khi chân J1 không được hàn thì chân SDA, SCL có chức năng giao tiếp I2C, nếu chân J1 được hàn lại thì 2 chân SDA, SCL sẽ không còn chức năng giao tiếp I2C mà sẽ là 2 chân OUTPUT tín hiệu giống như các chân P1 -> P4.*
## II. Hướng dẫn tạo tài khoản Blynk
### 1. Tạo tài khoản trên trang web

**Bước 1**: PC/ Laptop: Truy cập link Blynk: <https://blynk.io/> 

**Bước 2**: Bấm vào nút 'LOGIN'
![image](https://github.com/ainguyn/blynkgatetutorial/assets/167832348/c41eea17-b07d-42d1-b303-017ccd42c7b3)

**Bước 3**: Chọn Create new acccount 
-	Tiến hành nhập Email và mật khẩu để tạo tài khoản mới ![image](https://github.com/ainguyn/blynkgatetutorial/assets/167832348/2ca5597e-1ec6-4327-b934-72867b796e6e)

## III.	  Hướng dẫn sử dụng Blynk – gate để bật tắt đèn Led
### 1.	Setup trên Blynk

**Bước 1**: Tại giao diện chính của Blynk, chọn “For Makers”
![image](https://github.com/ainguyn/blynkgatetutorial/assets/167832348/28bdf82e-1111-42fc-ae09-bf5a5547dba1)

**Bước 2**: Thiết lập một template mới dùng để điều khiển dự án đèn Led tắt bật theo ý muốn, ấn chọn “New template”
![image](https://github.com/ainguyn/blynkgatetutorial/assets/167832348/793762ee-da51-447b-8f99-b2475433616a)


**Cách tạo một template mới**  
+ Name: Đặt tên bất kì cho template.
+ Hardware: Chọn mặc định ESP8266.

                                                                 ![image](https://github.com/ainguyn/blynkgatetutorial/assets/167832348/f03f84b7-0b3a-42ca-922a-3c21b1469395)

+ Connection Type: Wifi.
+ Description: Phần mô tả chi tiết thêm cho template.

Bước 3: Sau khi đã tạo một template mới, cần thiết lập các Datastreams (các chân Virtual Pin) 
 
Chọn New Datastream -> Virtual Pin




Bước 6: Sau khi đã tạo được các Datastreams, chúng ta sẽ kéo thả nó vào “Web Dashboard”, đây sẽ là nơi dùng để tùy chỉnh giao diện điều khiển các Virtual Pin Datastreams đã setup ở bước trước

+ Để bật tắt thiết bị, chúng ta chọn hộp lệnh “Switch” trong nhóm lệnh Control rồi kéo thả vào giao diện điều khiển hoặc click chuột trái 2 lần vào hộp lệnh.
+ Di chuyển con chuột tới hộp lệnh đã đặt trong phần giao diện và ấn vào biểu tượng bánh răng, khi đó sẽ hiện lên bảng “Switch Settings” dùng để thiết lập nút lệnh này với các Datastreams Virtual Pin đã tạo ở bước trước.
+ Tittle: Đặt tên tùy ý cho nút lệnh
+ Datastream: Chọn Datastream muốn điều khiển và ấn save

Bước 7: Quay về thẻ Home và nhấn “Add first device” để đặt tên cho thiết bị điều khiển và hoàn tất thiết lập.

 
## 2. Thiết lập Blynk trên điện thoại:
IOS/Android: Truy cập “App Store” /” Google Play” và tải app “Blynk IoT”
- Sau khi tải app, chúng ta đăng nhập vào tài khoản đã tạo ở trang web, khi đó tên thiết bị đã tạo trên web sẽ hiển thị sẵn trên màn hình
- Ấn vào tên thiết bị để vào giao diện điều khiển, sau đó chọn vào biểu tượng cờ lê như hình

-	Chọn Button (Công tắc) để điều khiển đèn tắt mở và có thể kéo thả đến vị trí tùy ý

- Sau khi ấn button, màn hình sẽ hiện ra giao diện giống hình 5, ấn vào nút lệnh lần nữa để thiết lập nó với các Datastream Virtual Pin đã tạo trước đó

 
## IV.	 Hướng dẫn kết nối Blynk – gate với Blynk app (Demo)
	Note: Truy cập Wifi Blynk gate trước rồi mới vào địa chỉ IP, mạng Wifi khai báo là 2.4G
-	Sau khi hoàn tất setup Blynk app, chúng ta sẽ có được “Blynk_Auth_Token” dùng để kết nối với Blynk – gate






-	 Ấn giữ nút Set trên Blynk – gate khoảng 10s cho tới khi thấy đèn xanh trên Blynk – gate chớp nhanh liên tục để reset toàn bộ dữ liệu.
- Truy cập vào wifi “Blynk gate” trên máy tính và vào địa chỉ IP: 192.168.4.1
Sau khi đã khai báo như ảnh thì ấn cập nhật, máy tính sẽ kết nối với Blynk – gate (Để ý đèn xanh trên Blynk – gate chớp nhanh vài giây sau kết nối nghĩa là kết nối thành công)
- Sau khi kết nối thành công, Blynk – gate sẽ tự động ngắt wifi trên máy tính. Vào lại wifi khác và truy cập Blynk web để tiến hành điều khiển

   

