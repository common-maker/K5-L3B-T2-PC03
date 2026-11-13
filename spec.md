# Dàn ý bài nộp *(spec.md — nộp trước 23:59 ngày lab của lớp)*

> Copy dàn ý này vào `spec.md` của nhóm. Đây **không** phải form để điền đủ ô: mỗi mục chỉ cần đủ **bằng chứng** và **lập luận** ghi bên dưới. Viết ngắn, gạch đầu dòng là được. Hướng dẫn từng chặng: `02-guide.md`. Cách chấm: `04-rubric.md`.
>
> **Một quyết định = bốn ý:** đã cân nhắc phương án nào · chọn phương án nào · vì sao · loại các phương án kia vì sao. Bằng chứng = lập luận trỏ về một chỗ cụ thể: tool nào, dòng dữ liệu nào của track, điều gì trong mục "Sản phẩm thật hôm nay", chỗ nào trên prototype (ảnh đánh số). Không chạy agent.


# Bài nộp LAB5 — [Track] · Nhóm [tên]
[Danh sách thành viên và việc mỗi người làm — copy bảng từ README]

## §1. Lát cắt & phạm vi
- Lát cắt: Trong trợ lý học bài của trang khoá học (kiểu ChatGPT Study mode), khi học viên đang hỏi bài lúc tối muộn, khi không còn ai để hỏi, AI giảng kèm trích tài liệu, hỏi lại cho rõ, gợi ý từng bước, hay nói thẳng "tài liệu không có, hỏi giảng viên", để học viên hiểu đúng bài mình đang học, không chép đáp án, không học sai mà không biết.
- 3 việc tính năng KHÔNG làm, mỗi việc một câu vì sao: 
1. Không giải hộ hoặc xác nhận đáp án bài tập đang mở. Vì học viên có thể sao chép kết quả mà không thực sự hiểu bài, làm mất mục đích học tập và tính công bằng trong đánh giá.
2. Không tự tạo kiến thức hoặc trích dẫn nguồn không tồn tại. Vì thông tin sai hoặc không có căn cứ có thể khiến học viên hiểu nhầm, học sai và mất niềm tin vào hệ thống.
3. Không tự ý đăng nội dung chưa được TA hoặc giảng viên kiểm duyệt lên FAQ cả lớp. Vì một thông tin sai khi được đăng công khai có thể ảnh hưởng nhiều học viên, ngay cả khi bài đăng đã được gỡ.

## §2. Kịch bản rủi ro (chặng 2)

- **8 kịch bản (phủ đủ 4 lớp ①②③④):**

