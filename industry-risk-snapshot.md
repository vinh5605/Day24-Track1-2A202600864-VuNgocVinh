# Industry Risk Snapshot — Y tế / Health AI (symptom checker, clinical decision support, care management)

| Câu hỏi | Mức độ | Vì sao? |
|---|---|---|
| Nếu AI sai, có thể gây hại thể chất không? | **Critical** | AI y tế tham gia trực tiếp vào chuỗi quyết định lâm sàng (phát hiện sepsis, xác định mức độ rủi ro, quyết định tiếp tục/dừng chăm sóc). Sai sót có thể dẫn tới chậm điều trị, biến chứng, hoặc tử vong. |
| AI có ảnh hưởng đến quyết định hệ trọng không? | **Critical** | AI ảnh hưởng tới các quyết định như: có cảnh báo sepsis hay không, bệnh nhân có được đưa vào chương trình chăm sóc chủ động hay không, bảo hiểm có tiếp tục chi trả phục hồi chức năng hay không — đều là quyết định hệ trọng đến sức khỏe và tài chính của bệnh nhân. |
| Hệ thống có động tới dữ liệu nhạy cảm không? | **High** | Toàn bộ các hệ thống này xử lý dữ liệu hồ sơ bệnh án điện tử (EHR), lịch sử chẩn đoán, chi phí điều trị — đều là protected health information (PHI). |
| Nếu sai, hậu quả có khó đảo ngược không? | **Critical** | Chậm phát hiện sepsis hoặc ngừng chăm sóc phục hồi sớm có thể gây tổn thương không thể hồi phục (biến chứng, tử vong); việc bị loại khỏi chương trình chăm sóc chủ động trong quá khứ cũng không thể "hoàn tác" lại sức khỏe đã mất. |
| Nếu triển khai rộng, blast radius có lớn không? | **Critical** | Các hệ thống này được bán dưới dạng platform dùng chung: Epic triển khai tại hàng trăm bệnh viện Mỹ; thuật toán kiểu Optum được dùng để quản lý chăm sóc cho hơn 200 triệu người/năm tại Mỹ; UnitedHealth là hãng bảo hiểm Medicare Advantage lớn nhất nước. Một lỗi thiết kế gốc nhân rộng thành harm ở quy mô dân số. |
| Có cần human review hoặc escalation không? | **Critical** | Bắt buộc phải có bác sĩ/y tá xác nhận trước khi hành động dựa trên gợi ý của AI. Tuy nhiên thực tế cho thấy cơ chế này dễ bị suy yếu (alert fatigue, áp lực KPI buộc nhân viên bám sát dự đoán AI). |
| **Risk profile tổng thể của ngành** | **Critical** | Y tế hội tụ đủ cả 6 yếu tố ở mức cao nhất: ảnh hưởng thể chất trực tiếp, quyết định hệ trọng, dữ liệu nhạy cảm, hậu quả khó đảo ngược, blast radius lớn, và cần human review nghiêm ngặt. Đây là một trong những ngành có risk profile cao nhất trong số 6 ngành của bài lab. |

## Gợi ý theo ngành (tham khảo từ đề bài)

Y tế / symptom checker / health assistant: **injury, harmful advice, delayed intervention, dữ liệu sức khỏe** — đúng với cả 3 case được phân tích trong repo này (xem [industry-pattern-summary.md](industry-pattern-summary.md)).
