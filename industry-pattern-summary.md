# Tổng hợp pattern rủi ro của ngành Y tế

Dựa trên 3 case (Epic Sepsis Model, thuật toán Optum, UnitedHealth nH Predict), pattern rủi ro chung của ngành Y tế / health AI là:

1. **Failure mode chủ đạo không phải hallucination kiểu chatbot, mà là lỗi thiết kế model/data** — proxy variable sai (Optum dùng chi phí thay cho nhu cầu sức khỏe), feature bị "nhiễm" tín hiệu vòng lặp (Epic dùng việc đã kê kháng sinh để dự đoán sepsis), hoặc AI ghi đè quyết định con người mà thiếu cơ chế kiểm soát thực chất (nH Predict). Đây là các hệ thống predictive/scoring/quyết định, không phải generative, nên failure mode khác hẳn nhóm "AI tutor" hay "content creator".
2. **Layer lỗi thường bắt đầu từ Model/Data** (lựa chọn feature, lựa chọn label mục tiêu) chứ không phải UX, nhưng hậu quả bị khuếch đại khi lớp **Safety/human-in-the-loop bị suy yếu** — alert fatigue (case 1), hoặc áp lực KPI ép nhân viên bám sát AI thay vì đánh giá lâm sàng độc lập (case 3).
3. **Severity luôn ở mức Critical** trong cả 3 case vì AI đụng tới an toàn thể chất (sepsis, ngừng chăm sóc) hoặc quyết định hệ trọng ảnh hưởng sức khỏe lâu dài (loại khỏi chương trình chăm sóc chủ động).
4. **Scale rất lớn vì các hệ thống này là platform dùng chung** — Epic triển khai tại hàng trăm bệnh viện, thuật toán kiểu Optum quản lý chăm sóc cho hơn 200 triệu người/năm, UnitedHealth là hãng bảo hiểm Medicare Advantage lớn nhất Mỹ. Một lỗi thiết kế gốc duy nhất nhân rộng thành harm ở quy mô dân số, khác với lỗi cục bộ chỉ ảnh hưởng một vài người dùng.
5. **Lỗi khó phát hiện sớm vì "vẻ ngoài khách quan" của thuật toán** — cả 3 case chỉ bị phơi bày nhờ (a) nghiên cứu kiểm định độc lập bên ngoài công ty phát triển (Michigan Medicine, Obermeyer et al.), hoặc (b) điều tra báo chí kết hợp kiện tụng (STAT News + đơn kiện liên bang). Bản thân các tổ chức vận hành hệ thống không tự công bố các sai sót này.

## Nếu là team sản phẩm, sẽ sửa gì trước?

1. Bắt buộc **external validation** (kiểm định độc lập, ngoài đội phát triển) trước khi đưa vào production và định kỳ sau khi triển khai.
2. Rà soát và loại bỏ **proxy variable mang tính cấu trúc bất công** (vd. dùng chi phí làm đại diện cho nhu cầu sức khỏe) — kiểm tra fairness theo nhóm nhân khẩu học trước khi ship.
3. Tách bạch rõ vai trò "AI gợi ý" và "AI quyết định" — giữ quyền veto thực chất cho con người, không đặt KPI/incentive nội bộ ép nhân viên bám sát kết quả AI thay vì đánh giá chuyên môn độc lập.
