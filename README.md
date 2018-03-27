# Tại sao không nên dùng bản alpha cho dự án của mình?
Tại vì bản alpha chưa hoàn chỉnh có thể có bug nào đó không mong muốn
Nhưng vì bản alpha đã bao gồm toàn bộ các tính năng nên có thể dùng để tìm hiểu trước.


# Chuyển từ sử dụng less sang sử dụng sass
Điểm khác biệt: 

## Les
- Viết trên javascript
- Sử dụng tiền tố @ cho biến
- Import cần phần mở rộng
## Sass
- Viết trên ruby
- Sử dụng tiền tố $ cho biến
- Không cần phần mở rộng
# Điểm mới trong bs4
## Chuyển hệ tính từ pixel sang rem
BS4 đã chuyển sang dùng đơn vị tương đối rem thay vì dùng đơn vị tuyệt đối px điều này làm nó có kích thước co dãn tốt hơn. 
Không còn hỗ trợ IE8
Động thái hướng đến việc sử dụng flexbox thật sự đã thúc đẩy một thay đổi khác: hỗ trợ trình duyệt. Bootstrap v4 đã chính thức loại bỏ sự hỗ trợ cho Internet Explorer 8, 9 và iOS 6. Điều này có nghĩa là các trang Bootstrap của bạn sẽ chỉ hỗ trợ IE10 + và iOS 7+

## Flex là một tuỳ chọn
Nếu bạn không muốn sử dụng flex bạn có thể tắt nó trong _variable.scss và rebuild lại.
## Bỏ Glyphicons Font
Nhiều khi Glyphicon không hiển thị trong một vài thiết bị, do đó bs4 bỏ nó và chúng ta sẽ phải tự bao gồm. Thông thường e hay dùng fontawesome.
## Thay thế Panel bằng Card
BS4 đã loại bỏ panel, well, thumbnail thay vào đó là khuyến khích sử dụng thành phần card mới thay thế.
## Thêm Outline button
Bổ sung thêm một phong cách button đơn giản mà đẹp, mới màu sắc chỉ bọc ngoài đường viền.
Cách sử dụng: “btn btn-outline-primary”
## Spacing
Cấu trúc :[margin or padding]-[direction]-[size]
Ví dụ: “ml-lg-4”, “pb-sm-2”
## Display 
Bổ sung một số class mới từ Display-1 tới Display-4
Giúp làm nổi bật tiêu đề tốt hơn.
# Nêu các ưu điểm của flexbox?
Tính mềm dẻo
Căn chỉnh thứ tự trên dưới của các phần tử, căn chỉnh ngang, căn chỉnh theo chiều dọc, căn chỉnh center các phần tử trở nên đơn giản hơn rất nhiều.
Bạn chỉ cần điều chỉnh kích thước một lần là nó sẽ tự động cập nhật cho mọi thiết bị.
# Nêu 1 số khác nhau giữa ES6 với ES5? BS4 sử dụng gì để compile Javascript
## ES5:
- Sử dụng function bình thường
- Không sử dụng callback xử lí async
- Nhập xuất module
- module.exports = myModule;
- var myModule = require('./myModule');
- Phạm vi biến toàn cục sử dụng var
- Không có giá trị mặc định cho tham số
- Không hỗ trợ trực tiếp nhị phân bát phân
## ES6
- Rút gọn code với arrow function
- Sử dụng promise xử lí async
- Nhập xuất module
- export default myModule;
- import myModule from './myModule';
- Phạm vị biến cục bộ sử dụng let
- Có giá trị mặc định cho tham số
- Hỗ trợ trực tiếp nhị phân bát phân
## BS sử dụng ES6 để compile js
# Cách ghi đè variable của bootstrap?
    - Tạo file custom variable.scss định nghĩa các biến mới
    - Import vào sau file _variable.scss của bs
# Mô tả  basic workflow của sass với bs4 được giới thiệu trong video?
    - Sử dụng source của BS compile lại sass kết hợp với custom scss của mình.
    - Tắt tất cả các component, untility trong boostrap.scss
    - Trong quá trình code sử dụng đến phần nào thì bật phần đó lên tránh bật thừa những component, untility không sử dụng.
