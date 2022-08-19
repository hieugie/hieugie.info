---
layout: post
title:  "Ưu điểm và nhược điểm của Microservices"
date:   2022-06-07 00:00:00
categories: Microservices
---
# Trong cái blog này, chúng ta hãy cùng nhau thảo luận qua 1 chút về microservice
## Định nghĩa
Trước tiên để có cái nhìn tổng quát về microservice là gì thì trước hết tôi xin phép được
định nghĩa khái niệm Microservice là gì.
<br/>
<br/>
**Sam Newman** có viết trong cuốn ***<u>Building Microservices: Designing Fine-Grained Systems</u>*** thì:
> Microservices là 1 tập hợp những service nhỏ làm việc cùng với nhau.
<!-- more -->
Còn theo như **James Lewis and Martin Fowler**
> Kiểu kiến trúc Microservices là 1 phương pháp tiếp cận việc phát triển 1 ứng dụng đơn lẻ từ 1 bộ các service nhỏ.
> Trong đó mỗi service sẽ tự chạy các tiến trình riêng của chính nó và giao tiếp với nhau theo 1 cơ chế đơn giản.
> Các services này được xây dựng dựa trên nghiệp vụ mong muốn và có  triển khai tự động 1 các độc lập.

Tổng kết lại thì cái tên nó cũng đã nói lên phần nào cái định nghĩa của chính nó. Thay vì chúng ta xây dựng 1 ứng dụng
lớn thì chia nó thành nhiều phần nhỏ khác nhau và có thể hoạt động tương tác với nhau 1 cách hợp lý.

### Nguyên tắc xây dựng Microservices
Về cơ bản thì để xây dựng một kiến trúc gì đó thì chúng ta đều phải có những nguyên tắc nhất định phải tuân theo.
Nó giúp chúng ta đưa ra những quyết định đúng đắn hơn, đúng chuẩn hơn. Hãy cùng điểm qua các nguyên tắc trong việc
xây dựng Microservices.

1. **Single responsibility principle.**
> Nguyên tắc này chỉ ra rằng 1 lớp hoặc 1 mô-dun trong 1 ứng dụng chỉ nên có 1 và chỉ 1 trách nhiệm duy nhất.
> Bất kỳ 1 service nào cũng không nên có nhiều hơn 1 trách nhiệm trong cùng 1 lúc.

2. **Modelled around business domain.**
> Khi xây dựng 1 microservice, nó sẽ không bị giới hạn bỏi bất kỳ cộng nghệ hay database nào. hãy chọn những công nghệ,
> database phù hợp nhất cho việc giải quyết bài toán nghiệp vụ

3. **Isolated Failure**
> Hãy luôn giũ trong đầu rằng service có thể bị chết bất cứ lúc nào, chình vì thế hãy luôn chuẩn bị các phương án
> cho việc phát hiện cũng như khôi phục lại các service bị chết.

4. **Infrastructure Automation**
> Tự động hoá cơ sở hạ tầng là quá trình tạo các mã để cấu hình môi trường, việc này sẽ giúp chúng ta áp dụng các
> cấu hình giống nhau cho 1 node hoặc hàng chục, trăm nodes, đơn giản hoá trong việc triển khai và scale.

5. **Deploy independently**
> Dĩ nhiên việc triển khai các service phải là độc lập với nhau, không liên quan, ràng buộc cũng như ảnh hường
> tới các service khác.

### Ưu điểm và nhược điểm của Microservices
Microservices được xây dựng trêm nguyên lý **Chia để trị** chính vì thế nó có tất cả các ưu điểm cũng như nhược điểm
của nguyên lý này, kết hợp với ngành IT thì mềnh nghĩ có các ưu điểm và nhược điểm như sau:

#### Ưu điểm
Về ưu điểm thì hầu hết sẽ liên quan đến việc code base của từng service do được chia ra nên rất nhỏ, dẫn đến những
ưu điểm mà mình có thể kể tên như sau:

1. Code base nhỏ sẽ giúp cho việc đọc hiểu 1 service dễ dàng hơn, dễ dàng trong việc kiểm thử, bảo trì cũng như nâng cấp các tính năng hơn

2. Vì Microservice là độc lập sẽ giúp việc triển khai dễ dàng hơn, nó cũng cho phép nhiều team có thể tham gia vào việc phát triển

3. Bởi thì triển khai độc lập nó sẽ giúp việc scale 1 cách dễ dàng hơn, ít tốn tài nguyên hơn do chỉ cần scale những Microservices cần thiệt

4. Giảm thời gian downtime của hệ thống theo nguyên lý Isolated Failure.

5. Dễ dàng thêm bớt các service mà không ảnh hưởng quá nhiều đến hệ thống

#### Nhược điểm
1. Không giống như monolithic, Microservices có thể bao gồm kiểu công nghệ, kiến trúc cũng như DB khác nhau dẫn đến việc khó khăn trong việc hiểu toàn bộ kiến trúc, cũng như quản lý nếu như số lượng lên trên hàng trăm, nghìn service nhỏ.

2. Việc thay đổi, cập nhật 1 service có khả năng ảnh hưởng đến các service khác gọi đến nó.

3. Trong 1 số trường hợp tài nguyên để triển khai Microservices có thể sẽ tốn nhiều hơn so với Monolithic.

4. Khó khăn trong việc test ở môi trường phân tán

5. Cần nhiều kiến thức để giải quyết các bài toàn liên quan đến độ trễ, cân bằng tải... dẫn đến nguy cơ giãn đoạn kết nối
 giữa các service với nhau.

### Tổng kết
Như những gì đã lướt qua bên trên có thể thấy, Microservice có rất nhiều ưu điểm cũng như khuyết điểm. Chúng ta đều có
thể thấy những ưu điểm vượt trội của microservice hơn so với monolithic, tuy nhiên thì đi kèm với đó bạn cũng phải
trade off nhiều thứ. Hãy cân nhắc kỹ lưỡng trước khi lựa chọn kiến trúc phù hợp cho dự án của mình.
