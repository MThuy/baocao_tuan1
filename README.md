# baocao_tuan1
**BÀI TẬP TUẦN 1**

**PHẦN 1: TỔNG QUAN VỀ MÔ HÌNH OSI VÀ TCP/IP**

*1.1.	 Tổng  quan về mô hình  OSI*
OSI (Open Systems interconnection Reference Model) : Mô hình tham chiếu kết nối hệ thống mở. Mô hình có 7 lớp : lớp cao nhất Application -> presentation-> session-> transport -> network-> datalink-> physical.

 
Mỗi lớp có một chức năng riêng.

1.	Lớp Physical (vật lý): có chức năng truyền một dòng bit  sang một đường truyền vật lý cụ thể nào đó. Để làm điều đó nó định nghĩa về việc thiết lập về cơ, điện , quang, thiết bị mạng... để đảm bảo truyền được dữ liệu bít đi 

2.	Datalink (lớp liên kết): Chức năng điều khiển truy nhập vào đường truyền vật lý và giao tiếp với lớp bên trên là network. Để điều khiển lớp truy nhập vào đường truyền vật lý đó nó định dạng và truy nhập vào đường truyền vật lý, lớp vật lý này quy định đóng khung dữ liệu,cấu trúc khóa dữ lệu và thực hiện cơ chế điều tiết làm sao các lớp trên truy nhập vào  nên lớp vật lý do đó lớp  datalink cung cấp chức năng dò lỗi.

3.	Network (lớp mạng): Chịu trách nhiệm phân bố dữ liệu đi điểm này đến điểm kia một cách tối ưu nhất. Để xác định đường đi tối ưu nhất thì  lớp mạng định nghĩa các giao thức , các giáo thức này gọi là giao thức định tuyến. Muốn biết dữ liệu đi đâu phải có địa chỉ, lớp network này định địa chỉ 

4.	Transport (Vận chuyển ): có chức năng quản lý kết nối từ đầu cuối, đầu cuối. Xử lí truyền tải các host một cách tin cậy, thiết lập duy trì  và giả phóng kết nối các vành ảo, cung cấp các cơ chế dò,sửa tin cậy và cơ chế phục hồi thông tin bằng cách điều khiển luồng

5.	Lớp Session (Phiên): truyền liên thông host bằng các thiết lập quản lý và giải phóng các session  giữa các ứng dụng.

6.	Lớp Presentation (lớp trình bày): chịu trách  nhiệm chuyển đổi dữ liệu gửi đi trên mạng từ một loại biểu diễn này sang một loại khác. Để đạt được điều đó nó cung cấp một dạng biểu diễn chung dùng để biểu diễn chung dùng để truyền khác. Để đạt được điều đó nó cung cấp một dạng biểu diễn chung dùng để truyền thông và cho phép chuyển đổi từ dạng biểu diễn cục bộ sang biểu diễn chung và ngược lại

7.	Application ( lớp ứng dụng): Chức năng của lớp này xác định giao diện giữa người sử dụng và nôi trường OSI và giải quyết các kỹ thuật mà các chương trình ứng dụng để giao tiếp với mạng

*1.2.	 Mô hình TCP/IP*
 

Mô hình TCP/IP có 4 lớp : application, transport, internet, network access
-	Network access (Lớp truy cập mạng):Kết hợp cức năng hai lớp vật lý và liên kết dữ liệu của mô hình OSI 
+ Các mô tả về chức năng, thủ tục, cơ học, điện học
+ Tốc độ truyền vật lý
+ Khoảng cách, các bộ kết nối vật lý
+ Khung – Frame
+ Địa chỉ vật lý
+ Cấu hình liên kết mạng
+ Điều khiển lỗi, điều khiển lưu lượng
+ Sự đồng bộ
-Internet : Gửi dữ liệu đến đích qua các mạng con : gói, thiết lập kết nối ảo, định tuyến, tìm đường, địa chỉ logic, sự phân đoạn, giao thức Internet
- Lớp Transport:  lớp vận chuyển liên quan đến chất lượng dịch vụ như độ tin cậy, điều khiển lưu lượng và sử lỗi: phân đoạn, dòng dữ liệu, định hướng kết nối và không kết nối, điều khiển luồng, phát hiện lỗi
- Lớp Application:  Kết hợp  chức năng của 3 lớp phiên, trình bày, ứng dụng trong mô hình OSI

*1.3. Sự khác nhau giữa 2 mô hình  OSI và ICP/IP*
- Giống nhau: đều phân lớp, đều có lớp ứng dụng, mạng, vận chuyển, kỹ thuật chuyển mạch gói
- Khác nhau:  
+TCP/IP kết hợp lóp trình bày và phiên vào lớp ứng dụng
+ TCP/IP kết hợp lớp liên kết dữ liệu và lớp vật lý và một lớp truy cập mạng
+ TCP/IP đơn gian hơn vì ít  lớp hơn
+ Bộ giao thức ICP/IP là tiêu chuẩn  trên Internet

**PHẦN 2: MỘT SỐ GIAO THỨC LỚP ỨNG DỤNG TRONG MÔ HÌNH TCP/IP**
Lớp ứng dụn trong mô hình TCP/IP có một số giao thức:  DNS, RIP, SMTP, FTP, HTTP

