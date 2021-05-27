# JS-Exam-Funix
Câu hỏi 1: Em hãy nêu cho anh mối liên hệ giữa javascript và processing js?
 Javascript là ngôn ngữ lập trình, processing js là thư viện được viết bằng js
Câu hỏi 2: jquery là gì, tại sao phải sử dụng jquery?
Jquery cũng là thư viên JS dựa trên cổng giao tiếp html dom,Dùng jquery để có thể viết code trực quan và ngắn gọn hơn
Câu hỏi 3: Scope trong js là gì? Nêu ví dụ scope nào thì dùng từ khóa khai báo biến nào?
Scope là phạm vi, Có global scope ( Var ngoài hàm) và local scope ( var trong hàm ), block scope dùng let sẽ khai báo được.
Câu hỏi 4: Em hãy viết cho anh 1 object có 2 thuộc tính là name và age, giá trị tùy em cho
var person {
name:"";
age:"";
}
Câu hỏi 5: Nếu anh ghi var person thì có giống var Person không em?
Khác nhau
Câu hỏi 6: Em tạo 1 file html, js hoặc viết code js trong file đó cũng được, em tạo 1 mảng có các số ngẫu nhiên, rồi em viết 1 hàm sắp xếp tăng dần mảng này
var arr = [1, 2, 4, 5, 9, 6];
function Sort(arr) {
    let NewValue;
    for (let i = 0; i < arr.length; i++) {
        NewValue = i;
        for (let j = i + 1; j < arr.length; j++) {
            if (arr[NewValue] > arr[j]) {
                NewValue = j;
            }
        }
        if (i !== NewValue) {
            let temp = arr[i];
            arr[i] = arr[NewValue];
            arr[NewValue] = temp;
        }
    }
    return arr;
}
console.log(Sort(arr));
Cẩu hỏi 7: Tạo object Car có 2 instance Vin, Kia
function Car(price, warranty) {
    this.price = price;
    this.warranty  = warranty ;
}
var Vin = new Car( 1000, "Good");
var Kia = new Car( 2000, "Bad");
console.log(Vin);
console.log(Kia);
Câu 8: Json là gì?
JSON là viết tắt của JavaScript Object Notation, là một kiểu định dạng dữ liệu tuân theo một quy luật nhất định mà hầu hết các ngôn ngữ lập trình hiện nay đều có thể đọc được. JSON là một tiêu chuẩn mở để trao đổi dữ liệu trên web.
Câu 9: Cách lấy data bằng jquery
Load() là một phương thức đơn giản nhất trong kỹ thuật ajax. Chức năng của nó là tải và hiển thị nội dung đã tải vào một phần tử HTML nào đó.
Cú pháp: load(url, params, callback)

url: URL Tiếp nhận, xử lý và gửi lại dữ liệu.
Params: lưu giữ các biến cần gửi đi.
Callback: hàm mà nó sẽ gọi đến sau khi quá trình Ajax hoàn tất .
Phương thức get()
Để gửi dữ liệu theo phương thức get() của kỹ thuật ajax. ta có cú pháp sau:

Cú pháp: get(url, params, callback)

Các tham số tương tự như phương thức load().

Phương thức post()
Tương tự như phương thức get() của kỹ thuật ajax, phương thức post giúp bảo mật dữ liệu gửi đi tốt hơn. ta có cú pháp sau:

Cú pháp: post(url, params, callback)

Các tham số tương tự như phương thức load().

