---
title: Trang chủ
description: Các phương pháp đạt được tính linh hoạt, khả năng di động và khả năng mở rộng khi xây dựng các ứng dụng phần mềm dưới dạng dịch vụ (SaaS).
hide:
 - toc
 - navigation
---

## Giới thiệu

Ngày nay, phần mềm thường được chuyển giao như là một dịch vụ: còn được
gọi là *các ứng dụng web*, hay *phần mềm-như-một-dịch vụ (software-as-a-service)*.
Ứng dụng 12-hệ số là một phương pháp để xây dựng các ứng dụng phần mềm-như-một-dịch vụ với
các tiêu chí sau:

* Sử dụng các định dạng theo kiểu **tường thuật** cho việc thiết lập tự động hoá, để
cắt giảm chi phí và thời gian cho lập trình viên mới tham gia dự án;
* Có một **hợp đồng sạch** với hệ điều hành bên dưới, cung cấp **tối đa khả năng dịch chuyển** giữa các môi trường thực thi;
* Phù hợp để **triển khai** trên các **nền tảng đám mây** mới, cắt giảm yêu cầu quản trị
cho server và hệ thống;
* **Giảm thiểu sự khác nhau** giữa môi trường phát triển và môi trường sản xuất, cho phép đạt được sự linh hoạt tối đa
trong **triển khai liên tục**;
* Và có thể **mở rộng** mà không cần thay đổi lớn cho các công cụ, kiến trúc, hoặc cách thức
phát triển.

Phương pháp 12-hệ số có thể được áp dụng cho các ứng dụng viết bằng bất kì ngôn ngữ lập
trình nào, và sử dụng bất kì kết hợp giữa các dịch vụ backend (cơ sở dữ liệu, queue, memory cache, vv.).

## Gốc gác

Tất cả tác giả của tài liệu này đã trực tiếp tham gia vào quá trình phát triển và triển
khai của hàng trăm ứng dụng, và gián tiếp theo dõi các quá trình phát triển, vận hành,
và mở rộng của hàng nghìn ứng dụng thông qua công việc của chúng tôi trên hệ thống [Heroku](http://www.heroku.com/).

Tài liệu này là cô đọng của tất cả kinh nghiệm và quan sát của chúng tôi trên một số lượng
lớn các ứng dụng-như-một-dịch vụ ở ngoài. Đây là kết hợp của kiến thức thực hành chuẩn mực
trong việc phát triển ứng dụng, với trọng tâm vào cơ cấu phát triển cơ bản của ứng dụng trong
một khoảng thời gian, cơ cấu động của sự hợp tác giữa các lập trình viên đang làm việc trên
cùng một mã gốc, và [tránh rò rỉ chi phí phát triển phần mềm](http://blog.heroku.com/archives/2011/6/28/the_new_heroku_4_erosion_resistance_explicit_contracts/).

Động lực của chúng tôi là tăng cường nhận thức về các vấn đề hệ thống mà chúng tôi biết
với các qui trình phát triển ứng dụng hiện tại, để chia sẻ một kho kiến thức thảo luận
về các vấn đề này, và để cung cấp một chuỗi các giải pháp mở chác vấn đề trên và cũng đi kèm
với các thuật ngữ chuyên môn. Định dạng này lấy ý tưởng từ cuốn sách *[Patterns of Enterprise Application Architecture](http://books.google.com/books/about/Patterns_of_enterprise_application_archi.html?id=FyWZt5DdvFkC)* và *[Refactoring](http://books.google.com/books/about/Refactoring.html?id=1MsETFPD3I0C)* của ông Martin Fowler.

## Ai nên đọc tài liệu này?

Bất kì lập trình viên đang xây dựng các ứng dụng-như-một-dịch vụ. Các kỹ sư hệ
thống đảm nhiệm triển khai hoặc quản lý các ứng dụng.

## 12 hệ số

### [I. Mã gốc](./codebase.md)

Một mã gốc được theo dõi với hệ thống quản lý phiên bản, và nhiều lần triển khai

### [II. Các phụ thuộc](./dependencies.md)

Khai báo rõ ràng và phân tách các phụ thuộc

### [III. Cấu hình](./config.md)

Lưu trữ cấu hình trong môi trường

### [IV. Dịch vụ hỗ trợ](./backing-services.md)

Dịch vụ hỗ trợ như là tài nguyên bổ xung

### [V. Xây dựng, phát hành, vận hành](./build-release-run.md)

Tách biệt hoàn toàn giữa bước xây dựng và vận hành

### [VI. Tiến trình](./processes.md)

Vận hành ứng dụng như là một hoặc nhiều tiến trình phi trạng thái

### [VII. Mở cổng mạng](./port-binding.md)

Cung cấp các dịch vụ thông qua công mạng

### [VIII. Đồng bộ](./concurrency.md)

Mở rộng theo chiều ngang thông qua mô hình tiến trình

### [IX. Tính khả dụng](./disposability.md)

Tối ưu hoá với khởi động nhanh và dừng phần mềm ổn định

### [X. Sự tương đồng giữa quá trình phát triển và vận hành thực tế](./dev-prod-parity.md)

Đảm bảo sự tương đồng giữa môi trường phát triển, kiểm thử và thực tế

### [XI. Nhật ký](./logs.md)

Nhật ký là các luồng sự kiện

### [XII. Tiến trình quản trị](./admin-processes.md)

Thực thi nhiệm vụ quản trị như là một tiến trình
