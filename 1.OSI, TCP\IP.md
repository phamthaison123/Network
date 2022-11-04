# Mô hình OSI
* Mô hình OSI (Open Systems Interconnection) hay còn được gọi là “mô hình tham chiếu 7 tấng OSI”.Mục đích chính của chúng là giúp người sử dụng dễ hình dung hơn về cơ chế truyền tin giữa các máy tính với nhau.Mô hình OSI bao gồm 7 tầng, mỗi tầng đều có đặc tính là chỉ sử dụng chức năng của tầng dưới nó, đồng thời chúng cũng chỉ cho phép tầng trên sử dụng các chức năng của mình.Mô hình OSI thực chất là chia nhỏ các hoạt động phức tạp của mạng thành các phần công việc đơn giản , dễ hình dung hơn.
* mô hình OSI - mô hình thăm chiếu 7 tầng
![image](https://user-images.githubusercontent.com/91528234/199876907-14a23b8d-d69e-4f8c-aade-7f2589f518f1.png)

* Chức năng của từng tầng:
  * Tầng 1: Tầng vật lý (Physical Layer) có chức năng chính là điều khiển việc truyền tải các bit trên đường truyền vật lý.Chúng định nghĩa các tín hiệu điện, trạng thái đường truyền, phương pháp mã hóa dữ liệu.
  * Tầng 2: Tầng liên kết dữ liệu (Data-Link Layer) Đảm bảo truyền tải các khung dữ liệu (Frame) giữa hai máy tính có đường truyền vật lý nối trực tiếp với nhau là điều mà chúng thực hiện.Ngoài ra nó còn cài đặt cơ chế phát hiện và xử lý lỗi dữ liệu nhận.
  * Tầng 3: Tầng mạng (Network Layer) tầng mạng đảm nhiệm việc truyển các gói tin (packet) giữa hai máy tính bất kỳ trong mạng máy tính.
  * Tầng 4: Tầng vận chuyển (Transport Layer) Vai trò của chúng là phân nhỏ các gói tin có kích thước lớn khi gửi và tập hợp chúng khi nhận, quá trình phân nhỏ khi gửi và nhận đảm bảo tính toàn vẹn cho dữ liệu (không bị mất mát, không lặp và đúng thứ tự).
  * Tầng 5: Tầng giao dịch (Session) Quản lý phiên làm việc giữa các người sử dụng chính là việc mà chúng làm.Tầng mạng này cung cấp cơ chế nhận biết tên và chức năng bảo mật thông tin qua mạng máy tính.
  * Tầng 6: Tầng trình bày (Presentaition Layer) Đảm bảo các máy tính có kiểu dụng dạng dữ liệu khác nhau vẫn có thể trao đổi thông tin cho nhau.Thường thì các máy tính sẽ thống nhất với nhau về một kiểu định dạng dữ liệu trung gian để trao đổi thông tin giữa các máy tính.Trong quá trình truyền dữ liệu, tầng trình bày bên máy gửi có nhiệm vụ dịch dữ liệu từ định dạng riêng sang định dạng chung và quá trình ngược lại trên tầng trình bày bên máy nhận.
  * Tầng 7: Tầng ứng dụng (Application Layer) là tầng cung cấp các ứng dụng truy xuất đến các dịch vụ mạng như Web Browser,Mail User Agent…hoặc các Program cung cấp các dịch vụ mạng như Web Server, FTP Server, Mail Server…

# Mô hình TCP/IP

* Nếu OSI được hình thành mang tính chất dùng cho học tập nghiên cứu nhiều hơn là triển khai thực tế,thì TCP/IP lại khác hoàn toàn.Chính trên chiếc máy tính chúng ta đang sử dụng hàng ngày cũng dùng các giao thức TCP/IPv4 hoặc TCP/IPv6.Mô hình TCP/IP còn được gọi với cái tên khác đó là mô hình DoD.
* Mô hình TCP/IP
![image](https://user-images.githubusercontent.com/91528234/199877169-4544beac-e264-4401-8c2a-74fc4317ed06.png)

* Chức năng các tầng:
  * Tầng 1: Tầng truy cập (Network Access Layer) tầng này có thể coi là một tầng riêng biệt hoặc cũng có thể tách nó thành 2 tầng vật lý và tầng liên két dữ liệu như trong mô hình OSI.Nó được sử dụng để truyền gói tin từ tầng mạng đến các Host trong mạng.Các thiết bị vật lý như : Switch, cáp mạng, card mạng HBA-Host Bus Adapter là các thành phần truy cập.
  * Tầng 2: Tầng mạng (Internet Layer) trên mô hình TCP/IP có vai trò chính là giải quyết vấn đề dẫn đến các gói tin đi qua các mạng để đến đúng đích.
  * Tầng 3: Tầng vận chuyển (Transport Layer) đảm nhiệm việc phân nhỏ các gói tin có kích thước lớn khi gửi và tập hợp lại khi nhận, tính toàn vẹn cho dữ liệu (không lỗi, không mất, đúng thứ tự) là yếu tố được đảm bảo.Nếu để ý thì bạn sẽ thất chức năng của tầng vận chuyển ở giao thức TCP/IP cũng giống với tầng vận chuyển của mô hình OSI.
  * Tầng 4: Tầng ứng dụng (Application Layer) là nơi các chương trình mạng như Web Browser,Mail User Agent làm việc để liên lạc giữa các node mạng.Do mô hình TCP/IP không có tầng nào nằm giữa các tầng ứng dụng và tầng vận chuyển, nên tầng Application của TCP/IP bao gồm các giao thức hoạt động như tầng trình diễn và giao dịch trong OSI.
# Phân biệt UDP/TCP
## Giống nhau
* TCP và UDP đều là các giao thức được sử dụng để gửi các bit dữ liệu - được gọi là các gói tin - qua Internet. Cả hai giao thức đều được xây dựng trên giao thức IP. Nói cách khác, dù bạn gửi gói tin qua TCP hay UDP, gói này sẽ được gửi đến một địa chỉ IP. Những gói tin này được xử lý tương tự bởi vì chúng được chuyển tiếp từ máy tính của bạn đến router trung gian và đến điểm đích.TCP và UDP không phải là giao thức duy nhất hoạt động trên IP, tuy nhiên, chúng được sử dụng rộng rãi nhất.

## Khác nhau

| TCP | UDP |
|:----|:----|
| Đảm bảo rằng dữ liệu đến đúng như khi được gửi. | Không đảm bảo dữ liệu đến.|
| Kiểm tra lỗi các luồng dữ liệu. | Không cung cấp tính năng kiểm tra lỗi. |
| Header 20 byte cho phép 40 byte dữ liệu tùy chọn | Header 8 byte chỉ cho phép dữ liệu bắt buộc. |
| Chậm hơn UDP | Nhanh hơn TCP |
| Tốt nhất cho các ứng dụng yêu cầu độ tin cậy. | Tốt nhất cho các ứng dụng yêu cầu tốc độ. |

# IPv4
* Ipv4 viết tắt cho Internet Protocol Version 4, dịch ra có nghĩa là giao thức Internet phiên bản thứ 4. Ipv4 đã được bộ quốc phòng Hoa Kỳ chuẩn hóa trong bản MIL-STD-1777. Giao thức Internet IP đã trải qua nhiều phiên bản khác nhau và phiên bản Ipv4 là phiên bản đầu tiên được sử dụng rộng rãi trên toàn thế giới và hiện vẫn còn đang là nòng cốt của Internet trên toàn thế giới.
* Ipv4 là giao thức mang tính hướng dữ liệu và được sử dụng cho hệ thống chuyển mạch gói. Ipv4 không quan tâm đến thứ tự truyền gói tin, cũng không đảm bảo gói tin sẽ đến đích hay là có xảy ra tình trạng lặp gói tin ở đích đến hay không. Nó chỉ có cơ chế đảm bảo tính toàn vẹn dữ liệu bằng việc sử dụng những gói kiểm tra được thiết lập đi kèm với nó.
* Địa chỉ Ipv4 là 1 địa chỉ đơn nhất đang được sử dụng bởi các thiết bị điện tử hiện nay để nhận diện và liên lạc với nhau trên Internet. Để đánh địa chỉ, Ipv4 sử dụng 32bit và chia ra làm 4 octet (mỗi octet có 8 bit = 1 byte). Dấu chấm được sử dụng để ngăn các octet với nhau.

![image](https://user-images.githubusercontent.com/91528234/199881389-d050bb90-25c8-469c-a2ac-b28a8d6e76e5.png)

* Các loại địa chỉ Ipv4: unicast, broadcast, multicast. Trong đó unicast là địa chỉ IP cho phép thiết bị gửi dữ liệu đến 1 nơi nhận duy nhất. Địa chỉ IP broadcast lại cho phép gửi dữ liệu đến các host trong 1 mạng con. Còn địa chỉ IP multicast cho phép thiết bị gửi dữ liệu đến 1 tập xác định trước các host.

## Địa chỉ Ipv4 có bao nhiêu lớp?
* Ban đầu, 1 địa chỉ Ipv4 được chia ra làm 2 phần là địa chỉ của mạng (Network ID) và địa chỉ của máy (Host ID). Địa chỉ của mạng (Network ID) được xác lập bởi octet đầu tiên và địa chỉ của máy (Host ID) được xác lập cho 3 octet còn lại. Với cách chia này thì địa chỉ của network bị giới hạn ở con số 256. Đây là con số quá ít so với nhu cầu sử dụng thực tế. Vì vậy người ta đã định nghĩa phân lớp mạng để vượt qua giới hạn này và tập hợp thành 1 lớp mạng đầy đủ còn được gọi là classful.

* Địa chỉ IP được phân ra thành 5 lớp khác nhau: lớp A, lớp B, lớp C, lớp D,lớp E. Với cách phân loại này sẽ tạo được vô số địa chỉ IPv4 khác nhau. Đặc điểm của các lớp IPv4 này là gì? Hãy cùng tìm hiểu tiếp nhé.

### Lớp A
* Lấy octet1 và bit đầu là 0 còn 7 bit. Chạy từ 1.0.0.0 đến 126.0.0.0 127.0.0.0 là loopback còn 24 bít còn lại host.

![image](https://user-images.githubusercontent.com/91528234/199881793-aa539a10-4024-444f-ac66-780ba9e98d90.png)

### Lớp B
* Lấy 2 octet đầu và 2 bit đầu là 10 còn 6 bit . Chạy từ 128.0.0.0 đến 191.255.0.0 còn 16 bit còn lại làm host

![image](https://user-images.githubusercontent.com/91528234/199882050-39594f2b-1922-4273-b502-b339adacd391.png)


### Lớp C
* Lớp C của địa chỉ Ipv4 dùng 3 octet đầu làm phần mạng và 1 octet sau làm phần host. Địa chỉ lớp C luôn có 3 bit đầu là 1 1 0. Dải mạng lớp C chạy từ 192.0.0.0 -> 223.255.255.0. Như vậy sẽ có 221 mạng trong lớp C. Đối với phần host gồm 1 octet sau cùng nên dài 8 bit và sẽ có (28 – 2) host trong lớp C. Xem ảnh minh họa.

![image](https://user-images.githubusercontent.com/91528234/199887028-2f4debb7-fb51-43c1-bc18-915f71ddb148.png)


### Lớp D
Lớp D được sử dụng làm các địa chỉ multicast và dải địa chỉ lớp D từ 224.0.0.0 -> 239.255.255.255. Lấy ví dụ như Ví dụ: 224.0.0.5 dùng cho OSPF; 224.0.0.9 dùng cho RIPv2.

### Lớp E
Lớp E gồm các giải số từ 240.0.0.0 trở đi và được sử dụng cho mục đích dự phòng.
# IPv6
## Cấu trúc IPv6
![image](https://user-images.githubusercontent.com/91528234/199883033-8c14d58f-67d9-45c3-b387-287aa73dc6bb.png)
* Địa chỉ IPv6 dài 128 bit, được chia làm 8 nhóm, mỗi nhóm gồm 16 bit, được ngăn cách với nhau bằng dấu hai chấm “:”. Mỗi nhóm được biểu diễn bằng 4 số hexa.
* Ví dụ:
``` 
FEDC:BA98:768A:0C98:FEBA:CB87:7678:1111
1080:0000:0000:0070:0000:0989:CB45:345F
```

* Những địa chỉ này lớn, khả năng cung cấp địa chỉ cho nhiều node và cung cấp cấu trúc phân cấp linh hoạt, nhưng nó không dễ để viết ra. Vì vậy cần có 1 số nguyên tắc để nhằm rút ngắn lại cách biểu diễn địa chỉ IPv6. Sau đây là các quy tắc để rút gọn IPv6:
 * Cho phép bỏ các số 0 nằm trước mỗi nhóm (octet).
 * Thay bằng số 0 cho nhóm có toàn số 0.
 * Thay bằng dấu “::” cho các nhóm liên tiếp nhau có toàn số 0.

* Ví dụ về nén địa chỉ IPv6:
```
 Cho một địa chỉ: 1080:0000:0000:0070:0000:0989:CB45:345F
  Dựa theo các quy tắc đã nêu trên, có thể nén địa chỉ IP trên như sau: 1080::70:0:989:CB45:345F hoặc 1080:0:0:70::989: CB45:345F
```

* Chú ý: Dấu “::” chỉ sử dụng đƣợc 1 lần trong toàn bộ địa chỉ IPv6 (nhiều dấu “::” có thể gây ra sự nhầm lẫn hoặc không thể biết đúng vị trí của các octet trong địa chỉ IPv6).

## Biểu diễn của Address Prefixes
* Prefix của địa chỉ IPv6 được biểu diễn tương tự với kí hiệu IPv4 CIDR. IPv6 prefix được biểu diễn như sau: IPv6-address/ prefix-length
* Trong đó:
 * IPv6-address là bất kì địa chỉ có giá trị, Prefix-length là số bit liền kề nhau được bao gồm trong prefix.
```
Ví dụ: Sau đây là quy tắc biểu diễn cho 56 bit prefix 200F00000000AB:
200F::AB00:0:0:0:0/56
200F:0:0:AB00::/56
```

* Chú ý với địa chỉ IPv6, kí hiệu “::” được sử dụng 1 lần duy nhất trong mỗi sự biểu diễn.
* Theo sau là các cách biểu diễn sai của 56 bit prefix:
```
200F:0:0:AB/56
200F::AB00/56
200F::AB/56
```
* Cách biểu diễn đầu tiên là không hợp lệ bởi vì các số 0 theo sau trong vòng một trường 16-bit (AB00) bị mất, và địa chỉ không đủ chiều dài hợp lệ. Địa chỉ IPv6 trên bên trái của dấu gạch chéo “/” phải là một địa chỉ IPv6 có chiều dài đầy đủ hoặc được nén hợp lệ. Cách biểu diễn thứ hai và thứ ba là địa chỉ IPv6 được nén hợp lệ nhưng nó không giãn ra thành địa chỉ chính xác. Thay vì 200F:0000:0000:AB00:0000:0000:0000:0000 nó sẽ giãn thành 200F:0000:0000:0000:0000:0000:0000:AB00 và 200F:0000: 0000:0000:0000:0000:0000:00AB, tương ứng.

## Phân loại địa chỉ IPv6
* Một địa chỉ IPv6 có thể được phân thành 1 trong 3 loại:
 * Unicast: Một địa chỉ unicast được định nghĩa duy nhất trên một cổng của một node IPv6. Một gói tin được gởi đến một địa chỉ unicast được đưa đến cổng được định nghĩa bởi địa chỉ đó.
 * Multicast: Một địa chỉ multicast định nghĩa một nhóm các cổng IPv6. Một gói tin gởi đến địa chỉ multicast được xử lý bởi tất cả những thành viên của nhóm multicast.
 * Anycast: Một địa chỉ anycast được đăng kí cho nhiều cổng (trên nhiều node). Một gói tin được gởi đến một địa chỉ anycast là được chuyển đến chỉ một trong số các cổng này, thường là gần nhất.
* Global Routing Prefixes
Bảng sau đây đưa ra các prefix được gán hiện tại của tiền tố dành riêng và địa chỉ đặc biệt, ví dụ như địa chỉ Link-local hoặc địa chỉ multicast. Phần chính của không gian địa chỉ (hơn 80%) không được gán, để chỗ cho những đăng kí trong tương lai.
![image](https://user-images.githubusercontent.com/91528234/199886930-53a63293-f1cc-40d0-8e4c-cae401ccec9e.png)
