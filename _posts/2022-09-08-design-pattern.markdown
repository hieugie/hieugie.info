---
layout: post
title:  "Ngắn gọn về 23 pattern theo Gangs of four(GoF) design patterns"
date:   2022-08-11 00:00:00
categories: Interview_Question
tags: Interview Question
---

## Vì sao chúng ta tên sử dụng design pattern?

Tính hữu dụng của các design pattern thì không cần phải bàn cãi nữa rồi, nó cung cấp cho chúng ta các giải pháp để 
giải quyết các vấn đề thường gặp bằng OOP. Nó giúp bạn rút ngắn thời gian phát triển cũng như bảo trì code

<!-- more -->

## Ba loại Design Pattern theo GoF

GoF chia design pattern thành 3 loại như sau:

1. ***Nhóm khỏi tạo***: Các nguyên mẫu thiết kế giúp bạn giải quyết vấn để khởi tạo 1 Object.
2. ***Nhóm cấu trúc***: Các nguyên mẫu thiết kế giúp bạn giải quyết vấn để liên quan đến thiết kế cấu trúc của 1 class như là *Inheritance*, *Composition*. 
3. ***Nhóm hành vi***: Các nguyên mẫu thiết kế này cung cấp các giải pháp để tương tác tốt hơn giữa các Object, lose coupling hoặc dễ dàng trong việc mở rộng trong tương lai.

## Nhóm khởi tạo
Bao gồm 5 design pattern như sau:
1. **Singleton**:
- **Định nghĩa**: Nguyên mẫu này giới hạn việc khỏi tạo 1 class, nó đảm bảo rằng chỉ duy nhất 1 *instance* của class được tạo ra.
- **Lợi ích**: Không lãng phí bộ nhớ khi chỉ khỏi tạo duy nhất 1 lần, Trong 1 số trương hợp bạn muốn chắc chắn rằng luốn chỉ có 1 instance duy nhất được sử dụng.
- **Khi nào dùng**: Khi bạn muốn có duy nhất 1 instance trong toàn bộ chương trình.
2. **Factory**
- **Định nghĩa**: Nguyên mẫu này chuyển trách nhiệm khởi tạo 1 object của 1 class sang Factory class
- **Lợi ích**: loose-coupling, khi bạn chỉ tương tác với factory class
- **Khi nào dùng**: Khi 1 class cha có nhiều class con và dựa trên các đầu vào khác nhau ta muốn khởi tạo các class con theo ý muốn
3. **Abstract Factory**
- **Định nghĩa**: Nguyên mẫu này giúp tạo Factory cho factory class ở mục 2
- **Lợi ích**: Giảm thiểu việc if else khi sử dụng Factory class theo mỗi class con mà nó implement
- **Khi nào dùng**: Giảm thiểu việc if else khi sử dụng Factory class theo mỗi class con mà nó implement
4. **Builder**
- **Định nghĩa**: Nguyên mẫu này giúp khởi tạo object dễ dàng hơn theo từng property 
- **Lợi ích**: Nó giúp giải quyết tính không nhất quán của object, object chỉ được khởi tạo và sử dụng khi tất cả các thuộc tính đã được cài đặt
- **Khi nào dùng**: Khi cần tính linh hoạt trong việc khỏi tạo object có quá nhiều tham số đầu vào, các tham số có thể là optional.
5. **Prototype**
- **Định nghĩa**: Khởi tạo object mới dựa trên 1 object đã có, rồi sau rồi sửa đổi theo yêu cầu mong muốn
- **Lợi ích**: Giảm thiểu thời gian cũng như tài nguyên khi khởi tạo object
- **Khi nào dùng**: khi muôn tạo ra 1 object giống những object đã có mà phải tổn rất nhiều thời gian cũng như tài nguyên

## Nhóm cấu trúc
Bao gồm 7 design pattern như sau:
1. **Adapter**:
- **Định nghĩa**: **Bộ chuyển đổi**, Cung cấp 1 interface để 2 thực thể không liên quan gì đến nhau có thể hoạt động được với nhau
- **Lợi ích**: Giúp các thực thể không liên quan đến nhau có thể hoạt động tốt với nhau
- **Khi nào dùng**: Khi cần liên kết giữa 2 thực thể không liên quan đến nhau
2. **Composite**:
- **Định nghĩa**: Nguyên mẫu này giúp xử lý 1 nhóm đối tượng theo cách xử lý của 1 object
- **Lợi ích**: Các thành phần được sắp xếp theo dạng tree, được đối xử với nhau theo cùng 1 cách xử lý
- **Khi nào dùng**: Composite Pattern được sử dụng khi chúng ta cần xử lý một nhóm đối tượng tương tự theo cách xử lý 1 object
3. **Proxy**:
- **Định nghĩa**: Nguyên mẫu này cung cấp surrogate hoặc placeholder để quản lý truy cập vào 1 object 
- **Lợi ích**: Ngăn chặn truy cập theo yêu cầu
- **Khi nào dùng**: Ngăn chặn truy cập theo yêu cầu
4. **Flyweight**: 
- **Định nghĩa**: Nguyên mẫu này giúp caching, sử dụng lại các object, thường được xử dụng với các immutable objects
- **Lợi ích**: Giảm thời gian khỏi tạo object, đỡ tốn bộ nhớ
- **Khi nào dùng**: Số lượng object khởi tạo lớn, việc khởi tạo object tốn nhiều bộ nhớ và thời gian
5. **Facade**: 
- **Định nghĩa**: Nguyên mẫu này giúp client tương tác với các hệ thống con 1 cách dễ dàng hơn
- **Lợi ích**: Giúp tương tác với các hệ thống con đơn giản, thuận tiện hơn
- **Khi nào dùng**: Khi bạn muốn tương tác với các hệ thống con khác nhau với cùng 1 mục đích như kết nối vào nhiều DB và cùng thực hiện 1 tác vụ là xuất báo cáo.
6. **Bridge**: 
- **Định nghĩa**: Nguyên mẫu này được sử dụng để tách interface khỏi việc implementation, và ẩn đi chi tiết việc implementation
- **Lợi ích**: Linh hoạt hơn trong việc implement các interface khác nhau thay 
- **Khi nào dùng**: khi bạn muốn sự linh hoạt trong việc implement các interface khác nhau, thay vì bó cứng vào 1 interface
7. **Decorator**: 
- **Định nghĩa**: Nguyên mẫu này được sử dụng để thay đổi chức năng của 1 object trong quá trình runtime
- **Lợi ích**: Linh hoạt hơn, dễ dàng sửa đổi và bảo trì cũng như mở rộng.
- **Khi nào dùng**: Khi bạn muốn linh hoạt hơn trong việc sửa dổi chức năng của object

## Nhóm hành vi
1. **Template Method**: 
- **Định nghĩa**: Nguyên mẫu này tạo trước 1 số hầm mẫu dùng chung và 1 số hàm sẽ phải implementation
- **Lợi ích**: Linh hoạt hơn, dễ dàng sửa đổi và bảo trì cũng như mở rộng.
- **Khi nào dùng**: Khi bạn muốn linh hoạt hơn trong việc sửa dổi chức năng của object
