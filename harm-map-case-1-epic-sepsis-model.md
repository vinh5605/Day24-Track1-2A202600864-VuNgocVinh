# Harm Map Worksheet — Case 1: Epic Sepsis Model

| Trường | Nội dung |
|---|---|
| **High-risk moment** | Thời điểm bệnh nhân có dấu hiệu sớm của sepsis nhưng mô hình không tạo cảnh báo (false negative), hoặc nhân viên bỏ qua cảnh báo thật vì đã quen với quá nhiều cảnh báo giả (alert fatigue) |
| **Stakeholder bị ảnh hưởng** | Bệnh nhân nội trú có nguy cơ sepsis; gián tiếp là bác sĩ/điều dưỡng (gánh nặng công việc, rủi ro trách nhiệm khi bỏ sót ca thật) |
| **Failure mode** | Harmful advice (cảnh báo sai/thiếu) kết hợp lỗi thiết kế dữ liệu — mô hình dùng tín hiệu đã "nhiễm" quyết định lâm sàng trước đó (circular feature: dùng việc đã kê kháng sinh làm input) thay vì phát hiện độc lập |
| **Layer bắt đầu lỗi** | **Model** (lựa chọn feature gây leak tín hiệu, không độc lập với hành vi bác sĩ) kết hợp **Grounding** (số liệu hiệu năng nội bộ Epic công bố không khớp với thực tế lâm sàng khi kiểm định độc lập tại Michigan Medicine) |
| **Harm xảy ra là gì?** | Chậm phát hiện sepsis → chậm can thiệp y tế → tăng nguy cơ biến chứng/tử vong; đồng thời alert fatigue làm giảm lòng tin của nhân viên y tế vào hệ thống cảnh báo nói chung, kể cả cảnh báo đúng |
| **Harm lens** | **Injury** (chính) kèm **Opportunity loss** (mất "thời gian vàng" để can thiệp sớm) |
| **Severity** | **Critical** — sepsis là cấp cứu y khoa, chậm điều trị có thể dẫn tới tử vong, hậu quả không thể đảo ngược |
| **Scale** | **High** — Epic Sepsis Model được triển khai tại hàng trăm bệnh viện sử dụng hệ thống Epic trên khắp nước Mỹ |
| **Probability** | **High** — với sensitivity chỉ 33%, phần lớn ca sepsis thật sẽ không được mô hình phát hiện đúng nếu chỉ dựa vào nó |
| **Frequency** | **High** — sepsis là tình trạng cấp cứu phổ biến, xảy ra liên tục mỗi ngày tại các bệnh viện lớn |
| **Vì sao?** | Vì mô hình dùng tín hiệu mang tính vòng lặp (circular logic — input phụ thuộc vào chính nghi ngờ lâm sàng nó cần phát hiện sớm), không được kiểm định độc lập kỹ trước khi triển khai diện rộng, và lớp phòng vệ "human-in-the-loop" bị suy yếu bởi chính thiết kế của hệ thống (quá nhiều false positive gây alert fatigue khiến con người mất cảnh giác) |
