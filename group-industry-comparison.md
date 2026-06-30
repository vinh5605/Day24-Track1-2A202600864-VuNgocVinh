# File tổng hợp nhóm — So sánh risk profile giữa các ngành

> **Hướng dẫn:** File này cần được hoàn thiện sau Bước 5–6 của bài lab (share case với cả bàn). Hàng "Y tế / symptom checker / health assistant" bên dưới đã được điền sẵn dựa trên phân tích 3 case cá nhân trong repo này. Các hàng khác cần điền dựa trên case thật mà từng thành viên trong bàn đã trình bày — **không tự suy đoán hộ ngành mà mình không nghiên cứu**.

## Bảng so sánh các ngành

| Ngành | Harm dễ gặp nhất | Failure mode hay lặp lại | Layer hay bắt đầu lỗi | Risk profile tổng thể | Vì sao? |
|---|---|---|---|---|---|
| HR / tuyển dụng | *(điền sau khi nghe case từ thành viên phụ trách ngành này)* | | | | |
| Giáo dục / AI tutor | | | | | |
| **Y tế / symptom checker / health assistant** | **Injury, Opportunity loss** (chậm can thiệp, mất cơ hội chăm sóc do bias/lỗi model) | **Lỗi thiết kế model/data** (proxy variable sai, feature nhiễm tín hiệu vòng lặp) + **Escalation failure** (AI ghi đè quyết định con người) | **Model/Data**, khuếch đại bởi **Safety** (human-in-the-loop bị suy yếu) | **Critical** | AI tham gia trực tiếp vào quyết định ảnh hưởng tính mạng/sức khỏe, dùng dữ liệu nhạy cảm, triển khai trên quy mô dân số lớn (hàng trăm triệu người), hậu quả khó đảo ngược. Xem chi tiết tại [industry-pattern-summary.md](industry-pattern-summary.md) |
| Mobility / autonomous driving | | | | | |
| Media / news / social / political assistant | | | | | |
| Content creator | | | | | |

## Câu hỏi thảo luận (điền sau khi cả bàn thảo luận)

- Ngành nào có Severity tiềm năng cao nhất? *(gợi ý: Y tế và Mobility là 2 ứng viên hàng đầu vì cùng liên quan an toàn thể chất — cần so sánh thực tế với case của bạn cùng bàn làm Mobility)*
- Ngành nào có Scale tiềm năng lớn nhất?
- Ngành nào có Probability hoặc Frequency cao nhất?
- Ngành nào xử lý dữ liệu nhạy cảm rõ nhất?
- Ngành nào cần human-in-the-loop rõ nhất?
- Ngành nào cần bar "được ship" cao nhất?

## Đoạn tổng hợp ngắn về risk profile giữa các ngành

*(Cần điền sau khi cả bàn share xong toàn bộ case. Gợi ý khung viết: ngành nào risk profile cao nhất và vì sao, ngành nào thấp hơn và vì sao, điểm chung/khác biệt về failure mode và layer giữa các ngành, bài học chung cho việc thiết kế AI an toàn.)*

**Phần Y tế (đã có sẵn, dùng làm input cho đoạn tổng hợp chung):** Y tế có risk profile Critical vì hội tụ đủ severity cao (an toàn thể chất), scale lớn (platform dùng chung quy mô dân số), và xác suất/tần suất harm cao khi thiếu external validation hoặc khi human-in-the-loop bị suy yếu bởi áp lực vận hành (alert fatigue, KPI nội bộ).
