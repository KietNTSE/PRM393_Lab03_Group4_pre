# Bộ Slide Thuyết Trình Lab 3 — EventHub (HTML & PDF)

Bộ slide này được xây dựng bằng **Reveal.js (HTML/CSS thuần qua CDN, 0 dependencies)**, tuân thủ 100% khung chuẩn **Software Project Presentation Guideline V11** (14 slide, tỉ lệ chuẩn 16:9, bố cục 4 phần: *Problem $\rightarrow$ Design $\rightarrow$ Demo Workflow $\rightarrow$ Proof*).

---

## 1. Cách Chạy Slide Trên GitHub Pages (`github.io`)

File slide được đặt trực tiếp tại `slides/index.html`. Để chia sẻ link online cho giảng viên và hội đồng xem trực tiếp:

1. Đẩy code lên GitHub:
   ```bash
   git add slides/
   git commit -m "docs(slides): add HTML presentation slide deck for Lab 3"
   git push origin main
   ```
2. Vào GitHub Repository $\rightarrow$ **Settings** $\rightarrow$ chọn mục **Pages** (cột bên trái).
3. Tại phần **Build and deployment**:
   - **Cách 1 (Tự động qua GitHub Actions - Khuyên dùng)**:
     - **Source**: Chọn `GitHub Actions`. Workflow `.github/workflows/deploy-slides.yml` đã được cấu hình sẵn sẽ tự động kích hoạt và deploy mỗi khi push code lên `main`.
   - **Cách 2 (Deploy trực tiếp từ Branch)**:
     - **Source**: Chọn `Deploy from a branch`.
     - **Branch**: Chọn `main`, thư mục `/ (root)`. Nhấn **Save**.
4. Sau 1–2 phút, link slide online hoạt động tại:
   - Repo nhóm chính: `https://thinhcri.github.io/PRM393_Lab03_Group4/slides/`
   - Repo fork: `https://kietntse.github.io/PRM393_Lab03_Group4_pre/slides/`

---

## 2. Cách Xuất Ra File PDF Chuẩn (`Lab03_Group4_slides.pdf`)

Reveal.js hỗ trợ chế độ in PDF chuyên dụng giữ nguyên độ nét vector và màu sắc:

1. Mở file `slides/index.html` bằng trình duyệt **Google Chrome** hoặc **Microsoft Edge** (chạy local hoặc mở link GitHub Pages).
2. Thêm tham số `?print-pdf` vào cuối URL, ví dụ:
   - Chạy local: `file:///D:/GitHub/PRM_LAB3/PRM393_Lab03_Group4/slides/index.html?print-pdf`
   - Hoặc link online: `https://.../slides/?print-pdf`
3. Nhấn tổ hợp phím **`Ctrl + P`** (hoặc `Cmd + P` trên Mac).
4. Thiết lập trong hộp thoại In của trình duyệt:
   - **Destination (Máy in đích)**: `Save as PDF` (Lưu dưới dạng PDF).
   - **Layout (Bố cục)**: `Landscape` (Khổ ngang).
   - **Margins (Lề)**: `None` (Không có).
   - **Options (Tùy chọn)**: Tích chọn **`Background graphics`** (Đồ họa nền) để nhận đầy đủ màu nền và khung thẻ.
5. Nhấn **Save** và lưu file vào:
   `slides/Lab03_Group4_slides.pdf`

---

## 3. Cấu Trúc Nội Dung 25 Slide Chuẩn Guideline (1 / 25 đến 25 / 25)

Bộ slide tái hiện chuẩn xác 100% từng slide theo tài liệu **PRM393 / HƯỚNG DẪN CHUẨN BỊ LAB 3 THỰC HÀNH**:

