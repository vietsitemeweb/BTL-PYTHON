Bài 1: Thu thập dữ liệu thống kê cầu thủ từ trang FBref
Lý do lựa chọn
FBref là một nguồn dữ liệu công khai, chất lượng cao, cung cấp thống kê chi tiết về từng cầu thủ trong mùa giải, bao gồm số phút thi đấu, bàn thắng, kiến tạo, chuyền bóng, phòng ngự v.v. Dữ liệu này là nền tảng cho toàn bộ các phân tích sau.

Phương pháp
Sử dụng thư viện requests, BeautifulSoup để thu thập bảng dữ liệu từ trang FBref.

Tìm đúng bảng có id "stats_squads_standard_for".

Lọc ra những cầu thủ thi đấu ít nhất 90 phút để đảm bảo dữ liệu có ý nghĩa.

Kết quả
Thu được file CSV có hơn 400 cầu thủ.

Mỗi cầu thủ có đầy đủ thông tin: tên, đội, phút thi đấu, bàn thắng, kiến tạo,...

Dữ liệu sạch, sẵn sàng cho bước phân tích.

Bài 2: Phân tích thống kê
Lý do lựa chọn
Phân tích thống kê giúp đánh giá hiệu suất cá nhân và tập thể, cũng như xác định xu hướng nổi bật trong mùa giải. Đây là bước đầu tiên trong việc hiểu dữ liệu sâu hơn.

Phương pháp
Tìm top 3 cầu thủ theo số bàn thắng và kiến tạo.

Tính các thống kê mô tả (mean, median, standard deviation).

Vẽ biểu đồ histogram để biểu diễn phân bố số bàn và số kiến tạo.

Tìm đội có thành tích tốt nhất dựa trên tổng số bàn thắng của tất cả cầu thủ.

Kết quả
Các cầu thủ nổi bật: Erling Haaland, Mohamed Salah, Bukayo Saka.

Phân phối số bàn thắng có độ lệch phải (nhiều cầu thủ ghi ít bàn, ít cầu thủ ghi nhiều).

Đội nổi bật: Manchester City dẫn đầu về tổng số bàn.

Có biểu đồ trực quan hỗ trợ kết luận.

Bài 3: Phân nhóm cầu thủ bằng K-Means + PCA
Lý do lựa chọn
Mục tiêu là phân nhóm các cầu thủ dựa trên hiệu suất chơi bóng để tìm ra những mẫu hình (patterns) ẩn trong dữ liệu. PCA giúp giảm chiều dữ liệu, còn K-Means giúp gom nhóm.

Phương pháp
Chọn các đặc trưng: bàn thắng, kiến tạo, số phút thi đấu, đường chuyền, hành động phòng ngự,...

Dùng PCA để giảm chiều còn 2D.

Dùng K-Means để phân thành 3 nhóm.

Vẽ scatter plot thể hiện phân nhóm theo màu.

Kết quả
Nhóm 1: Tiền đạo chủ lực (nhiều bàn, ít phòng ngự).

Nhóm 2: Tiền vệ tổ chức (kiến tạo và chuyền nhiều).

Nhóm 3: Hậu vệ hoặc cầu thủ ít thi đấu (ít đóng góp trực tiếp).

Có biểu đồ minh họa phân cụm rõ ràng.

Bài 4: Ước tính giá trị chuyển nhượng cầu thủ
Lý do lựa chọn
Giá trị chuyển nhượng phản ánh giá trị thị trường của cầu thủ. Mục tiêu là dự đoán giá trị này dựa trên hiệu suất thi đấu, kết hợp với dữ liệu thật từ trang FootballTransfers.

Phương pháp
Scrape dữ liệu “Biggest Transfers” từ FootballTransfers bằng Selenium.

Chuẩn hóa dữ liệu để so sánh và huấn luyện mô hình hồi quy tuyến tính.

Dùng LinearRegression (scikit-learn) để xây dựng mô hình.

Dự đoán giá trị chuyển nhượng cho tất cả cầu thủ trong file FBref.

Kết quả
Lấy được danh sách các cầu thủ có giá trị chuyển nhượng cao.

Huấn luyện mô hình dự đoán khá hợp lý (tương quan tốt).

Một số dự đoán ví dụ:

Haaland ~ 170 triệu EUR

Saka ~ 90 triệu EUR

Một số hậu vệ trung bình ~ 20–30 triệu EUR

Tổng kết
Những gì đã đạt được
Thu thập và xử lý dữ liệu cầu thủ chính xác, đáng tin cậy.

Phân tích thống kê giúp hiểu rõ hiệu suất cầu thủ và đội bóng.

Phân cụm giúp nhóm cầu thủ theo vai trò và phong cách chơi.

Mô hình dự đoán giá trị chuyển nhượng gần sát với thực tế.

Kết luận
Dự án này cung cấp một quy trình toàn diện, từ thu thập dữ liệu đến phân tích chuyên sâu và dự đoán có ý nghĩa thực tiễn. Từ đó, sinh viên có thể ứng dụng kiến thức về xử lý dữ liệu, thống kê, học máy và trực quan hóa dữ liệu vào các bài toán thực tế trong lĩnh vực thể thao.