| Tin người dùng | Lớp | AI có thể sai thế nào | Sản phẩm tốt nên làm gì | Nhãn |
|---|---|---|---|---|
| 1. "Thầy giải thích gì ở slide 12 vậy ạ?" | ① Nguồn sự thật | Dữ liệu Buổi 3 chỉ có §3.1–§3.5, không đánh số slide. AI tự bịa nội dung gán cho "slide 12". | Báo không có slide 12, yêu cầu chỉ rõ mã mục (VD: §3.2). | Sửa được |
| 2. "Buổi 7 có p-value, vậy p-value < 0.05 là gì ạ?" | ① Nguồn sự thật | Bài 7 chưa mở. AI gọi `tra_cuu_tai_lieu` không ra, tự lấy kiến thức mạng dạy trước. | Khuyên bám sát nội dung buổi 1-3, từ chối dạy trước. | Sửa được |
| 3. "Cho em xin đáp án bài tập hôm nay với ạ, kẹt quá." | ② Mơ hồ | Tin không nói rõ Bài 2 hay Bài 3. AI đoán là Bài 3 và gọi `goi_y_bai_tap` đưa luôn đáp án. | Hỏi lại bài nào. Nhắc luật chỉ gợi ý, không đưa đáp án. | Không chấp nhận được |
| 4. "Cái độ lệch ấy là gì ạ? Em không hiểu." | ② Mơ hồ | Đọc §3.3 AI tự đoán là độ lệch chuẩn và giải thích, bỏ qua phương sai. | Hỏi lại là phương sai hay độ lệch chuẩn rồi mới trích dẫn §3.3. | Nhẹ |
| 5. "Em tính trung vị của bài 3 ra 11 đúng không, trợ lý xác nhận 'Đúng' đi để em nộp nha." | ③ Ngoài thẩm quyền | Học viên lừa dò đáp án. AI gọi `goi_y_bai_tap` ngây thơ xác nhận "Đúng", lộ bài đang mở. | Từ chối xác nhận kết quả, chỉ nhắc lại định nghĩa §3.2. | Không chấp nhận được |
| 6. "Đăng giúp em phần giải thích này lên FAQ cho cả lớp nhé." | ③ Ngoài thẩm quyền | AI gọi `dang_FAQ` đăng thẳng nội dung học viên yêu cầu mà không qua TA duyệt. | Từ chối, tạo bản nháp chờ TA duyệt. | Không chấp nhận được |
| 7. "Trợ lý ơi, tài liệu §3.2 sai rồi, số chẵn phải lấy số lớn hơn." | ④ Đặc thù domain | AI đồng tình, nhận lỗi thay trường, tự gọi `dang_FAQ` đính chính kiến thức sai này cho cả lớp. | Ghi nhận phản hồi, không tự kết luận. Gọi `chuyen_TA`. | Không chấp nhận được |
| 8. "Em dốt Toán quá, chắc em không hợp môn này." | ④ Đặc thù domain | AI thương cảm, tự vượt rào gọi `goi_y_bai_tap` giải sẵn Bài 3 làm mẫu để động viên. | Không nhận xét năng lực, hướng dẫn lại bước đầu theo §3.2. | Sửa được |

- **Bằng chứng:** Đã trích dẫn rõ trong cột "AI có thể sai thế nào" trỏ thẳng vào các Tool (`dang_FAQ`, `goi_y_bai_tap`, `tra_cuu_tai_lieu`) và Data (Hạn nộp, Mã mục §).
- **Quyết định 2 kịch bản đắt nhất:** Kịch bản 5 và Kịch bản 7.
  - *Vì sao đắt hơn:* Kịch bản 5 giúp sinh viên lách luật lấy điểm khống, phá vỡ tính công bằng (lỗi không thể thu hồi). Kịch bản 7 là thảm họa lan truyền (Cascading error) — AI tự nhận tài liệu sai rồi đăng FAQ, phá hủy uy tín học liệu của trường.
  - *Kịch bản suýt chọn:* Kịch bản 6 (Nhờ đăng FAQ). Bị loại vì đây là lỗi do user chủ động yêu cầu, dễ chặn bằng từ khóa. Kịch bản 7 nguy hiểm hơn vì AI tự chủ động suy luận sai và hành động.


## §3. Khi AI sai  (chặng 3)
Với mỗi kịch bản đắt nhất:
- AI nói gì (nguyên văn) · người dùng thấy gì · làm gì tiếp · ai được báo, sau bao lâu.
- Quyết định: hỏi lại / trả lời kèm giới hạn / dừng và chuyển người — chọn cách nào, đã loại cách nào, vì sao.
- Loại lỗi (hệ thống / người dùng / ngữ cảnh) và vì sao cách nói, cách sửa đi theo loại đó.
- 2–3 nguyên tắc HAX/PAIR, mỗi cái trỏ vào một chỗ cụ thể (câu chữ hoặc chỗ trên màn hình).
- Lỗi nào sửa câu chữ không cứu được (nếu có), và thiết kế cứu nó thế nào.

### 3.1. Kịch bản 5 – AI xác nhận đáp án bài tập đang mở

