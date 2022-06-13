---
layout: default
title:  "Có nên học Kotlin thay vì java khi sử dụng Spring framework?"
date:   2022-06-07 17:50:00
categories: Spring
---
# Có nên học Kotlin thay vì java khi sử dụng Spring framework?
Trước đây khi tiếp cận lần đầu tiên với Java mềnh đã nghĩ rằng:
> Java có 1 cấu trúc viết rất đầy đủ và dễ hiểu

<p>Sẽ chẳng là vấn đề gì cho đến khi mình bắt đầu có thời gian và tiếp cận với các ngôn ngữ khác như JS, TS, python...
để rồi mình cảm nhận thấy, hmm <i>Cũng là ngôn ngữ lập trình đấy nhưng mà nó lạ lắm.</i> </p>
<br>
Có ông anh ở công ty cũ đã từng nhận xét với mình rằng:
> Code java rườm ra bỏ m*, code xong cái app java thì chắc phải xong mấy cái bằng ngôn ngữ khác rồi.

<p>Ừm thì nói chung Java là 1 trong những ngôn ngữ đã có từ khá lâu, thậm chí nó còn lớn tuổi hơn cả mềnh ._. </p>
<p>May mắn thay, chúng ta đã có Kotlin giải quyết cái vấn để rườm ra trong việc lập trình của java. Không chỉ vậy  
nó còn mang đến những sự cập nhất thực sự là hữu ích mà Java không hề có.</p>

### Kotlin là gì? 

> Kotlin là ***Statically typed language***, được phát triển bời jetbrain, ra đời vào năm 2011.

Mềnh xin phép không dịch cái cụm đen đen bên trên vì nó dịch ra tiếng việt hơi chuối, về cơ bản thì 
***Statically typed language*** để nói về những ngôn ngữ mà kiểu dữ liệu của biến phải được khải báo lúc compile time.

### Những tính năng chính của Kotlin.

> 100% tương thích với Java

Đây là 1 trong những điểm mà mình thích nhất khi bắt đầu học về kotlin. Nó có nghĩa là bất kì thư viện nào bạn đã từng làm việc
với Java nó cũng tương thích hoàn hảo khi dụng với Kotlin mà không cần sửa đổi bắt cứ gì.

<div class="tenor-gif-embed" data-postid="5074749" data-share-method="host" data-aspect-ratio="1.77778" data-width="100%"><a href="https://tenor.com/view/hey-thats-pretty-good-good-pretty-good-gif-5074749">Hey, That&#39;S Pretty Good - Idubbbztv GIF</a>from <a href="https://tenor.com/search/hey+thats+pretty+good-gifs">Hey Thats Pretty Good GIFs</a></div> <script type="text/javascript" async src="https://tenor.com/embed.js"></script>
<br>

> Code ngắn ngọn hơn rất nhiều so với Java cho cùng 1 mục đích.

Cái này thì các ví dụ bên dưới sẽ chỉ ra rất rõ việc đó.

> Nhiều nâng cấp được thêm vào mà mãi đến các version sau này của java mới có.

> Null-Safe

Một trong những điểm khiến mềnh và có lẽ hàng nghìn coder khác cũng có cũng cảm giác nhức ngồi này đấy là 
NullPointerException. Nhưng không, với Kotlin thì gần như không bao giờ phải lo lắng về vấn đề này nữa.

### Có nên học Kotlin thay vì java khi sử dụng Spring framework?

Cùng đi vào vấn đề chính của bài viết ngày hôm nay. Nên hay không nên sử dụng Kotlin thay cho java?

> Có

<p>Nói ngắn gọn lại thì với những ưu điểm trên thì tại sao lại không chứ chỉ? và 1 vấn đề quan trọng hơn nữa đó là 
từ bản Spring framework 5.0, Spring boot 2.2 Kotlin đã hoàn toàn được support, tất cả các vấn đề khả năng bị null khi chuyển từ java sang 
Kotlin đã có người khác làm hộ cho rồi (quá ngon). Cùng với đó thì Document cũng như các Example rất hoàn hảo để cho bạn 
có thể bắt đầu ngay lúc này. </p>