- **Slide 01 (1/25)**: **TỔNG QUAN** — Từ thiết kế Lab 2 đến ứng dụng Flutter kết nối đám mây.
- **Slide 02 (2/25)**: **MÔI TRƯỜNG** — Chuẩn bị trước khi thực hành (Flutter, Android, Firebase CLI, ARTEMIS, tài khoản test).
- **Slide 03 (3/25)**: **KHỞI TẠO** — Thiết lập dự án Firebase (ID Android, gói FlutterFire, flutterfire configure, Console).
- **Slide 04 (4/25)**: **KIẾN TRÚC** — Ranh giới tích hợp theo MVVM (View $\rightarrow$ ViewModel $\rightarrow$ Service $\rightarrow$ Firebase SDK).
- **Slide 05 (5/25)**: **FIREBASE 01 - KHÁI NIỆM** — Firebase Authentication (Định nghĩa, Vai trò, Cách hoạt động, Yêu cầu Lab 3).
- **Slide 06 (6/25)**: **FIREBASE 01 - TÍCH HỢP** — Firebase Authentication (Bật Google, SHA Android, authStateChanges, xóa state khi logout).
- **Slide 07 (7/25)**: **FIREBASE 01 - KIỂM CHỨNG** — Firebase Authentication (Trình diễn Google Sign-In, ảnh trước/sau, Console Users, thông báo lỗi).
- **Slide 08 (8/25)**: **FIREBASE 02 - KHÁI NIỆM** — Firebase Cloud Storage (Định nghĩa, Vai trò, Cách hoạt động reports/{uid}/..., Yêu cầu Lab 3).
- **Slide 09 (9/25)**: **FIREBASE 02 - TÍCH HỢP** — Firebase Cloud Storage (Tạo PDF, tải lên hiển thị tiến độ %, URL tải xuống, storage.rules).
- **Slide 10 (10/25)**: **FIREBASE 02 - KIỂM CHỨNG** — Firebase Cloud Storage (Tiến độ & URL Console, storage.rules trên GitHub, cấm allow true).
- **Slide 11 (11/25)**: **FIREBASE 03 - KHÁI NIỆM** — Firebase Cloud Messaging (Định nghĩa, Vai trò, 3 trạng thái, Yêu cầu Lab 3).
- **Slide 12 (12/25)**: **FIREBASE 03 - TÍCH HỢP** — Firebase Cloud Messaging (Quyền Android 13+, xử lý 3 trạng thái, lưu Hộp thư, chạm điều hướng).
- **Slide 13 (13/25)**: **FIREBASE 03 - KIỂM CHỨNG** — Firebase Cloud Messaging (Gửi thử từ Console, ghi nhận 3 trạng thái, kiểm tra từ chối quyền, ghi token).
- **Slide 14 (14/25)**: **FIREBASE 04 - KHÁI NIỆM** — Google Analytics for Firebase (Định nghĩa, Vai trò, Cấu trúc sự kiện + tham số, Yêu cầu Lab 3).
- **Slide 15 (15/25)**: **FIREBASE 04 - TÍCH HỢP** — Firebase Analytics (docs/analytics-plan.md, ít nhất 7 sự kiện, snake_case, user ID sau login, No PII).
- **Slide 16 (16/25)**: **FIREBASE 04 - KIỂM CHỨNG** — Firebase Analytics (DebugView Console, ảnh chụp từng sự kiện, đối chiếu tiêu chí Lab 2).
- **Slide 17 (17/25)**: **FIREBASE 05 - KHÁI NIỆM** — Firebase Crashlytics (Định nghĩa, Vai trò, Cách hoạt động, Yêu cầu Lab 3).
- **Slide 18 (18/25)**: **FIREBASE 05 - TÍCH HỢP** — Firebase Crashlytics (Khởi tạo error handler, gửi non-fatal từ luồng thật, user ID & custom key, crash test).
- **Slide 19 (19/25)**: **FIREBASE 05 - KIỂM CHỨNG** — Firebase Crashlytics (Console hiển thị non-fatal & crash, thông báo UI, không kích hoạt crash ở luồng thường).
- **Slide 20 (20/25)**: **FIREBASE 06 - KHÁI NIỆM** — Firebase Remote Config (Định nghĩa, Vai trò, Cách hoạt động, Yêu cầu Lab 3).
- **Slide 21 (21/25)**: **FIREBASE 06 - TÍCH HỢP** — Firebase Remote Config (2 tham số + default values, RemoteConfigService, thay đổi Console không rebuild).
- **Slide 22 (22/25)**: **FIREBASE 06 - KIỂM CHỨNG** — Firebase Remote Config (Ảnh Console & UI trước/sau, kiểm tra fallback khi mất mạng, giải thích cache & fetch).
- **Slide 23 (23/25)**: **ĐẢM BẢO CHẤT LƯỢNG** — ARTEMIS — Chuẩn bị kiểm thử tự động đầu cuối (Ít nhất 10 ca, chạy 3 lần, nhánh lỗi, Android gốc, phiên khám phá 15–30p).
- **Slide 24 (24/25)**: **RÀ SOÁT KỸ THUẬT** — AI Code Review — Quyết định dựa trên bằng chứng (Review PR #3, 5 findings thuộc 2+ nhóm lỗi, commit sửa độc lập).
- **Slide 25 (25/25)**: **SẴN SÀNG CHO LAB 3** — Danh sách kiểm tra và sản phẩm nộp (Đủ 6 dịch vụ có lỗi, bộ tài liệu, nhật ký & Console, GitHub/PDF/Video).
