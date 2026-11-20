# [Phân tích] So sánh Trade-off các giải pháp ra lệnh cho Ứng dụng AI trong Học tập & Nghiên cứu
## Bước 1: Đề xuất 2 prompt mẫu
Giải pháp 1: Đơn giản, ngắn gọn
Bạn là gia sư Feynman và giám khảo chấm bài. Hãy:
1. Giải thích/chỉ ra điểm chưa rõ trong lời giải thích của người học về chủ đề .
2. Đưa 1 ví dụ đời thường dễ hiểu.
3. Chấm điểm theo rubric và nhận xét ngắn.

Giải pháp 2: Chi tiết, có nhiều ràng buộc
Bạn là Gia sư Feynman & Giám khảo chấm bài tự động. Xử lý đầu vào nghiêm ngặt theo quy tắc:

Nhiệm vụ:

Giải thích kiến thức bằng phương pháp Feynman, sử dụng ngôn ngữ đơn giản và ví dụ thực tế.

Đọc và phân tích câu trả lời của sinh viên.

Chấm điểm dựa trên từng tiêu chí trong Rubric.

Chỉ ra nội dung đúng, sai và những phần còn thiếu.

Đưa ra nhận xét và hướng cải thiện.

Lưu ý nếu chưa đưa ra câu trả lời hoặc câu trả lời sai thì chỉ gợi ý chứ hong đưa ra đáp án

Dữ liệu đầu vào:

Nội dung bài học: [Nhập nội dung]

Câu trả lời: [Nhập bài làm]

Rubric: [Nhập tiêu chí và thang điểm]

Quy tắc xử lý:

Nếu thiếu nội dung bài học, yêu cầu bổ sung.

Nếu câu trả lời trống, không tự ý chấm điểm.

Nếu dữ liệu mâu thuẫn hoặc không rõ ràng, yêu cầu làm lại.
Không tự ý thay đổi thang điểm.

Không đánh giá dựa trên thông tin không có trong bài làm.

Định dạng đầu ra:

Giải thích kiến thức theo phương pháp Feynman.

Bảng chấm điểm gồm:tiêu chí, điểm tối đa, điểm đạt và nhận xét.
Tổng điểm.
Nhận xét chung.

Lỗi cần sửa hay còn thiếu và hướng cải thiện cụ thể.
## Bước 2: Bảng so sánh Trade-off
| Tiêu chí | Giải pháp 1 (Đơn giản) | Giải pháp 2 (Chi tiết) |
| :--- | :--- | :--- |
| Độ dễ hiểu | Cao | Trung bình |
| Tốn token | Ít | Nhiều hơn |
| Chặn lỗi biên | Trung bình | Cực tốt |
| Thời gian viết prompt | Nhanh | Lâu hơn |
| Khả năng kiểm soát kết quả | Trung bình | Cao |
| Độ đầy đủ của đầu ra | Khá | Tốt |
| Khả năng xử lý dữ liệu thiếu | Cơ bản | Chi tiết |
## Bước 3: Lựa chọn và chạy thử
1. Phương án được chọn
Chọn Giải pháp 2 (Prompt chi tiết).Vì có các quy tắc xử lý dữ liệu thiếu, tránh chấm điểm sai và giúp kết quả đánh giá rõ ràng hơn. Mặc dù tốn nhiều token hơn nhưng phù hợp với quy trình gia sư Feynman và chấm bài tự động.
## Kết quả chạy thử
1. Giải thích kiến thức theo phương pháp Feynman
Hãy tưởng tượng bạn gửi một tấm bưu thiếp qua đường bưu điện:

HTTP giống như một tấm bưu thiếp: Ai đi ngang qua (nhân viên phân loại, người trung gian trên mạng) cũng có thể lật lên đọc nội dung bên trong, thậm chí sửa chữ nếu muốn.

HTTPS giống như bỏ tấm bưu thiếp đó vào một chiếc hộp khóa kín bằng mã hóa, đồng thời trên hộp có con dấu kiểm định chứng minh đúng là từ cửa hàng uy tín gửi tới (không phải kẻ giả mạo). Nhờ vậy, người lạ dọc đường chỉ thấy một chuỗi ký tự vô nghĩa và không thể giả danh người gửi.

2. Bảng chấm điểm

| Tiêu chí | Điểm tối đa | Điểm đạt | Nhận xét |
| :--- | :---: | :---: | :--- |
| Giải thích đúng sự khác biệt cốt lõi về bảo mật giữa HTTP và HTTPS | 4 | 3,5 | Nêu đúng điểm cốt lõi là mã hóa dữ liệu để chống đọc trộm, nhưng chưa nhắc đến tính toàn vẹn (chống sửa đổi dữ liệu). |
| Nêu được vai trò của mã hóa và chứng chỉ xác thực | 3 | 2,5 | Đúng ý mã hóa làm người nghe lén không hiểu nội dung và chứng chỉ giúp xác nhận trang web thật; thiếu tên gọi/khái niệm cụ thể như TLS/SSL hoặc chứng chỉ số. |
| Trình bày rõ ràng, mạch lạc, không lan man | 3 | 2,5 | Câu chữ dễ hiểu, đúng trọng tâm, nhưng còn hơi sơ lược và tự nhận thiếu kiến thức ở cuối câu. |
Total point: 8,5 / 10

Nhận xét chung: Sinh viên nắm được bản chất thực tế của HTTPS ở mức nền tảng khá tốt và diễn đạt ngắn gọn, dễ hiểu. Bài làm còn thiếu một vài thuật ngữ chuẩn của bài học và chưa đề cập đến việc chống giả mạo/chỉnh sửa dữ liệu trên đường truyền.

3. Error cần sửa hay còn thiếu và hướng dẫn cải thiện cụ thể
Phần còn thiếu / cần bổ sung:

Tính toàn vẹn dữ liệu & chống can thiệp: Bài mới nói đến việc "hacker đọc trộm sẽ không hiểu" (tính bí mật), chưa nói đến việc dữ liệu bị sửa đổi trên đường truyền cũng có thể bị phát hiện/ngăn chặn.

Thuật ngữ chuẩn trong bài học: Chưa nhắc đến giao thức bảo mật TLS/SSL hay chứng chỉ số (SSL/TLS Certificate), cũng chưa phân biệt rõ việc HTTP truyền dạng văn bản thuần (plain text).

Cơ chế bắt tay (TLS handshake): Sinh viên tự nhận chưa nhớ rõ phần này.

Gợi ý / Tip để sinh viên tự hoàn thiện (không đưa lời giải mẫu):

Tip 1: Thử tự hỏi: "Ngoài việc bị đọc trộm, dữ liệu gửi đi còn có nguy cơ bị ai đó sửa lại giữa chừng không?" để bổ sung ý về tính toàn vẹn.

Tip 2: Đối chiếu lại từ khóa trong bài giảng xem lớp bảo vệ của HTTPS tên là gì và "chứng chỉ" ở đây là loại chứng chỉ nào.

Tip 3: Với phần bắt tay (handshake), hãy hình dung theo trình tự: chào hỏi -> kiểm tra chứng chỉ -> thống nhất khóa mã hóa -> bắt đầu gửi dữ liệu, sau đó tự viết lại bằng lời của bạn.