### Lợi ích của việc code ngắn ngọn

Không thể phủ nhận được 1 điều là code ít đi nghĩa là bạn sẽ có nhiều thời gian hơn để làm các việc khác. Tuy nhiên thì
 nó không chỉ dừng lại tại đó mà còn có các lợi ích khác như:
1. Khả năng đọc hiểu code dễ dàng hơn
2. Code ít hơn -> sẽ có ít chỗ bị dính bug hơn (không code thì không bug?)
3. Hầu hết các trường hợp code common đều đã được kotlin hỗ trợ sẵn
4. Framework lúc này cũng không phải load nhiều code ngầm.

### Cùng điểm qua 1 chút về Syntax của Kotlin 

**Variables và value**

Trong Kotlin chúng ta có variables và value. Variable có thể thay đổi giá trị, cùng nhìn ví dụ dưới đây


```kotlin
var fullName: String = "hieugie"
```

 Chúng ta có 1 variable với tên là `fullName`, có kiểu dữ liệu là `String` với giá trị là `hieugie`, và vì là variable 
 chúng ta hoàn toàn có thể thay đổi giá trị của biến fullname này.
 
```kotlin
fullname = "another name"
```

Ngược lại thì value không thể thay đổi sau khi khởi tạo:

```kotlin
val fullName: String = "hieugie"
```

Khi cũng ta thử thay đổi giá trị của `fullName` sẽ dẫn tới lỗi `compile error`

```kotlin
fullName = "another name"  // compile error
```

### Type Reference

Nhìn vào cách khai báo Variable và value ở bên trên ta có thể thấy có sự hơi khang khác so với java. Nhưng cái hay ở chỗ 
kolin cho phép ta thậm chí lượng bỏ hoàn toàn Type Reference khi khai báo biến, cụ thể thì ta có thể khai báo như sau


```kotlin
val fullName = "hieugie"
val age = 30
```

thay thế cho việc khai báo:

```kotlin
val age: Int = 30
val fullName: String = "hieugie $age tuổi"
```

Nó như kiểu 1 sự thật hiển nhiên vậy, giống như việc mặt trăng quay quanh trái đất, chúng ta nhìn vào có thể nhận thấy 
ngay fullName là String, age là Int không có gì cần phải bàn cãi. Nó làm code đơn giản hơn rất nhiều
Một điều nữa là không cần phải chấm phẩy ở cuối mỗi dòng, điều này làm mình khá thích thú

## So sánh bằng trong kotlin

Trong Java chắc hẳn mọi người cũng biết, với kiểu nguyên thuỷ thì chúng sẽ sử dụng toán tử `==` với kiểu object thì sử 
dụng hàm `equals()` để so sánh. Nhưng trong kotlin thì chỉ cần sử dụng  toán tử `==` mà không cần phải suy nghĩ nhiều

```kotlin
val myName = "hieugie"
val otherName = "HIEUGIE"

// So sánh bằng

myName == otherName.toLowerCase() // kết quả sẽ trả về true
```

Nhưng trong trường hợp bạn muốn so sánh cái giá trị reference thì. yeah, với kotlin bạn vẫn có thể bằng cách sử dụng 
toán tử `===`

```kotlin
myName === otherName // Kết quả trả về false
```

### Raw String 

Đã bao giờ bạn copy 1 chuỗi String vào code của mình mà chứa những ký tự đặc biệt để rồi nó trông rất đần độn chưa.
yeah, mình thì hay gặp phải khi xử lý các chuỗi json. Nhưng khi sang với kotlin thì hết rồi nhé:

```
val json = { \"key\": \"value\" } // 1 chuỗi nhìn hết sức ngu ngốc như này 
```

Còn bây giờ thì nó sẽ trông như này đối với kotlin

```kotlin
val json = 
"""
 {"key": "value"}
"""
```

### Null safety 

