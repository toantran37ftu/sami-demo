# Nguyên tắc UI cho phần mềm kế toán (rút từ MISA, Fast)

Kế toán Việt Nam đã quen tay với MISA SME/AMIS Kế toán và Fast Accounting nhiều năm. Họ không đánh giá UI theo "đẹp", mà theo **có làm đúng thói quen tay không**: tìm đúng chỗ, bấm đúng phím, đọc số đúng cột. Sami giữ phần khác biệt (AI đọc chứng từ, gợi ý khoản mục, trợ lý chat) nhưng phải **đặt nó vào khuôn quen thuộc**, không bắt kế toán học lại cách làm.

Bộ nguyên tắc dưới đây có 3 mức: **Bắt buộc** (thiếu là bị chê "khó dùng"), **Nên có**, **Sami thêm** (điểm AI, chỉ thêm, không thay luồng chuẩn).

> Ghi chú: ta học **quy ước** (bố cục, thuật ngữ, phím tắt, thứ tự cột), không sao chép logo, màu thương hiệu hay hình ảnh của MISA/Fast.

---

## A. Khung ứng dụng

| # | Nguyên tắc | Mức | MISA / Fast làm thế nào |
|---|---|---|---|
| A1 | Menu trái chia theo **phân hệ nghiệp vụ** (Quỹ, Ngân hàng, Mua hàng, Bán hàng, Thuế, Tổng hợp, Báo cáo, Danh mục), không chia theo tính năng | Bắt buộc | AMIS: mỗi phân hệ một mục, thêm "Danh mục", "Báo cáo" riêng. Fast: 16 phân hệ |
| A2 | Thanh trên luôn hiện **ngày hạch toán / kỳ làm việc**, ô **tìm nhanh** chức năng–chứng từ–báo cáo, người dùng | Bắt buộc | AMIS: thiết lập Ngày hạch toán, tìm nhanh Alt+X |
| A3 | Trang đầu mỗi phân hệ có tab **Quy trình** (sơ đồ nghiệp vụ, bấm ô để mở chứng từ) và tab danh sách chứng từ | Nên có | AMIS: tab Quy trình, tab Thu chi tiền… |
| A4 | Giao diện **phẳng, dày đặc thông tin**: nền trắng, 1 màu nhấn, bo góc nhỏ (≤ 4px), không gradient, không bóng đổ lớn | Bắt buộc | Cả hai |
| A5 | Thuật ngữ **chế độ kế toán tiếng Việt**: Ghi sổ, Bỏ ghi, Hạch toán, Đối tượng, Diễn giải, TK Nợ/TK Có, Ngày hạch toán. Không dùng tiếng Anh (Kanban, Browse…) cho thao tác nghiệp vụ | Bắt buộc | Cả hai |

## B. Màn hình danh sách chứng từ

| # | Nguyên tắc | Mức | Ghi chú |
|---|---|---|---|
| B1 | **Lưới kẻ ô**, dòng thấp (~32px), chữ 13px, tiêu đề cột viết thường | Bắt buộc | Không dùng thẻ (card), không pill màu trong từng ô |
| B2 | Thứ tự cột chuẩn: **Ngày hạch toán · Ngày chứng từ · Số chứng từ · Diễn giải · Số tiền · Đối tượng · Trạng thái** | Bắt buộc | Kế toán dò cột theo trí nhớ cơ |
| B3 | **Dòng tổng cộng** ở đáy lưới, luôn thấy | Bắt buộc | Dùng để đối chiếu nhanh với sổ |
| B4 | **Thanh công cụ trên lưới**: Thêm · Sửa/Xem · Xóa · Ghi sổ/Bỏ ghi · Nhân bản · In · Xuất Excel · Nạp. Nút tác động lên dòng đang chọn | Bắt buộc | AMIS: nút Thêm có ▾ (Nhập khẩu Excel) |
| B5 | **Click = chọn dòng, double-click / Enter = mở**. Mũi tên lên/xuống để di chuyển | Bắt buộc | Click mở ngay là thói quen web, kế toán thấy "lỡ tay" |
| B6 | **Ngăn chi tiết phía dưới** (master–detail): chọn chứng từ là thấy các dòng hạch toán, không cần mở | Bắt buộc | AMIS: thanh Mở rộng / Thu gọn ở đáy danh sách |
| B7 | Lọc theo **kỳ** (Tháng này, Quý này, Từ ngày–Đến ngày), tìm theo số CT / đối tượng / MST | Bắt buộc | |
| B8 | Trạng thái bằng **chữ**: "Đã ghi sổ / Chưa ghi sổ"; chứng từ chưa ghi sổ chữ màu đỏ/đậm | Nên có | |
| B9 | Chọn nhiều để **ghi sổ / bỏ ghi / in hàng loạt** | Nên có | |
| B10 | Ẩn/hiện, sắp xếp cột; mật độ 1 dòng / 2 dòng | Nên có | AMIS: bánh răng |

