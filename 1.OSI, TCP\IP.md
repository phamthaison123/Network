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

