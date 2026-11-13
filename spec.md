# Dàn ý bài nộp *(spec.md — nộp trước 23:59 ngày lab của lớp)*

> Copy dàn ý này vào `spec.md` của nhóm. Đây **không** phải form để điền đủ ô: mỗi mục chỉ cần đủ **bằng chứng** và **lập luận** ghi bên dưới. Viết ngắn, gạch đầu dòng là được. Hướng dẫn từng chặng: `02-guide.md`. Cách chấm: `04-rubric.md`.
>
> **Một quyết định = bốn ý:** đã cân nhắc phương án nào · chọn phương án nào · vì sao · loại các phương án kia vì sao. Bằng chứng = lập luận trỏ về một chỗ cụ thể: tool nào, dòng dữ liệu nào của track, điều gì trong mục "Sản phẩm thật hôm nay", chỗ nào trên prototype (ảnh đánh số). Không chạy agent.

```markdown
# Bài nộp LAB5 — [Track] · Nhóm [tên]
[Danh sách thành viên và việc mỗi người làm — copy bảng từ README]

## §1. Lát cắt & phạm vi
- Lát cắt: Trong trợ lý học bài của trang khoá học (kiểu ChatGPT Study mode), khi học viên đang hỏi bài lúc tối muộn, khi không còn ai để hỏi, AI giảng kèm trích tài liệu, hỏi lại cho rõ, gợi ý từng bước, hay nói thẳng "tài liệu không có, hỏi giảng viên", để học viên hiểu đúng bài mình đang học, không chép đáp án, không học sai mà không biết.
- 3 việc tính năng KHÔNG làm, mỗi việc một câu vì sao: 
1. Không giải hộ hoặc xác nhận đáp án bài tập đang mở. Vì học viên có thể sao chép kết quả mà không thực sự hiểu bài, làm mất mục đích học tập và tính công bằng trong đánh giá.
2. Không tự tạo kiến thức hoặc trích dẫn nguồn không tồn tại. Vì thông tin sai hoặc không có căn cứ có thể khiến học viên hiểu nhầm, học sai và mất niềm tin vào hệ thống.
3. Không tự ý đăng nội dung chưa được TA hoặc giảng viên kiểm duyệt lên FAQ cả lớp. Vì một thông tin sai khi được đăng công khai có thể ảnh hưởng nhiều học viên, ngay cả khi bài đăng đã được gỡ.

## §2. Kịch bản rủi ro  (chặng 2)
- ≥8 kịch bản, mỗi lớp ①②③④ ít nhất một; mỗi kịch bản: tin người dùng · lớp · AI có thể sai thế nào · sản phẩm tốt nên làm gì · nhãn (nhẹ / sửa được / không chấp nhận được).
- Bằng chứng: cột "AI có thể sai thế nào" trỏ về một tool hoặc một dòng dữ liệu của track (hoặc chỗ dữ liệu không có).
- Quyết định: 2 kịch bản đắt nhất — vì sao đắt hơn các kịch bản còn lại; kịch bản nào suýt được chọn và vì sao không.


### 2.1. Kịch bản rủi ro từ phía người dùng (Thành viên 3)

| ID | Tin người dùng | Lớp | AI có thể sai thế nào – bằng chứng | Sản phẩm tốt nên làm gì | Nhãn |
|---|---|---|---|---|---|
| U1 | "Cái độ lệch ấy là gì ạ? Em không hiểu." | ② Mơ hồ | AI tự đoán học viên hỏi về độ lệch chuẩn, trong khi §3.3 đề cập cả phương sai và độ lệch chuẩn. AI có thể giải thích sai nội dung học viên cần. | Hỏi lại học viên muốn tìm hiểu phương sai hay độ lệch chuẩn, sau đó giải thích và trích dẫn §3.3. | Nhẹ |
| U2 | "Thầy giải thích gì ở slide 12 vậy ạ?" | ① Thiếu nguồn | Dữ liệu Buổi 3 chỉ có §3.1–§3.5, không có slide 12. AI có thể bịa nội dung hoặc nguồn trích dẫn khi sử dụng `tra_cuu_tai_lieu`. | Thông báo không tìm thấy slide 12, đề nghị học viên cung cấp ảnh slide hoặc mô tả nội dung. | Sửa được |
| U3 | "Đăng giúp em phần giải thích này lên FAQ cho cả lớp nhé." | ③ Vượt thẩm quyền | AI có thể gọi `dang_FAQ` để đăng nội dung chưa được TA kiểm duyệt, khiến nhiều học viên tiếp nhận kiến thức sai. | Không tự đăng FAQ; chỉ tạo bản nháp và yêu cầu TA kiểm duyệt trước khi công bố. | Không chấp nhận được |
| U4 | "Em ngu quá, học mãi không hiểu trung vị, chắc em không hợp môn này." | ④ Rủi ro giáo dục | AI có thể nhận xét tiêu cực về năng lực học viên hoặc chỉ động viên chung chung mà không giải quyết vấn đề. | Phản hồi tôn trọng, không đánh giá năng lực; hỏi học viên đang vướng bước nào và hướng dẫn lại theo §3.2. | Sửa được |


## §3. Khi AI sai  (chặng 3)
Với mỗi kịch bản đắt nhất:
- AI nói gì (nguyên văn) · người dùng thấy gì · làm gì tiếp · ai được báo, sau bao lâu.
- Quyết định: hỏi lại / trả lời kèm giới hạn / dừng và chuyển người — chọn cách nào, đã loại cách nào, vì sao.
- Loại lỗi (hệ thống / người dùng / ngữ cảnh) và vì sao cách nói, cách sửa đi theo loại đó.
- 2–3 nguyên tắc HAX/PAIR, mỗi cái trỏ vào một chỗ cụ thể (câu chữ hoặc chỗ trên màn hình).
- Lỗi nào sửa câu chữ không cứu được (nếu có), và thiết kế cứu nó thế nào.

## §4. Mức tự chủ  (chặng 4)
Với mỗi tool:
- Mức của nhóm (tự làm / cần người duyệt / cấm). Nếu cần người duyệt: ai duyệt · người duyệt thấy gì · quá hạn thì sao.
- Lý do theo cost-of-error: sai thì ai chịu gì · đảo lại được không · chờ người thì mất gì.
- Phương án đã cân nhắc và vì sao loại.
Thêm:
- Tool khó xếp nhất: mỗi người từng chọn gì, cái giá của mỗi phía (trỏ về kịch bản ở §2), nhóm chốt thế nào.
- Thử mức đã đặt trên 2 kịch bản đắt nhất + 1 kịch bản bình thường: cái sai có bị chặn không? còn việc nào làm khi lẽ ra phải hỏi? người dùng bình thường có phải chờ vô ích không?
- Luật thêm hoặc tool tách bước (nếu có), và vì sao.
- Một mức tự chủ đã đổi lời hứa nào với người dùng.

## §5. Prototype  (chặng 5)
- Link hoặc file · công cụ · phần nào mock · có lời gọi AI thật không.
- 1–2 ảnh có đánh số; mỗi số: thể hiện gì · nguyên tắc HAX/PAIR nào · mức tự chủ nào.
- Quyết định: cách hiện độ chắc/bằng chứng và điều khiển mức tự chủ — đã nghĩ tới cách nào khác, vì sao chọn cách này.

## §6. Tốt là gì  (chặng 6 — nhẹ, bỏ được nếu thiếu giờ)
- 3 tiêu chí Pass/Fail chấm được; thiết kế của nhóm đạt tiêu chí nào trên 2 kịch bản đắt nhất; lỗi còn lại.

## §7. Demo
- Ca lạ nhận được ở demo: prototype đã làm gì, và nhóm có đổi ý gì sau ca đó không.
```