## C. Form chứng từ

| # | Nguyên tắc | Mức | Ghi chú |
|---|---|---|---|
| C1 | Tiêu đề = **loại chứng từ + số** (Chứng từ mua hàng 0001245) và trạng thái ghi sổ | Bắt buộc | |
| C2 | Phần đầu 2 cột: **trái** Đối tượng, MST, Địa chỉ, Diễn giải/Lý do; **phải** Ngày hạch toán, Ngày chứng từ, Số chứng từ (+ Ký hiệu, Số hóa đơn) | Bắt buộc | AMIS: khối đối tượng trước, khối chứng từ sau |
| C3 | Lưới chi tiết theo **tab**: **Hạch toán** (Diễn giải · TK Nợ · TK Có · Số tiền · Khoản mục CP · Bộ phận) và **Thuế** (Diễn giải thuế · % thuế · Tiền thuế · TK thuế · Ký hiệu · Số HĐ · Ngày HĐ · MST) | Bắt buộc | AMIS: tab "Hạch toán", "Kê khai hóa đơn và hạch toán thuế" |
| C4 | **TK Nợ / TK Có là cột chính** trong lưới, hiện số TK; khoản mục là thông tin phụ | Bắt buộc | Kế toán nghĩ theo cặp TK |
| C5 | Nhập lưới **như Excel**: Enter/Tab sang ô kế, Enter ở ô cuối tự thêm dòng, Ctrl+Insert thêm dòng, Ctrl+Delete xóa dòng | Bắt buộc | AMIS: Ctrl+Insert / Ctrl+Delete |
| C6 | **Dòng tổng** cuối lưới, **số tiền bằng chữ** ở đáy | Bắt buộc | |
| C7 | **Thanh nút cố định đáy form**: Cất (Ctrl+S) · Cất và Thêm (Ctrl+Shift+S) · Cất và Đóng (Ctrl+Q) · Ghi sổ · Hủy (Esc). Phím tắt ghi ngay trên nút | Bắt buộc | AMIS dùng đúng các phím này |
| C8 | Form chiếm trọn màn hình, không bị che bởi panel khác | Nên có | |

## D. Số, ngày, chữ

| # | Nguyên tắc | Mức |
|---|---|---|
| D1 | Số tiền **canh phải**, phân tách nghìn bằng dấu chấm (1.845.000), không ghi "₫" trong lưới, số âm trong ngoặc | Bắt buộc |
| D2 | Ngày **dd/MM/yyyy** đủ năm | Bắt buộc |
| D3 | Font số dạng tabular (các chữ số rộng bằng nhau) để cột thẳng | Bắt buộc |

## E. Phím tắt chuẩn

Ưu tiên theo AMIS (phần lớn kế toán đang dùng), thêm F-key kiểu Fast cho người quen Fast. Trình duyệt không cho chặn Ctrl+N / Ctrl+1, nên "Thêm" dùng **F4** (giống Fast).

| Phím | Việc | Nguồn |
|---|---|---|
| F4 | Thêm chứng từ | Fast |
| Enter / F3 | Mở / sửa chứng từ đang chọn | Fast F3 |
| ↑ ↓ | Di chuyển dòng trong danh sách | Cả hai |
| Ctrl+S | Cất | AMIS |
| Ctrl+Shift+S | Cất và Thêm | AMIS |
| Ctrl+Q | Cất và Đóng | AMIS |
| Ctrl+G | Ghi sổ (Duyệt) | — |
| Ctrl+Insert / Ctrl+Delete | Thêm / xóa dòng lưới | AMIS |
| Esc | Đóng form | Cả hai |
| Alt+X | Tìm nhanh | AMIS |
| F1 | Bảng phím tắt | Cả hai (F1 = trợ giúp) |