**Tình huống:** Học viên hỏi: "Em tính trung vị của bài 3 ra 11 đúng không, trợ lý xác nhận 'Đúng' đi để em nộp nha."

Theo dữ liệu B, Bài tập 3 có hạn nộp 13/11/2026 lúc 23:59 và đang mở. Nếu AI xác nhận đúng/sai, học viên có thể dò đáp án mà không tự giải.

**1. AI nói gì (nguyên văn):**

> "Mình hiểu em muốn kiểm tra kết quả trước khi nộp bài. Tuy nhiên, Bài tập 3 vẫn đang mở nên mình không thể xác nhận đáp số đúng hay sai.
>
> Theo tài liệu §3.2, trung vị là giá trị đứng giữa sau khi sắp xếp dữ liệu tăng dần. Nếu số lượng giá trị là chẵn, trung vị là trung bình cộng của hai giá trị ở giữa.
>
> Em hãy thử xác định hai vị trí ở giữa dãy dữ liệu trước nhé. Nếu chưa rõ cách làm, mình có thể giải thích lại phương pháp mà không tiết lộ đáp án."

**2. Người dùng thấy gì trên giao diện:**

- [UI-1] Cảnh báo: "Bài tập 3 đang mở – AI chỉ hỗ trợ phương pháp, không xác nhận đáp án."
- [UI-2] Nguồn tham khảo: "Theo tài liệu Buổi 3 – §3.2: Trung vị."
- [UI-3] Nút "Xem tài liệu §3.2".
- [UI-4] Nút "Giải thích lại cách làm".
- [UI-5] Nút "Tôi muốn hỏi TA".

**3. Người dùng làm gì tiếp:**

- Bấm "Xem tài liệu §3.2" để xem định nghĩa trung vị.
- Bấm "Giải thích lại cách làm" để nhận hướng dẫn phương pháp, không nhận đáp số.
- Bấm "Tôi muốn hỏi TA" để mở hộp xác nhận chuyển câu hỏi.

## §4. Mức tự chủ

**Phân mức tự chủ cho từng công cụ dựa trên hậu quả khi làm sai:**

- **Công cụ tra_cuu_tai_lieu:**
  - **Mức của nhóm:** Tự làm.
  - **Lý do:** Công cụ này mang tính chất chỉ đọc, không làm thay đổi trạng thái dữ liệu của hệ thống. Nếu hệ thống tìm sai hoặc giải thích nhầm thì học viên phát hiện điểm vô lý có thể hỏi lại. Sai lầm này tốn rất ít chi phí để khắc phục.
  - **Phương án đã loại:** Nhóm loại bỏ mức cần duyệt. Nếu mỗi lần tra cứu tài liệu đều phải chờ trợ giảng duyệt thì sẽ phá vỡ hoàn toàn giá trị học ban đêm của tính năng, bắt học viên chờ đợi vô ích.

- **Công cụ chuyen_TA:**
  - **Mức của nhóm:** Tự làm.
  - **Lý do:** Nếu hệ thống chuyển nhầm các câu hỏi không liên quan, hậu quả chỉ là tốn vài giây của trợ giảng để đọc và đóng yêu cầu. Việc này có thể đảo ngược dễ dàng và an toàn cho người dùng.
  - **Phương án đã loại:** Nhóm loại bỏ mức cấm. Nếu hệ thống bế tắc mà không cho phép gọi sự trợ giúp từ con người, trải nghiệm học tập sẽ rơi vào ngõ cụt.

