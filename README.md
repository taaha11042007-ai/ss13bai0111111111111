PHẦN 1: PHÂN TÍCH LỖI GIAO DIỆN
1. Bảng phân tích chi tiết
Tiêu chí	Nội dung phân tích
Hiện trạng lỗi	Trường nhập liệu "Giới tính" đang sử dụng thành phần Checkbox (hộp kiểm vuông). Thành phần này cho phép người dùng kích hoạt cùng lúc cả 2 giá trị "Nam" và "Nữ", hoặc submit form mà không chọn giá trị nào nếu thiếu validation bắt buộc.
Hệ quả nghiệp vụ	• Gây xung đột logic dữ liệu hồ sơ người dùng (một tài khoản cá nhân thông thường chỉ mang một định danh giới tính duy nhất tại thời điểm đăng ký).
• Dẫn tới sai lệch số liệu thống kê nhân khẩu học, lỗi hệ thống luồng checkout/cá nhân hóa đề xuất sản phẩm về sau.
• Làm tăng tỷ lệ rời bỏ trang (drop-off rate lên tới 68%) do trải nghiệm nhập liệu gây bối rối.
Nguyên tắc UI vi phạm	• Affordance (Khả năng gợi ý hành động): Biểu tượng hình vuông của Checkbox theo quy chuẩn giao diện vốn gợi ý người dùng có thể chọn nhiều mục (Multiple choice). Việc sử dụng Checkbox cho một bài toán loại trừ lẫn nhau (Mutually exclusive) gây hiểu lầm nghiêm trọng về công năng.
• Clarity (Tính rõ ràng & Nhất quán): Không phản ánh đúng giới hạn và quy tắc nghiệp vụ "chỉ được chọn 1", làm tăng tải nhận thức (cognitive load) của khách hàng khi điền form.
Thành phần UI chuẩn thay thế	Radio Button (nút tròn đơn chọn).
Lý do chọn Radio Button	• Quy chuẩn Input Control: Radio Button được định nghĩa chuyên dụng cho các tập giá trị loại trừ lẫn nhau — khi kích hoạt một mục, toàn bộ các mục còn lại trong cùng nhóm (name attribute) sẽ tự động bị bỏ chọn.
• Tối ưu trải nghiệm (UX): Với số lượng tùy chọn ít (2–3 mục), Radio Button cho phép trải toàn bộ lựa chọn lên bề mặt giao diện, giúp người dùng nhận diện và hoàn tất thao tác chỉ với 1 click (nhanh hơn dạng Dropdown menu).
PHẦN 2: HƯỚNG DẪN CHỈNH SỬA TRÊN WIREFRAME FIGMA
Chỉ thực hiện can thiệp cục bộ tại hàng hiển thị Giới tính, duy trì định dạng Low-fidelity Wireframe (thang độ xám, không lên màu sắc, không dùng ảnh):

1. Quy cách thông số UI mới
Xóa thành phần cũ:

Xóa bỏ 2 khung vuông Checkbox hiện tại.
Xóa dòng text chú thích lỗi: [LỖI: Checkbox cho phép chọn cả 2 — cần sửa thành Radio Button].
Tạo thành phần Radio Button thay thế:

Trạng thái Chưa chọn (Unselected / Inactive):
Vẽ hình tròn đường viền nét đơn: Đường kính 16px × 16px (hoặc 18px × 18px).
Stroke: 1.5px (màu #333333 hoặc #000000).
Fill: None (hoặc nền trắng #FFFFFF).
Trạng thái Đã chọn (Selected / Active) - Minh họa mẫu 1 trạng thái:
Giữ nguyên khung tròn ngoài như trên.
Thêm một chấm tròn đồng tâm bên trong: Đường kính 8px × 8px, Fill: #333333 hoặc #000000.
Căn chỉnh bố cục (Layout & Spacing):

Cụm lựa chọn 1: (○) Nam — Khoảng cách giữa icon tròn và nhãn text "Nam" là 8px.
Cụm lựa chọn 2: (○) Nữ — Khoảng cách giữa icon tròn và nhãn text "Nữ" là 8px.
Khoảng cách giữa 2 nhóm: Khoảng cách giữa đuôi chữ "Nam" và icon (○) của mục "Nữ" duy trì từ 24px đến 32px để tránh bấm nhầm (đảm bảo diện tích vùng chạm / touch target).
Căn hàng: Căn đều trục ngang (Align Vertical Center) giữa các nút tròn và nhãn text với nhãn đề mục "Giới tính".
2. Trình bày trên Figma Canvas
Frame 1 — Before (Legacy UI): Giữ nguyên bản Wireframe lỗi ban đầu để đối chiếu.
Frame 2 — After (Fixed Wireframe): Wireframe đã thay thế trường Giới tính sang cụm Radio Button theo đúng tiêu chuẩn.
link figma : https://www.figma.com/design/6W3FC3JpvJshgytAMQyaCg/Session-13--V%25E1%25BA%25ADn-d%25E1%25BB%25A5ng-c%25C6%25A1-b%25E1%25BA%25A3n-S%25E1%25BB%25ACA-L%25E1%25BB%2596I-GIAO-DI%25E1%25BB%2586N-FORM-%25C4%2590%25C4%2582NG-K%25C3%259D-?node-id=0-1&p=f&t=SHZJJgfLBI3lkKdw-0

