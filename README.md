HƯỚNG DẪN CÀI ĐẶT VÀ SỬ DỤNG CODE TRÒ CHƠI Ô ĂN QUAN (AI MINIMAX)

1. Giới Thiệu Dự Án

Đây là một chương trình mô phỏng trò chơi dân gian Việt Nam "Ô Ăn Quan" được phát triển bằng Python.

Mục tiêu: Xây dựng một giao diện đơn giản và tích hợp thuật toán trí tuệ nhân tạo Minimax (có cắt tỉa Alpha-Beta) để máy có thể chơi ở chế độ Người vs Máy (PvA) hoặc Máy vs Máy (AvA).

File Code Chính: Demo_DOAN_O_An_Quan.py

2. Yêu Cầu Hệ Thống (Prerequisites)

Chương trình được xây dựng trên nền tảng Python và sử dụng thư viện giao diện đồ họa Tkinter (thư viện chuẩn của Python).

Hệ điều hành: Windows, macOS, hoặc Linux.

Phiên bản Python: Python 3.6 trở lên (Khuyến nghị Python 3.8+).

Thư viện bắt buộc:

tkinter (thường đã được cài đặt sẵn cùng Python).

threading (thường đã được cài đặt sẵn cùng Python, dùng để chạy AI Minimax mà không làm treo GUI).

Lưu ý: Nếu bạn không thể chạy code và gặp lỗi liên quan đến Tkinter, bạn có thể cần cài đặt gói Tkinter riêng biệt cho hệ điều hành của mình (ví dụ: sudo apt-get install python3-tk trên Ubuntu).

3. Hướng Dẫn Cài Đặt (Installation)

Vì chương trình chỉ sử dụng các thư viện chuẩn của Python, quá trình cài đặt rất đơn giản.

Bước 1: Tải Code

Tải file Demo_DOAN_O_An_Quan.py về máy tính của bạn và đặt vào một thư mục dễ truy cập (ví dụ: OAnQuan_Project/).

Bước 2: Kiểm Tra Python

Mở Terminal (trên Linux/macOS) hoặc Command Prompt/PowerShell (trên Windows) và gõ lệnh sau để kiểm tra phiên bản Python:

python --version
# hoặc
python3 --version


Đảm bảo kết quả hiển thị là Python 3.x.

Bước 3: Khởi Chạy Chương Trình bằng Command Line

Sử dụng cửa sổ Terminal/Command Prompt, điều hướng đến thư mục chứa file code và chạy lệnh:

python Demo_DOAN_O_An_Quan.py
# hoặc
python3 Demo_DOAN_O_An_Quan.py


Cửa sổ giao diện đồ họa (GUI) của trò chơi sẽ hiện ra.

3.4. Khởi Chạy Chương Trình bằng Visual Studio 2022 (VS 2022)

Nếu bạn muốn tận dụng môi trường phát triển (IDE) Visual Studio 2022 để quản lý và debug code, hãy làm theo các bước sau:

Yêu cầu:

Đảm bảo bạn đã cài đặt "Phát triển Python" (Python development) trong công cụ cài đặt Visual Studio.

Các bước thực hiện:

Tạo Dự án Mới:

Mở Visual Studio 2022.

Chọn "Create a new project".

Tìm kiếm và chọn template "Python Application" (hoặc "Ứng dụng Python").

Đặt tên dự án (ví dụ: OAnQuanMinimax) và chọn thư mục lưu trữ (khuyến nghị là thư mục chứa file Demo_DOAN_O_An_Quan.py).

Thêm Mã Nguồn:

Trong cửa sổ Solution Explorer của dự án mới, bạn sẽ thấy một file mặc định (thường là PythonApplication1.py hoặc app.py).

Xóa file mặc định đó (nếu có).

Nhấp chuột phải vào tên dự án (ví dụ: OAnQuanMinimax) trong Solution Explorer, chọn Add > Existing Item... (Thêm > Mục Hiện có...).

Chọn file Demo_DOAN_O_An_Quan.py đã tải về.

Thiết lập File Khởi động:

Sau khi thêm file, nhấp chuột phải vào file Demo_DOAN_O_An_Quan.py trong Solution Explorer.

Chọn Set as Startup File (Đặt làm File Khởi động).

Chạy Chương trình:

Nhấn phím F5 (hoặc chọn Debug > Start Debugging) để chạy và debug.

Hoặc nhấn tổ hợp phím Ctrl + F5 (hoặc Debug > Start without Debugging) để chạy trực tiếp.

4. Hướng Dẫn Sử Dụng

4.1. Màn Hình Menu Chính

Sau khi khởi chạy, màn hình Menu sẽ xuất hiện, cho phép bạn chọn một trong các chế độ chơi sau:

Chế độ

Mô tả

Người vs Người (PvP)

Hai người chơi luân phiên điều khiển X và O.

Người vs Máy (PvA - AI Minimax)

Bạn điều khiển Người chơi X (Minimizing Player), Máy điều khiển Người chơi O (Maximizing Player) bằng thuật toán Minimax.

Máy vs Máy (AvA - AI Minimax)

Hai AI tự chơi với nhau (X vs O). Bạn chỉ cần quan sát.

4.2. Thao Tác Trong Game

Bắt đầu: Chọn chế độ và nhấn nút.

Lượt chơi: Màn hình sẽ hiển thị rõ ràng lượt của người chơi nào.

Người chơi X: Hàng dưới (Pits 7-11).

Người chơi O: Hàng trên (Pits 1-5).

Chọn ô:

Nếu là lượt của bạn (hoặc chế độ PvP), nhấn chuột vào ô Dân (ô nhỏ) của mình có chứa đá.

Sau khi chọn ô, một khung Direction Chooser sẽ xuất hiện yêu cầu bạn chọn hướng rải quân (Xuôi hoặc Ngược).

Quan sát AI (PvA/AvA):

Trong lượt của AI, bạn sẽ thấy thông báo "AI đang tính toán Minimax...".

Do Minimax được chạy trên một luồng riêng (threading), giao diện sẽ không bị treo. AI sẽ tự động chọn và thực hiện nước đi sau một khoảng thời gian chờ (1 giây).

Độ sâu AI mặc định: AI_DEPTH = 4. Bạn có thể thay đổi giá trị này trong file mã nguồn nếu muốn AI tính toán nhanh hơn (độ sâu thấp hơn) hoặc sâu hơn (tốn thời gian hơn).

4.3. Luật Kết Thúc Trò Chơi (NEW!)

Trò chơi kết thúc khi một trong hai điều kiện sau xảy ra:

Cả hai ô Quan (Index 0 và 6) đều không còn đá TO.

Một bên (hoặc cả hai bên) không còn bất kỳ quân Dân nào trong 5 ô nhỏ của mình.

Khi trò chơi kết thúc, chương trình sẽ tự động thực hiện luật "Hốt Chán" (Hốt tất cả quân Dân còn lại trên bàn vào điểm Quan của bên đó) và công bố người chiến thắng.

5. Cấu Trúc File & Dữ Liệu

Tên File

Mô tả

Demo_DOAN_O_An_Quan.py

Mã nguồn chính của trò chơi (Python/Tkinter), bao gồm logic game và thuật toán Minimax.

HuongDanCaiDat

File hướng dẫn này.

(Thêm Link Dữ liệu ở đây)





Bạn có thể sử dụng nội dung trên làm file hướng dẫn chính thức. Đừng quên nén tất cả các file cần thiết (báo cáo, PPTX, code, và file hướng dẫn này) thành một file .zip hoặc .rar trước khi nộp lên hệ thống.