Điều mà mình thực sự thích của kotlin là đây, Kotlin đảm bảo với bạn sang sẽ không bao giờ có chuyện null sảy ra. Giả 
sủ mình khai báo 1 String như sau

```kotlin
var fullName: String = "hieugie"
```

Kotlin sẽ không cho phép bạn khai báo 1 biến với giá trị null, tuy nhiên nếu bạn muốn giá trị có thể null thì sao? Bạn 
có thể sử dụng dấu hỏi chấm (?) ngay sau kiểu dữ liệu mà bạn mong muốn:

```kotlin
var age: Int? = null
```

Vây chuyện gì sẽ sảy ra khi bạn code với dấu hỏi chấm cho phép null như bên trên? các hàm liên quan đến biến đó sẽ không
được phép sử dụng trừ trường hợp bạn sử dụng dấu hỏi chấm cùng với biến đã khai báo:

```kotlin
var fullName: String? = "hieugie"

fullname.toUpperCase() // compiler sẽ báo lỗi ngay tại đây vì biến fullname này có thể null

fullName?.toUpperCase() // trường hợp null thì sẽ không bị throw exception gì
```

Chắc hẳn syntax này đã quá quen với những bạn đã từng code các ngôn ngữ khác như C# hoặc TypeScript.

### Toán tử elvis

Đã bao giờ bạn viết code java kiểu như

```java
String data = json != null ? json : "hello";
```

Rất thường xuyên phải không, còn đối với kotlin thì sao? nó gọn hơn rất là nhiều khi áp dụng toán tử elvis

```kotlin
val fullName: String? = "hieugie"
val otherName: String = fullName ?: "other name"  
```

Cho bạn nào không hiểu thì đơn giản là nếu như phần tử đầu tiên không null thì lấy, còn nếu bị null thì lấy giá trị
phần tử thứ 2.

ơ nhưng mà trong trường hợp ví dụ bên trên, bạn biết rõ ràng cái fullName nó không bị null mà, cần gì phải có cái
`other name` nữa đâu. Đừng lo lắng vì đã có toán tử (!!). Kiểu như nó sẽ bảo cho kotlin rằng: "`Tao biết tao đang 
làm gì cứ gán giá trị vào cho tao đi, nó đéo thể null được đâu`"

```kotlin
val fullName: String? = "hieugie"
val otherName: String = fullName!! 
```

Đến lúc này sẽ có bạn thắc mắc là: "`ơ thế nếu cái fullname nó null thì sao `". yeah yeah yeah, thì lúc này nó sẽ throw
nullPointerException chứ sao. Thằng nào nó bảo kotlin không có null là lừa đấy đừng tin nó 

```kotlin
val fullName: String? = null
val otherName: String = fullName!! 

// Lúc này sẽ throw NullPoiterException!!!!!!
```

### Expressions - If, Try - catch, When

Đã bao giờ bạn code kiểu nếu như A thì trả về 1, B thì trả về 2... chưa? Java thì rất ra rườm rà đúng không, hãy xem 
kotlin nó làm như nào nhé:

```kotlin
val data = if (code = "a") {
    1
} else {
    2
}
```

thể con Try catch thì sao, kiểu như bạn muốn ép kiểu từ kiểu này sang kiểu khác và muốn gán giá trị?

```kotlin
val data = try {
    code.toUpperCase();
} catch(e: Exception) {
    "Hello"
}
```

Lạ hơn 1 chút thì ta có cú pháp `When` cụ thể như sau

```kotlin
val x = when(data) {
    0 -> "Hello"
    in 1..10 -> "data trong khoảng từ 1 đến 10"
    in someSet -> "Data thuộc 1 set nào đó"
    is someType -> "Data có kiểu dữ liệu"
    parseString(data) -> "Có cùng kiểu với parseString"
    else  -> "Không biết gì luôn"
}
```

## Ép kiểu thông minh

Cùng xem ví dụ sau để hiểu rõ hơn nó là gì nhé 

```kotlin
val x = when(data) {
    is Int -> data + 1
    is String -> data.length + 1
    is IntArray -> data.sum() + 1
}
```

Có thể thấy rằng chưa biết data có kiểu dữ liệu gì nhưng các dòng lệnh tiếp theo đã ép đúng kiểu như ta mong muốn 
nếu như điều kiện đúng: `is Int` nếu là Int thì data lúc này đã đc kotlin ép về kiểu Int, không như Java để làm được việc
này thì bản phải làm kiểu như `Integer.parseInt(data) + 1`

### Classes Trong kotlin

Trong kotlin thì chúng ta sẽ không con keywords extends hay implements nữa và mặc định class trong kotlin là final. Điều
này khiến cho Developer phải nghĩ ngay đến việc có cho phép các Class khác kế thừa lại không. nếu có chúng ta có thể
sử dụng keyword open 

```kotlin
open class Dog: Animal {

}

