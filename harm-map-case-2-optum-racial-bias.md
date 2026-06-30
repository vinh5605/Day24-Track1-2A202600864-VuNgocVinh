# Harm Map Worksheet — Case 2: Thuật toán Optum phân biệt chủng tộc

| Trường | Nội dung |
|---|---|
| **High-risk moment** | Thời điểm thuật toán chấm điểm rủi ro để quyết định bệnh nhân nào được đưa vào chương trình "high-risk care management" (thêm nguồn lực chăm sóc, theo dõi chủ động) |
| **Stakeholder bị ảnh hưởng** | Bệnh nhân da đen (Black patients) bị đánh giá thấp hơn thực tế mức độ bệnh |
| **Failure mode** | **Bias / fairness** — thuật toán dùng proxy variable (chi phí y tế quá khứ) vốn đã phản ánh bất bình đẳng tiếp cận y tế có sẵn, khiến mô hình khuếch đại bất công thay vì đo đúng nhu cầu sức khỏe |
| **Layer bắt đầu lỗi** | **Model** (lựa chọn label/biến mục tiêu "chi phí y tế" làm proxy cho "nhu cầu sức khỏe" là lỗi thiết kế gốc ngay từ khâu chọn dữ liệu huấn luyện, không phải lỗi vận hành phát sinh sau) |
| **Harm xảy ra là gì?** | Bệnh nhân da đen bị loại khỏi chương trình chăm sóc chủ động dù bệnh nặng tương đương hoặc nặng hơn bệnh nhân da trắng được chọn, dẫn tới chậm can thiệp y tế và duy trì/khuếch đại bất bình đẳng y tế theo chủng tộc |
| **Harm lens** | **Opportunity loss** (chính — mất cơ hội được chăm sóc chủ động) kèm **Injury** (gián tiếp, do bệnh không được quản lý sớm) và **Dignity loss** (bị hệ thống đánh giá thấp một cách hệ thống theo chủng tộc) |
| **Severity** | **Critical** — bias khiến tỉ lệ bệnh nhân da đen được chọn vào chương trình chỉ ở mức 17,7% thay vì mức công bằng 46,5%, ảnh hưởng trực tiếp đến việc quản lý bệnh mãn tính lâu dài |
| **Scale** | **High** — thuật toán dạng này được dùng để quản lý chăm sóc cho hơn 200 triệu người mỗi năm tại Mỹ |
| **Probability** | **High** — bias mang tính hệ thống (systemic), xảy ra với mọi bệnh nhân da đen đủ điều kiện được chấm điểm, không phải lỗi ngẫu nhiên hiếm gặp |
| **Frequency** | **High** — thuật toán chạy liên tục theo chu kỳ chấm điểm định kỳ, mỗi lần chạy lại tái tạo cùng một dạng bias |
| **Vì sao?** | Vì bias bắt nguồn từ lựa chọn proxy variable mang tính cấu trúc (chi phí y tế phản ánh khả năng/quyền tiếp cận hơn là tình trạng bệnh thực), nên đây không phải lỗi ngẫu nhiên mà là lỗi lặp lại có hệ thống, ở quy mô dân số rất lớn — đúng như nghiên cứu đã định lượng (17,7% so với mức công bằng 46,5%) |
