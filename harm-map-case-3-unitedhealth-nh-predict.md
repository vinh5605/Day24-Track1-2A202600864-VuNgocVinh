# Harm Map Worksheet — Case 3: UnitedHealth nH Predict

| Trường | Nội dung |
|---|---|
| **High-risk moment** | Thời điểm AI dự đoán "ngày xuất viện lý tưởng" được dùng làm căn cứ để ngừng chi trả bảo hiểm cho chăm sóc phục hồi chức năng, bất kể đánh giá lâm sàng thực tế của bác sĩ điều trị |
| **Stakeholder bị ảnh hưởng** | Bệnh nhân cao tuổi (Medicare Advantage) đang cần phục hồi chức năng tại cơ sở điều dưỡng chuyên môn; gia đình bệnh nhân |
| **Failure mode** | **Escalation failure** (AI ghi đè quyết định của bác sĩ mà không có cơ chế human review thực chất; nhân viên bị gây áp lực bám sát dự đoán AI trong phạm vi 1%) kết hợp **Harmful advice** (khuyến nghị ngừng chăm sóc không phù hợp với tình trạng thực tế của bệnh nhân) |
| **Layer bắt đầu lỗi** | **Safety** (thiếu cơ chế human-in-the-loop đủ mạnh để override AI một cách thực chất) kết hợp yếu tố tổ chức/UX quy trình (incentive nội bộ ép nhân viên tuân theo AI thay vì đánh giá lâm sàng độc lập) |
| **Harm xảy ra là gì?** | Bệnh nhân bị cắt bảo hiểm chăm sóc phục hồi chức năng sớm hơn nhu cầu y tế thực tế, dẫn tới nguy cơ tái nhập viện, biến chứng, hoặc phải tự chi trả chi phí lớn |
| **Harm lens** | **Injury** (nguy cơ sức khỏe do ngừng chăm sóc sớm) kèm **Opportunity loss** (mất quyền lợi bảo hiểm đã đóng phí) |
| **Severity** | **Critical** — ngừng chăm sóc phục hồi chức năng sớm với người cao tuổi có thể dẫn tới biến chứng nghiêm trọng, khó hồi phục, thậm chí tử vong |
| **Scale** | **High** — UnitedHealth là hãng bảo hiểm Medicare Advantage lớn nhất Mỹ; nH Predict dựa trên dữ liệu ~6 triệu bệnh nhân, ảnh hưởng số lượng lớn người tham gia bảo hiểm hậu cấp tính |
| **Probability** | **High (theo cáo buộc, chưa được tòa xác nhận)** — đơn kiện cáo buộc tỉ lệ sai lên tới ~90% trong các đơn kháng cáo, tỉ lệ từ chối hậu cấp tính tăng gần gấp 3 lần (8,7% → 22,7%) |
| **Frequency** | **Medium/High** — lặp lại với mỗi chu kỳ đánh giá tiếp tục chi trả bảo hiểm cho bệnh nhân tại cơ sở điều dưỡng chuyên môn, nhưng chỉ ảnh hưởng nhóm bệnh nhân cần chăm sóc hậu cấp tính kéo dài (không phải toàn bộ dân số bảo hiểm) |
| **Vì sao?** | Vì đây là cáo buộc trong vụ kiện đang tố tụng (chưa có phán quyết cuối cùng), nhưng được củng cố bởi điều tra báo chí độc lập (STAT News) dựa trên tài liệu nội bộ và lời khai cựu nhân viên — cho thấy probability/frequency cao có cơ sở thực tế dù chưa phải sự thật được tòa xác nhận chính thức |