class Dog: Animal {

}
```

### No more getter and setter

Nó là mặc định trong kotlin, bạn sẽ hoàn toàn quên mất nó khi sử dụng kotlin

```kotlin
class Dog {
    var name: String? = null
}

var aDog = Dog() // sẽ không còn keyword new nữa đâu nhé

aDog.name = "chihuahua" // bằng việc gọi `.name` sẽ gọi hàm setter name cho object chó này 
println("The dog name {$aDog.name}") // // bằng việc gọi `.name` sẽ gọi hàm getter name của object chó này
```

Vậy đó mặc định đã có getter và setter cho properties trong class, ơ vậy nhỡ như mềnh muốn hàm setter nó hoạt động 
khác so với bình thường, kiểu như cái tên này lúc nào gán cho con chó nó cũng phải in hoa cơ, thì sao? No worry, với 
kotlin bạn hoàn toàn có thể làm được điều này bằng cách override hàm setter của nó 

```kotlin
class Dog {
    var name: String? = null
        set(value) {
            field = value?.toUpperCase();
        }
}
```

### data class 

Bình thường khi thao tác với 1 lớp POJO, chắc chắn chúng nó để thao tác với nó sẽ phải viết các hàm cơ bản như getter,
setter, toString(), equals(), hashCode(), rất nhiều thứ phải không, nhứng với kotlin chỉ với `data class` nó thay thế
hết các thứ thừa thãi bên trên 

```kotlin
data class Dog (val name)
```

### Copying data class

Đôi khi bạn có 1 cái POJO to vật vã và muốn copy nó nhưng lại muốn thay đổi 1 số thuộc tính như mong muốn. Tất nhiện 
với kotlin thì nó khá là đơn giản

```kotlin
val student = Student("John Doe", 15);

val otherStudent = student.copy(fullname = "Other")
// Lúc này sẽ tạo ra đc student mới với tên Other, và tất cả các thuộc tính khác thì giữ nguyên như cũ
```

### Function 

Cùng lướt qua 1 chút về function trong kotlin. Cùng xem cấu trúc đầy đủ của 1 function như thế nào nhé 

```kotlin
fun createNewUser(): String {
    return "John Doe"
}
```

Trong ví dụ trên thì cái function của mình chỉ có 1 nhiệm vụ duy nhất là trả về cái tên `John Doe`. Trong kotlin bạn có 
thể khai báo 1 function với chỉ 1 expression duy nhất như trên:

```kotlin
fun createNewUser(): String = "John doe"
```

Tất nhiên bạn có thể bỏ luôn cái kiểu dữ liệu trả về luôn cũng được thì Kotlin nó tự động hiểu cho mình luôn 

```kotlin
fun createNewUser() = "John doe"
```

### Function với giá trị default 

Cùng nhìn vào ví dụ sau:

```kotlin
fun hello(fullName: String = "John doe"): String {
 return "hello $fullName";
}
```

Bạn hoàn toàn có thể khai báo giá trị default cho mọi tham số truyền vào của, nghĩa là khi mềnh gọi cái function hello,
mềnh hoàn toàn có thể lược bỏ phàn truyền vào tham số fullName, vì nó đã có giá trị default rồi và mình k muốn thay đổi nó

```kotlin
hello() // hello John doe
hello("hieugie") // hello hieugie
```

Tất nhiên khi truyền tham số thì nó vẫn nhận tham số như bình thường. Và cái này hay ở chỗ, bình thường khi bạn add thêm
1 hoặc 1 số tham số truyền vào cho function, thì với Java theo SOLID thì mình sẽ phải overloading cái function. Còn ở 
Kotlin có thể không cần, chỉ cần thêm tham số và truyền giá trị default cho nó. 

```kotlin
fun plus(first: Int, second: Int): Int {
 return first + second
}

