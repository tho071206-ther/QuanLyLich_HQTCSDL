# QuanLyLich_HQTCSDL   ( Nhóm 9 )
Ai làm mục nào thì chỉ tập trung đúng phần đó, không đụng chéo
File nào thuộc phần mình thì code → Không cần làm dư Không sửa file người khác nếu chưa hỏi Tránh conflict Git Nếu cần sửa → báo trước Commit rõ ràng Test riêng phần mình trước khi push Tránh lỗi làm crash toàn bộ project Không tự ý đổi tên file / folder
Mỗi người pull bài về và làm 1 branch riêng: Không code trực tiếp trên main
# Người 5: Chỉ sửa file trong thư mục Views (XAML).
# Người 4: Xử lý file .xaml.cs và các thư mục logic.
# Người 1, 2, 3: Chỉ đẩy file script vào thư mục Database/Scripts.

## App.config               <-- Connection String tới SQL Server.
## App.xaml
## MainWindow.xaml          
## Database            
  ── DatabaseHelper.cs    <-- Chứa code mở SqlConnection, gọi Stored Procedure, bắt lỗi Transaction.
## Models               
   ── UserModel.cs         <-- Id, Username, Password, Role...
  ── ScheduleModel.cs     <-- Id, TenLichTrinh, NgayTao...
  ── TaskModel.cs         <-- Id, TenCongViec, ThoiGianBatDau, TrangThai...
## ViewModels            
 ── BaseViewModel.cs     
 ── RelayCommand.cs      
  ── MainViewModel.cs     
  ── LoginViewModel.cs    <-- Code truyền User/Pass xuống DB để kiểm tra.
 ── ScheduleViewModel.cs <-- Code các hàm Thêm, Xóa, Sửa, Lấy danh sách, Tìm kiếm.
## Views                 Người 5 
    ── LoginView.xaml       <-- UserControl đăng nhập.
    ── DashboardView.xaml   <-- UserControl màn hình chính, thống kê công việc.
    ── ScheduleView.xaml    <-- UserControl chứa DataGrid để hiển thị danh sách lịch trình.