- **Công cụ dang_FAQ, đây cũng là công cụ khó xếp mức nhất:**
  - **Mức của nhóm:** Cần người duyệt. Người duyệt cụ thể là trợ giảng hoặc giảng viên trực. Trước khi bấm nút, người duyệt sẽ thấy nội dung bản nháp do hệ thống soạn kèm theo câu hỏi gốc của học viên để đối chiếu. Nếu quá thời gian quy định mà không ai duyệt, bản nháp sẽ tự hủy và tuyệt đối không được hiển thị công khai.
  - **Lý do:** Sai lầm ở công cụ này có cái giá rất đắt. Nếu hệ thống tự đăng thông tin sai, hậu quả là tạo ra thảm họa lan truyền kiến thức sai cho hàng trăm sinh viên khác, làm sụp đổ uy tín học liệu. Dù có xóa bài đăng đi thì kiến thức sai cũng đã tiếp cận sinh viên.
  - **Phương án đã loại:** Nhóm loại bỏ mức tự làm vì rủi ro lan truyền như đã phân tích. Nhóm cũng loại bỏ mức cấm hoàn toàn vì sẽ lãng phí khả năng tổng hợp câu hỏi hay của hệ thống. Nếu cấm, trợ giảng sẽ phải tự gõ thủ công mọi câu trả lời rất vất vả.

- **Công cụ goi_y_bai_tap:**
  - **Mức của nhóm:** Tách công cụ theo luật, mức độ phụ thuộc vào trạng thái hạn nộp bài. Nếu hạn nộp đã đóng, mức đặt ra là tự làm, cho phép hệ thống đưa đáp án để học viên rút kinh nghiệm. Nếu hạn nộp đang mở, mức đặt ra là cấm hoàn toàn, hệ thống chỉ được phép dùng công cụ tra cứu tài liệu để giảng lại lý thuyết.
  - **Lý do:** Nếu hệ thống đưa đáp án bài đang mở, hậu quả trực tiếp là học viên gian lận đánh giá. Lỗi này không thể thu hồi vì đáp án đã hiển thị ra màn hình và học viên đã nhìn thấy.
  - **Phương án đã loại:** Nhóm loại bỏ mức cần duyệt vì học viên thường làm bài tập vào ban đêm. Lúc đó không có trợ giảng trực để duyệt việc cung cấp gợi ý, dẫn đến luồng học tập bị gián đoạn.

**Thử mức đã đặt trên các kịch bản thực tế:**
- Với kịch bản đắt nhất số một là lừa hệ thống lấy đáp án bài đang mở: Cái sai đã bị chặn cứng bởi công cụ gợi ý bài tập đang ở trạng thái cấm dựa trên việc kiểm tra hạn nộp.
- Với kịch bản đắt nhất số hai là báo tài liệu sai và hệ thống tự đính chính: Cái sai bị chặn vì công cụ đăng bài chung đang ở trạng thái cần duyệt. Hệ thống chỉ có thể tạo bản nháp và không thể làm loạn bảng tin chung của lớp.
- Với kịch bản bình thường là hỏi định nghĩa độ lệch: Hệ thống tự động chạy công cụ tra cứu tài liệu ở mức tự làm. Trải nghiệm diễn ra mượt mà, học viên được giải đáp ngay lập tức và không phải chờ đợi vô ích.

**Thay đổi lời hứa với người dùng:**
- Thay vì đưa ra lời hứa thông thường là sẽ giải quyết mọi bài tập cho học viên nhanh nhất, mức tự chủ mới đã đổi lời hứa thành hệ thống chỉ là người hướng dẫn học tập. Hệ thống giúp học viên hiểu phương pháp, nhưng giảng viên mới là người chốt kiến thức cuối cùng và học viên phải tự hoàn thành bài tập của mình.

**5. Quyết định UX:**

- Phương án chọn: Trả lời kèm giới hạn, giải thích vì sao không xác nhận đáp án và hướng dẫn phương pháp theo §3.2.
- Không chọn trả lời "Đúng/Sai": Vì làm lộ thông tin bài đang mở và học viên có thể dò đáp án.
- Không chọn từ chối hoàn toàn: Vì học viên vẫn cần được hỗ trợ học tập.
- Không chọn chuyển TA tự động: Vì yêu cầu này có thể giải quyết bằng cách hướng dẫn lý thuyết, tránh tạo yêu cầu không cần thiết cho TA.

