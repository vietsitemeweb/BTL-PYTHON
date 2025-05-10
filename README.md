Ngoại hạng Anh 2024–2025

Tổng quan dự án

Dự án gồm 4 phần, tập trung vào việc thu thập, phân tích và khai thác dữ liệu cầu thủ và chuyển nhượng tại giải Ngoại hạng Anh mùa 2024–2025. Mục tiêu là đưa ra cái nhìn trực quan, thống kê và ước tính giá trị cầu thủ dựa trên dữ liệu thật từ các trang web uy tín.
Bài 1: Thu thập dữ liệu thống kê cầu thủ từ trang FBref
Lý do lựa chọn
FBref là một nguồn dữ liệu công khai, chất lượng cao, cung cấp thống kê chi tiết về từng cầu thủ trong mùa giải.

Phương pháp
- Sử dụng `requests`, `BeautifulSoup` để thu thập bảng dữ liệu.
- Tìm bảng `stats_squads_standard_for`.
- Lọc cầu thủ thi đấu >= 90 phút.

Kết quả
- Thu được file CSV hơn 400 cầu thủ với các chỉ số đầy đủ.
Bài 2: Phân tích thống kê
Lý do lựa chọn
Giúp đánh giá hiệu suất và xu hướng nổi bật trong mùa giải.

Phương pháp
- Tìm top 3 cầu thủ theo bàn và kiến tạo.
- Tính mean, median, std.
- Vẽ histogram.
- Tìm đội có tổng số bàn cao nhất.

Kết quả
- Các cầu thủ nổi bật: Haaland, Salah, Saka.
- Phân phối lệch phải.
- Đội nổi bật: Man City.
Bài 3: Phân nhóm cầu thủ bằng K-Means + PCA
Lý do lựa chọn
Nhằm phát hiện mẫu hình và nhóm vai trò cầu thủ dựa trên đặc trưng thi đấu.

Phương pháp
- Chọn đặc trưng liên quan bàn, kiến tạo, chuyền, phòng ngự.
- PCA để giảm chiều.
- KMeans (k=3).
- Vẽ scatter plot.

Kết quả
- Nhóm 1: Tiền đạo.
- Nhóm 2: Tiền vệ tổ chức.
- Nhóm 3: Hậu vệ/ít thi đấu.
Bài 4: Ước tính giá trị chuyển nhượng cầu thủ
Lý do lựa chọn
Giúp đánh giá giá trị thị trường dựa vào hiệu suất.

Phương pháp
- Scrape dữ liệu chuyển nhượng từ FootballTransfers.
- Chuẩn hóa và kết hợp với dữ liệu FBref.
- Linear Regression để dự đoán giá trị.

Kết quả
- Huấn luyện mô hình có độ khớp tốt.
- Dự đoán ví dụ: Haaland ~170M EUR, Saka ~90M EUR.
Tổng kết
Những gì đã đạt được
- Thu thập dữ liệu đáng tin cậy.
- Phân tích hiệu suất và phân nhóm theo vai trò.
- Mô hình ước tính giá trị hợp lý.

Kết luận
Dự án ứng dụng kiến thức phân tích dữ liệu, học máy và trực quan hóa trong bóng đá. Quy trình toàn diện từ thu thập -> phân tích -> dự đoán có thể áp dụng cho nhiều lĩnh vực khác.
