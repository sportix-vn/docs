# Tournament screenshot coverage

Ảnh trong thư mục này phải được chụp từ UI Sportix thật. Không dùng ảnh mock hoặc AI-generated.

| How-to | Route | State cần có | Target/selector | Viewport | Output | Trạng thái |
| --- | --- | --- | --- | --- | --- | --- |
| Mở Dashboard | `/organizer/tournaments/dashboard?...&tab=overview` | Organizer; workspace có ít nhất một giải | `[data-tour="tournament-dashboard-nav"]` cùng khu tổng quan | Desktop 1440×900 | `organizer-dashboard-overview.png` | Ảnh cũ outdated; cần chụp |
| Mở đăng ký | `/organizer/tournaments/dashboard?...&tab=setup` | Giải nháp đã hoàn tất các mục bắt buộc | text `Sẵn sàng mở đăng ký` và nút `Mở đăng ký` | Desktop 1440×900 | `organizer-open-registration.png` | Cần chụp |
| Quản lý nội dung | `/organizer/tournaments/dashboard?...&tab=events` | Giải có ít nhất một nội dung | heading `Nội dung thi đấu` và danh sách nội dung | Desktop 1440×900 | `organizer-manage-events.png` | Cần chụp |
| Quản lý Ban tổ chức | `/organizer/tournaments/dashboard?...&tab=staff` | Chủ giải; có ít nhất một manager hoặc lời mời demo | heading `Ban tổ chức` và danh sách nhân sự | Desktop 1440×900 | `organizer-staff.png` | Text đủ rõ cho lần cập nhật này; chụp khi có state demo an toàn |
| Nhập danh sách VĐV | `/organizer/tournaments/dashboard?...&tab=athletes` | Organizer; giải có nội dung; mở `Nhập VĐV từ Excel` ở bước preview | dialog tên `Nhập VĐV từ Excel` | Desktop 1440×900 | `organizer-import-athletes.png` | Cần chụp |
| Cấu hình bảng đấu | `/organizer/tournaments/dashboard?...&tab=bracket&mode=bracket` | Nội dung có danh sách VĐV; màn cấu hình đang hiển thị preview | `[data-tour="bracket-setup-preview"]` | Desktop 1440×900 | `organizer-bracket-setup.png` | Ảnh cũ outdated; cần chụp |
| Gán vị trí bảng đấu | `/organizer/tournaments/dashboard?...&tab=bracket&mode=bracket` | Bracket trống; còn VĐV chưa được xếp | `[data-tour="bracket-setup-preview"]` cùng danh sách chưa xếp | Desktop 1440×900 | `organizer-bracket-slots.png` | Cần chụp |
| Bốc thăm | `/organizer/tournaments/dashboard?...&tab=draw` | Bracket trống có slot; chưa hoàn tất bốc thăm | `[aria-label="Bracket bốc thăm"]` | Desktop 1440×900 | `organizer-draw.png` | Cần chụp |
| Điều phối sân | `/organizer/tournaments/dashboard?...&tab=courts` | Đã bật điều phối sân; có trận sẵn sàng và sân trống | `[data-docs="tournament-court-control"]` | Desktop 1440×900 | `organizer-court-coordination.png` | Cần chụp |
| Nhập điểm | `/organizer/tournaments/dashboard?...&tab=bracket` | Giải đang diễn ra; mở trận có đủ hai bên | dialog tên `Cập nhật tỉ số` | Desktop 1440×900 | `organizer-dashboard-score-modal.png` | Tái sử dụng; đã khớp UI chính |
| Màn hình trọng tài | `/referee/matches/{matchId}` | Bật trọng tài công khai; mở link bằng phiên chưa đăng nhập; form nhập tên và PIN đang hiển thị | `[data-docs="referee-pin-entry"]` | Mobile 390×844 | `organizer-referee-pin.png` | Cần chụp |
| Kết quả thi đấu | `/organizer/tournaments/dashboard?...&tab=results` | Nội dung có trận hoàn tất; có vòng bảng hoặc nhánh đấu | `[data-docs="tournament-results"]` | Desktop 1440×900 | `organizer-results.png` | Cần chụp |

## Quy tắc chụp

- Ưu tiên local. Chỉ dùng staging khi local không thể tái tạo state.
- Dùng dữ liệu demo, không để lộ email, số điện thoại hoặc thông tin thanh toán.
- Chụp đúng vùng phục vụ thao tác; không chụp toàn màn hình chỉ để trang trí.
- Tái kiểm tra ảnh sau mỗi thay đổi lớn của Tournament Dashboard.
- Nếu selector semantic không đủ ổn định, thêm một `data-docs` tối thiểu vào vùng cần chụp.