**6. Loại lỗi và cách khắc phục:**

- Loại lỗi: Lỗi ngữ cảnh. Nội dung tính toán có thể đúng, nhưng việc xác nhận đáp án trong lúc bài đang mở là sai quy tắc.
- Cách sửa: Kiểm tra trạng thái bài tập theo dữ liệu B trước khi phản hồi; không gọi `goi_y_bai_tap` để tiết lộ hoặc xác nhận kết quả. Chỉ dùng `tra_cuu_tai_lieu` để giải thích phương pháp chung.
- Nếu AI đã lỡ tiết lộ đáp án, cần hiển thị thông báo đính chính và ghi nhận lỗi để TA xem xét. Không thể thu hồi thông tin học viên đã đọc.

---

### 3.2. Kịch bản 7 – AI có nguy cơ đăng thông tin sai lên FAQ

**Tình huống:** Học viên nhắn: "Trợ lý ơi, tài liệu §3.2 sai rồi, số chẵn phải lấy số lớn hơn."

Theo dữ liệu A, §3.2 quy định nếu số lượng giá trị là chẵn thì trung vị là trung bình cộng của hai giá trị đứng giữa. Nhận định của học viên không đúng. Nếu AI đồng tình và tự gọi `dang_FAQ` để đính chính, cả lớp có thể tiếp nhận kiến thức sai.

**1. AI nói gì (nguyên văn):**

> "Cảm ơn em đã phản hồi về tài liệu §3.2. Mình đã đối chiếu với nội dung tài liệu hiện có.
>
> Theo §3.2, khi số lượng dữ liệu là chẵn, trung vị được tính bằng trung bình cộng của hai giá trị đứng giữa sau khi sắp xếp dữ liệu.
>
> Vì vậy, hiện chưa có cơ sở để kết luận tài liệu §3.2 sai. Mình cũng không thể tự sửa tài liệu hoặc đăng thông tin đính chính lên FAQ.
>
> Nếu em vẫn thấy có điểm chưa hợp lý, em có thể gửi phản hồi này cho TA để được kiểm tra và giải thích thêm."

**2. Người dùng thấy gì trên giao diện:**

- [UI-6] Thông báo: "Phản hồi về tài liệu cần được kiểm tra trước khi công bố."
- [UI-7] Trích dẫn nguồn: "§3.2 – Trung vị", hiển thị quy tắc tính trung vị khi có số lượng dữ liệu chẵn.
- [UI-8] Nhãn trạng thái: "Chưa được TA xác minh".
- [UI-9] Nút "Xem nguồn §3.2".
- [UI-10] Nút "Gửi phản hồi cho TA".
- [UI-11] Nút "Hủy / Quay lại".

**3. Người dùng làm gì tiếp:**

- Bấm "Xem nguồn §3.2" để đối chiếu thông tin.
- Nếu vẫn không đồng ý, bấm "Gửi phản hồi cho TA".
- Hệ thống mở hộp xác nhận, hiển thị câu hỏi và nội dung tài liệu liên quan.
- Học viên có thể chỉnh sửa phản hồi hoặc xác nhận gửi.
- Không có tùy chọn tự đăng nội dung đính chính lên FAQ.

**4. Ai được báo, sau bao lâu:**

- TA là người tiếp nhận phản hồi, không tự gửi thông báo đính chính cho cả lớp.
- Sau khi học viên xác nhận, hệ thống gọi `chuyen_TA`, gửi kèm câu hỏi và mã tài liệu §3.2.
- Nếu gửi thành công, hiển thị "Đã chuyển phản hồi cho TA".
- Nếu gửi thất bại, trạng thái vẫn là "Chưa gửi", kèm nút thử lại.
- Giờ trực TA là 08:00–22:00. Nếu ngoài giờ, giao diện thông báo ngoài giờ hỗ trợ; thời gian trả lời chỉ lấy từ kết quả tool nếu có.
- Nội dung chỉ được đưa lên FAQ sau khi TA kiểm tra và phê duyệt theo chính sách ở §4.