fun plus(first: Int, second: Int, third: Int = 0): Int {
 return first + second + third
}

// Bây giờ thì bạn có thể gọi function này theo 2 cách như trên đã nói
plus(1, 2) // 3
plus(1, 2, 3) // 6
```

Và 1 điều nữa mình thích đó là kotlin có Named Parameters, nghìa là bạn có gọi function theo bất kì cách nào bạn muốn:

```kotlin
plus(1, 2)
plus(second = 2, first = 1)
plus(first = 2, second = 1)
plus(second = 2, third = 3,  first = 1)
```

### Extension function

```kotlin
fun Int.isEven(): Boolean {
    return this % 2 == 0
}
```

Khác với Java thì bạn sẽ phải viết 1 hạm static để có thể check số là chẵn hay lẻ, tuy nhiên với kotlin như trên thì giờ 
đây nó hiểu rằng Int luôn có hàm isEven() , như kiểu là nó luôn thuộc về biến Int vậy, cho nên từ bây giờ trở 
đi bất kì biến Int nào cũng có hàm isEven():

```kotlin
10.isEven()  // True
```

### use Extension

Ở Java 7 thì nó có giới thiệu cho chúng ta thêm API, try with resource, nghĩa là nó sẽ mở Resource này ra nếu có thể
và sẽ đóng nó lại khi hết hàm.

```java
try (Connection conn = getConnection()) {
    // some code
}
```

Còn với kotlin thì gọn với với use expression và đưa cho 1 hàm lambda

```kotlin
getConnection().use { conn -> 
 // do something
}
```

### apply Extension

Giả sử mềnh muốn khai báo 1 Student với tên và tuổi, thì như bình thường với những code Java thì sẽ nghĩ theo hướng 
như sau

```kotlin
val student = Student() // expression
student.name = "hieugie" // statement
student.age = 17 // statement
```

Điều này sẽ tốn 1 expression và 2 statement. Nhưng với kotlin thì bạn hoàn toàn có thể làm việc này chỉ bằng 1 single 
expression, điều này rất hay vì single expression trong kotlin là 1 cái gì đó rất đặc biệt:

```kotlin
val student = Student().apply{
    name = "hieugie"
    age = 17
}
```

### 1 số điều khác với function

1. Function thì default của nó là final, như mình đã nói, kotlin muốn bạn suy nghĩ về việc có cho phép nó được extends hay không ngay từ đầu
2. Tham số truyền vào của Function cũng là final
3. Function hoàn toàn có thể định nghĩa ở ngoài class 
4. Function có thể đc định nghĩa bên trong 1 function khác 
5. Kotlin support tail recursive.

### Checked exception

Trong kotlin thì không có checked exception, tất cả exception trong kotlin đều là RunTimeException


# Kết luận

Còn rất nhiều những thứ tuyệt vời khác Kotlin có mà mình không thể đề cập hết trong bài viết này nhưng chốt lại thì tại 
sao mềnh nên chuyển qua dụng kotlin?

1. Mềnh code ít hơn rất nhiều
2. Code mềnh viết ra sẽ rất rõ ràng và dễ hiểu hơn rất nhiều 
3. Mềnh tránh đuọc rất nhiều các thể loại defect, những thứ mà kotlin đã xử lý hết cho mềnh, như null
4. Nó hoàn toàn tương thích với các tool dành cho Java như Spring, Intellij ....