## F. Phần AI của Sami — đặt vào khuôn

| # | Nguyên tắc |
|---|---|
| F1 | AI **điền vào form chuẩn**, không tạo form riêng. Ô do AI điền có nền nhạt + nhãn "AI", kế toán sửa như ô thường |
| F2 | "Duyệt" của Sami = **Ghi sổ** trong ngôn ngữ kế toán; hiển thị cả hai nếu cần ("Duyệt (ghi sổ)") |
| F3 | Chứng từ gốc (PDF/ảnh) là **ngăn phụ bên phải** form, bật/tắt được — không đẩy lưới hạch toán xuống dưới |
| F4 | Trợ lý AI là **nút nổi + panel**, không chiếm menu nghiệp vụ |
| F5 | Kanban chỉ là **chế độ xem phụ**; mặc định luôn là lưới danh sách |

---

## Áp dụng vào Sami (bản này)

- Đổi toàn bộ giao diện sang phẳng, lưới kẻ ô, dày đặc (A4, B1, D1–D3).
- Thanh trên: ngày hạch toán, tìm nhanh Alt+X, phím tắt F1 (A2).
- Danh sách chứng từ: cột chuẩn, dòng tổng cộng, thanh công cụ, click chọn / double-click mở, ↑↓, ngăn chi tiết hạch toán phía dưới, mặc định lưới thay vì Kanban (B1–B8, F5).
- Form chứng từ: tiêu đề loại + số, phần đầu 2 cột, tab Hạch toán / Thuế / Bút toán, cột TK Nợ–TK Có, nhập lưới bằng Enter, thanh nút đáy có phím tắt (C1–C7), chứng từ gốc ở ngăn phải (F3).

Vòng 2 (bám sát khuôn AMIS):
- Menu trái nền tối, nút hành động chính màu xanh lá, nút "Thêm ▾" tách đôi (nhập tay / tải hóa đơn / đồng bộ).
- Danh sách: tab trạng thái có số đếm, "Thực hiện hàng loạt ▾", cột **Chức năng** cố định bên phải (Xem ▾: duyệt, bỏ duyệt, để xử lý sau, xem lịch sử), dòng phân trang "Tổng số: N bản ghi".
- Form: tổng tiền thanh toán chữ lớn ở góc phải phần đầu, nút ‹ › và × trên tiêu đề, chân form nền tối: Hủy/Đóng bên trái, Cất… và nút xanh bên phải.

UX tốt hơn MISA (giữ khuôn, thêm tiện):
- Chuyển chứng từ trước / sau ngay trong form (‹ ›, PgUp/PgDn) — không phải đóng form, chọn dòng, mở lại.
- Ngăn hạch toán dưới danh sách cập nhật khi chọn dòng, không cần mở chứng từ.
- Chứng từ gốc (PDF/ảnh) đặt cạnh form để so khi nhập; AI điền sẵn, ô AI điền có đánh dấu.
- "Theo bước" (Kanban) là chế độ xem phụ để dọn hàng chờ duyệt.

Chưa làm (để vòng sau): tab Quy trình cho từng phân hệ (A3), ẩn/hiện cột (B10), xóa / nhân bản / in chứng từ, lọc theo từng cột.

## Nguồn

- MISA AMIS – Ý nghĩa các chức năng trên giao diện nhập liệu: https://helpact.misa.vn/?p=79481
- MISA AMIS – Cải tiến giao diện: https://helpact.misa.vn/?p=23581
- MISA AMIS – Chi khác bằng tiền mặt: https://helpact.misa.vn/?p=533
- MISA AMIS – Chi mua ngoài có hóa đơn: https://helpact.misa.vn/kb/chi_mua_ngoai_co_hoa_don/
- MISA AMIS – Tìm kiếm nhanh: https://helpact.misa.vn/?p=23456
- Fast Accounting – phím chức năng (trang đào tạo bên thứ ba): https://www.ketoanthienung.net/cach-su-du-ng-pha-n-me-m-ke-toa-n-fast-accounting-qua-mang.htm