Phương thức ajax()
Ngoài các phương thức trên, ajax() là một phương thức tổng quát phổ biến nhất để sử dụng tải dữ liệu bất động bộ. Phương thức này cho phép cấu hình và tùy chỉnh các thông số, không bị bó buột như các phương thức trên.
$.ajax({
  type: 'Loại gửi dữ liệu (POST hoặc GET)',
  url: 'URL Tiếp nhận, xử lý và gửi lại dữ liệu',
  data: { Các biến dữ liệu được gửi lên server.(ten_bien1:dữliệu,ten_bien2:dữliệu,...). Có thể sử dụng  var data = $('form#ID_form').serialize(); để lấy toàn bộ dữ liệu từ 1 form có id là ID_form},
  dataType: Kiểu dữ liệu trả về ('html','text','json','xml'),
  success: function(data) {
    Nội dung sẽ được thực thi sau khi nhận được dữ liệu từ server
  },
  error: function() {
    Nội dung sẽ được thực thi khi có lỗi phát sinh
  }
});
Câu 10: Selector trong jquery là gì ?
Selector chọn phần tử là chức năng quan trong của jQuery, như bạn thấy Selector bắt đầu bằng ký tự $. Selector cho phép bạn chọn phần tử HTML và tương tác với phần tử, Selector tìm kiếm và lựa chọn phần tử dựa trên id, class, thẻ, thuộc tính phần tử, giá trị phần tử và cả nội dung trong phần tử.
Câu 11: Cách thao tác cập nhật DOM bằng jquery thông qua selector?
Phương thức html( ) nhận nội dung html (bên trong HTML) của phần tử đã so khớp đầu tiên.
selector.html( )
Bạn có thể thay thế hoàn toàn một phần tử DOM với các phần tử HTML hoặc DOM đã xác định. Phương thức replaceWith( content ) thực hiện mục đích này rất hiệu quả.
selector.replaceWith( content )
Phương thức empty( ) gỡ bỏ tất cả node con từ tập hợp các phần tử đã so khớp, trong khi phương thức remove( expr ) gỡ bỏ tất cả các phần tử đã so khớp từ DOM.
selector.remove( [ expr ])

or 

selector.empty( )
Phương thức after( content ) chèn content sau mỗi phần tử đã so khớp, trong khi phương thức before( content ) chèn content trước mỗi phần tử đã so khớp.
selector.after( content )

or

selector.before( content )
1	after( content )
Chèn content sau mỗi phần tử đã so khớp

2	append( content )
Phụ thêm content tới bên trong mỗi phần tử đã so khớp

3	appendTo( selector )
Phụ thêm tất cả phần tử đã so khớp tới tập hợp phần tử đã cho khác

4	before( content )
Chèn content trước mỗi phần tử đã so khớp

5	clone( bool )
Mô phỏng các phần tử DOM đã so khớp, và tất cả các Event Handler của chúng, và chọn các mô phỏng đó

6	clone( )
Mô phỏng các phần tử DOM đã so khớp và chọn các mô phỏng đó

7	empty( )
Gỡ bỏ tất cả các node con từ tập hợp các phần tử đã so khớp

8	html( val )
Thiết lập các nội dung HTML của mỗi phần tử đã so khớp

9	html( )
Nhận các nội dung HTML (HTML bên trong) của phần tử đã so khớp đầu tiên

10	insertAfter( selector )
Chèn tất cả phần tử đã so khớp vào sau tập hợp các phần tử đã xác định khác

11	insertBefore( selector )
Chèn tất cả phần tử đã so khớp vào trước tập hợp các phần tử đã xác định khác

12	prepend( content )
Thêm vào trước content tới bên trong mỗi phần tử đã so khớp

13	prependTo( selector )
Thêm vào trước tất cả phần tử đã so khớp tới tập hợp các phần tử đã xác định khác

14	remove( expr )
Gỡ bỏ tất cả phần tử đã so khớp từ DOM

15	replaceAll( selector )
Thay thế các phần tử đã so khớp bởi Selector đã cho với các phần tử được so khớp

16	replaceWith( content )
Thay thế tất cả phần tử đã so khớp với các phần tử HTML hoặc DOM đã xác định

17	text( val )
Thiết lập các nội dung text của tất cả phần tử đã so khớp

18	text( )
Nhận các nội dung text đã tổ hợp của tất cả phần tử đã so khớp

19	wrap( elem )
Bao bọc (wrap) mỗi phần tử đã so khớp với phần tử đã xác định

20	wrap( html )
Wrap mỗi phần tử đã so khớp với nội dung HTML đã xác định

21	wrapAll( elem )
Wrap tất cả phần tử trong tập hợp đã so khớp vào trong một phần tử bao bọc đơn (elem ở đây là phần tử DOM)

22	wrapAll( html )
Wrap tất cả phần tử trong tập hợp đã so khớp vào trong một phần tử bao bọc đơn (html là phần tử HTML)

23	wrapInner( elem )
Wrap các nội dung con bên trong mỗi phần tử đã so khớp (bao gồm các node văn bản) với một phần tử DOM

24	wrapInner( html )
Wrap các nội dung con bên trong mỗi phần tử đã so khớp (bao gồm các node văn bản) với một cấu trúc HTML