*2.1. Giao thức HTTP( Hyper text tranfer protocol)*
- Là giao thức dùng  cho các ứng dụng web
- Sử dụng mô hình client- server:
+ Client: Browser gửi yêu cầu, nhận, hiển thị các đối tượng web. Browser:IE, fireFox, Netcape
+Server: webserver gửi các đối tượng khi có yêu cầu. 
Web server: IIS, APPche, Tomcat
- Client khởi tạo kết nối TCP tới server thông qua cổng 80 ( cổng web mặc định)
- Server chấp nhận kết nối TCP từ client gửi đến
- Các thông điệp http troa đôit brower_ web server
-	Đóng kết nối TCP/IP

*2.2. Giao thức truyền file  FTP*
- Giao thức trao đổi file với máy tính ở xa
- Sử dụng mô hình client-server
+ Client : khởi tạo kết nối
+ Server máy tính ở xa: cổng dịch vụ: port 21
-	Các lệnh thường gặp: được mã hóa bằng mã ASCII, USER username, PASS password, LIST trả về danh sách các file thư mục hiện hành, RETR filename lấy file từ thư mục hiện thời, STOR file name tải file vào thư mục hiện thời trên máy tính ở xa
-	Các mã trả về thường gặp: Tương tự HTTP;  331 chấp nhận username, yêu cấu password;  125: kết nối dữ liệu được thiết lập, chuẩn bị truyền dữ liệu; 425 không thể thiết lập kết nối dữ liệu; 452 lỗi ghi file

*2.3. Giao thưc SMTP*
- Giao thức SMTP sử dụng kết nối bền vững
- SMTP đòi hỏi thông điệp phải được định dạng bằng mã ASCII 7 bit
- Những xâu kí tự đặc biệt không được phép ghi vào thông điệp 
- SMTP server sử dụng CRLF. CRLF để đánh dấu kết thúc thông điệp

*2.4. Giao thức DNS*
- DNS là hệ thống tên miền, chỉ có 1 hệ thống cho phép thiết  lập tương ứng giữa địa chỉ IP và tên miền 
- Nó liên kết nhiều thông tin đa dạng với tên miền gán cho những người tham gia
- Chức năng của DNS:
+ Mỗi website có 1 tên miền, 1 địa chỉ IP
+ Quá trình dịch tên miền-> địa chỉ IP -> trình duyệt hiểu, truy cập được vào website là công việc cuae 1 DNS Server
+ Các DNS trợ giúp qua lại với nhau để dịch địa chỉ IP-> tên miền và ngược lại
-	Nguyên  tắc làm việc của DNS
+ Mỗi nhà cung cấp dịch vụ và duy trì DNS Server riêng của mình
+ Một trình duyệt tìm địa chỉ 1 website thì DNS Server phân tên website này phải là DNS Server của mình tổ chức quản lý website đó
-	DNS có khả năng truy xuất các DNS Server khác để có được 1 cái tên đã được phân tán

*2.5. Giao thức RIP*
RIP ( Routing Information Protocol) là một giao thức định tuyến quảng bá thông tin về địa chỉ mạng mà mình muốn quảng bá ra bên ngoài và thu nhập thông tin để ghi vào bảng định tuyến cho Router. Đây là một giao thức Distance Vector hoạt động dựa vào số hop count. Vì sử dụng tiêu chí định tuyến là hop count và bị giới hạn ở số hop là 15 nên giao thức này chỉ được sử dụng trong các mạng nhỏ dưới 15 hop. RIO có 2 phiên bản là RIPv1 và RIPv2

RIPv1 có đặc điểm:
-	Là một giao thức định tuyến vector khoảng cách nên quảng bá toàn bộ bảng định tuyến của nó cho các router láng riềng theo định kỳ . Chu kỳ cập nhật của RIP là 30 giây. Thông số định tyến của RIP là số lượng hop, giá trị tối đa là 15 hop.
-	RIPv1 là giao thức định tuyến theo địa chỉ. Khi RIP router nhận thông tin về một mạng nào đó từ một cổng, trong thông tin định tuyến này không có thông tin về subnet mask đi kèm. Do đó router sẽ lấy subnet  mask củ cổng để áp dụng cho địa chỉ mạng nó nhận được từ cổng này. Nếu subnet mask này không phù hợp thì nó sẽ lấy subnet mask mặc định theo lớp địa chỉ áp dụng cho địa chỉ mạng mà nó nhận được
-	Địa chỉ lớp A có subnet mask : 255.0.0.0
-	Địa chỉ lớp B có subnet mask : 255.255.0.0
-	Địa chỉ lớp C có subnet mask : 255.255.255.0
-	RIPv1 là giao thức định tuyến được sử dụng phổ biến vì mọi router IP đều hỗ trợ giao thức  và nó phổ biến .
-	Một số hạn chế: không gửi thông tin subnet mask trong thông tin định tuyến, gửi quảng bá thông tin định tuyến theo địa chỉ 255.255.255.255, không hỗ trợ xác minh thông tin nhận được, không hỗ trợ VLSM

RIPv2
-	Giao  thức định tuyến theo Distance Vector
-	Hoạt động theo cơ chế Auto_Summarization trên các border router
-	Giao thức định tuyến dạng Classless ( hỗ trợ VLSM)
-	Hỗ trợ tính năng split horizon kết hợp poison reverse
-	Subnet mask được gửi kèm trong gói tin update.






