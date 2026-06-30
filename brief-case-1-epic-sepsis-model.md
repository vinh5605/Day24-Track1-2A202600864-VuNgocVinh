# Brief Case 1 — Epic Sepsis Model bỏ sót 2/3 ca nhiễm trùng huyết

| Field | Nội dung |
|---|---|
| **Tên case** | Epic Sepsis Model (ESM) bỏ sót phần lớn ca sepsis |
| **Ngành** | Y tế / health assistant (clinical decision support) |
| **Tổ chức / sản phẩm** | Epic Systems — mô hình Epic Sepsis Model, tích hợp trong hệ thống EHR Epic; kiểm định độc lập thực hiện tại Michigan Medicine (University of Michigan) |
| **Use case AI** | Mô hình dự đoán sớm nguy cơ nhiễm trùng huyết (sepsis) dựa trên dữ liệu hồ sơ bệnh án điện tử theo thời gian thực, tạo cảnh báo cho bác sĩ/điều dưỡng để can thiệp sớm |
| **Thời điểm** | Mô hình được Epic triển khai rộng tại hàng trăm bệnh viện Mỹ từ khoảng 2017; nghiên cứu kiểm định độc lập công bố ngày 21/06/2021 trên JAMA Internal Medicine |
| **Case xảy ra chuyện gì?** | Nhóm nghiên cứu tại Michigan Medicine (Habib et al.) kiểm định độc lập Epic Sepsis Model trên 38.455 lượt nhập viện. Kết quả: mô hình chỉ phát hiện đúng 33% ca sepsis thực tế (bỏ sót khoảng 2/3 số ca), độ chính xác (AUC) thực tế chỉ đạt 0,63 — thấp hơn nhiều so với mức 0,76–0,83 mà Epic công bố nội bộ. Đồng thời, để tìm ra 1 ca dương tính thật, nhân viên y tế phải kiểm tra trung bình 109 cảnh báo, gây "alert fatigue" (mệt mỏi vì cảnh báo giả). Một nguyên nhân kỹ thuật: mô hình dùng việc đã chỉ định kháng sinh làm một biến đầu vào — nhưng kháng sinh thường được kê khi bác sĩ đã nghi ngờ sepsis, khiến mô hình một phần chỉ "lặp lại" nghi ngờ của bác sĩ thay vì phát hiện độc lập sớm hơn. |
| **Stakeholder bị ảnh hưởng** | Bệnh nhân nội trú có nguy cơ sepsis (chậm được phát hiện/điều trị); bác sĩ và điều dưỡng (gánh nặng xử lý cảnh báo giả, rủi ro mất cảnh giác với cảnh báo thật) |
| **Số liệu chính** | Sensitivity (độ nhạy) thực tế: **33%** (bỏ sót ~67% ca sepsis thật); cần kiểm tra trung bình **109 cảnh báo** để tìm 1 ca dương tính thật; AUC thực tế **0,63** so với mức 0,76–0,83 Epic công bố; kiểm định trên **38.455 lượt nhập viện** |
| **Trích nguồn ngắn** | "The Epic Sepsis Model... missed two-thirds of sepsis cases... clinicians would need to investigate 109 alerts to find one real patient." — STAT News, 21/06/2021, dẫn lại từ nghiên cứu JAMA Internal Medicine |
| **Nguồn 1** | Habib A.R., Lin A.L., Grant R.W. "The Epic Sepsis Model Falls Short — The Importance of External Validation." *JAMA Internal Medicine*, 21/06/2021. DOI/PubMed: https://pubmed.ncbi.nlm.nih.gov/34152360/ |
| **Nguồn 2** | STAT News — "A popular algorithm to predict sepsis misses most cases and sends frequent false alarms, study finds" (21/06/2021): https://www.statnews.com/2021/06/21/epic-sepsis-prediction-tool/ |
| **Ghi chú độ tin cậy** | Nguồn 1 là **primary source** (nghiên cứu bình duyệt, peer-reviewed, đăng trên tạp chí y khoa uy tín). Nguồn 2 là **high-quality secondary source** (báo chí khoa học/y tế chuyên sâu, tóm tắt đúng số liệu của nguồn 1, không mâu thuẫn). |
