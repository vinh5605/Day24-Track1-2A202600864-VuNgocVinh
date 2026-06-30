# Brief Case 2 — Thuật toán quản lý chăm sóc của Optum phân biệt chủng tộc

| Field | Nội dung |
|---|---|
| **Tên case** | Thuật toán risk-scoring của Optum (UnitedHealth Group) phân biệt chủng tộc trong phân bổ chăm sóc y tế |
| **Ngành** | Y tế / health assistant (population health management algorithm) |
| **Tổ chức / sản phẩm** | Optum, công ty con của UnitedHealth Group — thuật toán chấm điểm rủi ro dùng để xác định bệnh nhân cần đưa vào chương trình "high-risk care management" |
| **Use case AI** | Chấm điểm rủi ro sức khỏe của bệnh nhân để quyết định ai cần thêm nguồn lực chăm sóc chủ động (theo dõi, can thiệp sớm). Thuật toán dùng **chi phí y tế trong quá khứ** làm proxy (biến đại diện) cho "mức độ bệnh/nhu cầu sức khỏe" |
| **Thời điểm** | Nghiên cứu phơi bày vấn đề công bố ngày 25/10/2019 trên tạp chí *Science*; thuật toán đã được nhiều hệ thống y tế Mỹ sử dụng trong nhiều năm trước đó |
| **Case xảy ra chuyện gì?** | Nhóm nghiên cứu (Obermeyer, Powers, Vogeli, Mullainathan) phát hiện: ở cùng một điểm rủi ro do thuật toán chấm, bệnh nhân da đen trên thực tế bệnh nặng hơn đáng kể so với bệnh nhân da trắng. Nguyên nhân: thuật toán dùng "chi phí y tế đã chi" làm thước đo "nhu cầu sức khỏe", trong khi bệnh nhân da đen có xu hướng chi tiêu y tế thấp hơn do rào cản tiếp cận hệ thống y tế (không phải vì họ khỏe hơn). Hệ quả: bệnh nhân da đen bị đánh giá thấp hơn thực tế và ít được chọn vào chương trình chăm sóc chủ động hơn dù bệnh nặng tương đương hoặc hơn. |
| **Stakeholder bị ảnh hưởng** | Bệnh nhân da đen (Black patients) trong các hệ thống y tế Mỹ sử dụng thuật toán này hoặc thuật toán tương tự |
| **Số liệu chính** | Thuật toán dạng này được dùng để quản lý chăm sóc cho **hơn 200 triệu người/năm** tại Mỹ; ở cùng mức bệnh mãn tính, bệnh nhân da đen chi tiêu y tế ít hơn **khoảng 1.800 USD/năm** so với bệnh nhân da trắng; do đó bias của thuật toán làm giảm mức độ chăm sóc bệnh nhân da đen nhận được đi **hơn 50%**; sau khi nhóm nghiên cứu hợp tác điều chỉnh lại biến mục tiêu, bias giảm được **84%** |
| **Trích nguồn ngắn** | "Remedying this disparity would increase the percentage of Black patients receiving additional help from 17.7% to 46.5%." — Obermeyer et al., *Science*, 25/10/2019 |
| **Nguồn 1** | Obermeyer Z., Powers B., Vogeli C., Mullainathan S. "Dissecting racial bias in an algorithm used to manage the health of populations." *Science*, 25/10/2019, vol. 366, issue 6464, pp. 447–453. https://www.science.org/doi/10.1126/science.aax2342 |
| **Nguồn 2** | Science News — "A health care algorithm's bias disproportionately hurts black people" (24/10/2019): https://www.sciencenews.org/article/bias-common-health-care-algorithm-hurts-black-patients |
| **Ghi chú độ tin cậy** | Nguồn 1 là **primary source** (nghiên cứu bình duyệt đăng trên *Science* — một trong những tạp chí khoa học uy tín nhất). Nguồn 2 là **high-quality secondary source**, tóm tắt khớp với nguồn 1, không có mâu thuẫn. |