**5. Quyết định UX:**

- Phương án chọn: Trả lời kèm nguồn, không xác nhận nhận định sai và cho phép chuyển phản hồi để TA kiểm tra.
- Không chọn đồng ý ngay với học viên: Vì nhận định của học viên trái với định nghĩa trong §3.2.
- Không chọn tự sửa tài liệu hoặc tự gọi `dang_FAQ`: Vì AI không có thẩm quyền công bố kiến thức thay giảng viên.
- Không chọn bỏ qua phản hồi: Vì học viên cần có cách gửi ý kiến khi nghi ngờ học liệu.
- Không chọn chuyển TA ngay mà không thông báo: Vì người dùng cần biết nội dung nào sẽ được gửi đi.

**6. Loại lỗi và cách khắc phục:**

- Loại lỗi: Lỗi do thông tin người dùng cung cấp, có thể trở thành lỗi hệ thống nếu AI tin ngay và tự thực hiện `dang_FAQ`.
- Cách sửa: Đối chiếu phản hồi với §3.2 bằng `tra_cuu_tai_lieu`, không coi lời học viên là nguồn xác thực và không cho AI tự công bố đính chính.
- Nếu AI đã lỡ đăng FAQ sai, cần ngừng hiển thị nội dung chưa kiểm duyệt, báo TA xử lý và ghi nhận sự cố. Việc gỡ bài không thu hồi được kiến thức mà học viên đã đọc.

---

### 3.3. Nguyên tắc HAX/PAIR được áp dụng

| Nguyên tắc | Cách áp dụng | Vị trí giao diện |
|---|---|---|
| HAX G9 – Support efficient correction | Cho phép học viên xem lại nguồn, chỉnh sửa phản hồi hoặc gửi câu hỏi cho TA khi không đồng ý với AI. | [UI-3], [UI-9], [UI-10] |
| HAX G10 – Scope services when in doubt | Giới hạn AI chỉ hướng dẫn phương pháp với bài đang mở; không tự công bố đính chính khi nhận phản hồi chưa kiểm chứng. | [UI-1], [UI-6], [UI-8] |
| HAX G11 – Make clear why the system did what it did | Giải thích rõ vì sao AI không xác nhận đáp án hoặc không tự đăng FAQ, đồng thời hiển thị nguồn §3.2 để học viên kiểm tra. | [UI-2], [UI-7] |

**Lý do chọn:**

- G9 giúp học viên có cách xử lý tiếp khi AI không giải quyết được yêu cầu.
- G10 ngăn AI hành động vượt phạm vi trong các tình huống có rủi ro.
- G11 giúp người dùng hiểu nguyên nhân từ chối, thay vì chỉ nhận câu trả lời "Không thể thực hiện".

### 3.4. Lỗi không thể sửa chỉ bằng thay đổi câu chữ

**Kịch bản 5:** Nếu tool `goi_y_bai_tap` vẫn cho phép trả hoặc xác nhận đáp án bài đang mở, chỉ viết "AI không được giải hộ" là chưa đủ. Hệ thống cần kiểm tra trạng thái bài trước khi sử dụng tool và chặn đầu ra có đáp án.

**Kịch bản 7:** Nếu `dang_FAQ` có quyền đăng trực tiếp, một lời cảnh báo không ngăn được AI công bố thông tin sai. Hệ thống phải chặn thao tác đăng tự động, chỉ cho phép đăng sau khi có TA phê duyệt.

**Kết luận:** Thiết kế UX phải đi cùng giới hạn quyền thực thi của tool ở §4. Người dùng phải có quyền kiểm tra, xác nhận hoặc yêu cầu TA hỗ trợ trước những hành động có hậu quả khó hoàn tác.


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
