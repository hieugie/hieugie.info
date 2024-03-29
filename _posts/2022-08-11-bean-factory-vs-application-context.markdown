---
layout: post
title:  "Bean factory vs Application Context"
date:   2022-08-11 00:00:00
categories: Interview_Question
tags: Interview Question
---

### Application context vs Bean Factory trong Spring giống và khác nhau như nào?

Về cơ bản thì hiếm có bao giờ tôi sử dụng 2 cái interface này, và chắc hẳn nhiều bạn cũng như thế. Tuy nhiên thì trong các buổi phỏng vấn bạn vẫn có thể bị hỏi 1 câu như này.
<br>
Tất nhiên là bạn cũng chẳng thể trả treo lại kiểu như
> Anh có dùng bao giờ không mà hỏi làm m* gì?
<!-- more -->
Thì đây là câu trả lời mà mềnh biết:

## Bean Factory:
1. Lazy load bean (Bean bạn cần sẽ không được khởi tạo khi chưa gọi hàm getBean)
2. Only support singleton, prototype
3. Do not support internationalization
4. Do not register BeanFactoryPostProcessor and BeanPostProcessor at start up

## Application Context
1. Eager load bean (Bean bạn cần sẽ được khởi tạo trước mặc dù chưa gọi hàm getBean)
2. Support all type of bean scope
3. Support internationalization
4. Registers BeanFactoryPostProcessor and BeanPostProcessor at start up

DRY (Don’t Repeat Yourself)
This principle states that each small pieces of knowledge (code) may only occur exactly once in the entire system. This helps us to write scalable, maintainable and reusable code.

KISS (Keep it simple, Stupid!)
This principle states that try to keep each small piece of software simple and unnecessary complexity should be avoided. This helps us to write easy maintainable code.

YAGNI (You ain't gonna need it)
This principle states that always implement things when you actually need them never implements things before you need them.
