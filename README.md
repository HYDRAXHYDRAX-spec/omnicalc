# OmniCalc

**Máy tính khoa học · Quy đổi đơn vị · Tỷ giá ngoại tệ** — ứng dụng Android (WebView) kiêm PWA, chạy được **offline**, hỗ trợ **6 ngôn ngữ**.

<p>
  <img alt="Version" src="https://img.shields.io/badge/version-1.7.0%20(9)-19b875">
  <img alt="Android" src="https://img.shields.io/badge/Android-24%2B-3DDC84?logo=android&logoColor=white">
  <img alt="PWA" src="https://img.shields.io/badge/PWA-offline--first-4a90d9?logo=pwa&logoColor=white">
  <img alt="License" src="https://img.shields.io/badge/license-MIT-green">
</p>

> Ảnh chụp bên dưới được chụp trực tiếp trên thiết bị thật (Samsung Note 10+, 1080 × 2280).

---

## 📸 Ảnh chụp ứng dụng

| Máy tính khoa học | Quy đổi đơn vị | Ngoại tệ & Vàng |
| :---: | :---: | :---: |
| <img src="docs/screenshot-calc.png" width="240" alt="Máy tính"> | <img src="docs/screenshot-units.png" width="240" alt="Đơn vị"> | <img src="docs/screenshot-currency.png" width="240" alt="Ngoại tệ"> |

---

## Tổng quan

OmniCalc gộp ba công cụ hay dùng nhất vào một ứng dụng duy nhất, không quảng cáo chen ngang khi đang tính:

- **Máy tính** hiển thị biểu thức là dòng chính, kết quả trực tiếp hiện nhỏ bên dưới (kiểu máy tính Samsung), tính bằng bộ phân tích cú pháp AST — **không dùng `eval`**.
- **Quy đổi đơn vị** với 88 đơn vị / 12 nhóm, có đơn vị vàng truyền thống Việt Nam (Lượng, Chỉ).
- **Ngoại tệ** với 162 loại tiền, crypto và vàng, tự làm mới từ 2 nguồn API dự phòng, có sẵn mức hoàn thuế Tax-Free và phí thẻ.

---

## Tính năng

### 🧮 Máy tính

- Hiển thị kiểu Samsung: **biểu thức to ở trên**, kết quả trực tiếp nhỏ bên dưới, tự cuộn khi biểu thức dài.
- Bấm `=` xong gõ số mới → **bắt đầu phép tính mới**; gõ phép tính → tính tiếp từ kết quả.
- Toán tử và hàm: `+ − × ÷`, `^`, `n!`, `sin`, `cos`, `tan` (DEG/RAD), `log`, `ln`, `√`, `π`, `e`, ngoặc, `%`.
- Ngữ nghĩa `%` kiểu máy tính bỏ túi: `100 + 10% = 110`, `200 − 5% = 190`.
- **Băng tính (Tape)**: lưu lịch sử, chạm để dùng lại, xuất **CSV**.
- Dấu phẩy phân cách hàng nghìn ở mọi nơi hiển thị (`1,000,000`), dấu chấm thập phân.

### 📐 Quy đổi đơn vị

- 12 nhóm: Chiều dài, Khối lượng & Vàng, Nhiệt độ, Thể tích, Diện tích, Tốc độ, Thời gian, Dữ liệu số, Áp suất, Góc, Năng lượng, Công suất.
- Bảng **quy đổi tương đương** hiện toàn bộ đơn vị cùng nhóm ngay trên một màn hình.
- Đảo chiều FROM ↔ TO bằng một chạm; bàn phím có sẵn phím tắt đơn vị.

### 💱 Ngoại tệ

- 162 loại: tiền pháp định, crypto (BTC, ETH, USDT, SOL) và vàng (XAU, XAU_L).
- Hai nguồn dự phòng (`open.er-api.com` và `@fawazahmed0/currency-api`), timeout 8 giây, có cache offline.
- **Tax-Free & phí thẻ**: −8% (JP), −10% (KR/SG), −12% (EU), +1.5% → +3.5% phí Visa/Mastercard, hoặc tự nhập mức bất kỳ.
- Chạm để đổi tiền gốc, **giữ 0,5 giây** để thay đồng tiền trong danh sách ghim.

### 🌐 Khác

- **6 ngôn ngữ**: Tiếng Việt, English, 日本語, 한국어, 中文, Español (137 khóa dịch, đủ 100%).
- Hoạt động **offline** hoàn toàn với dữ liệu đã cache.
- Cờ quốc gia và biểu tượng crypto là **SVG nội tuyến** — không tải ảnh từ mạng.

---

## Bản Free và bản PRO

| | Free | PRO |
| :--- | :---: | :---: |
| Máy tính & quy đổi đơn vị | ✅ | ✅ |
| Ghim ngoại tệ | 3 | Không giới hạn |
| Làm mới tỷ giá thủ công | 6 giờ/lần *(hoặc xem 1 quảng cáo thưởng)* | Không giới hạn |
| Lịch sử tính toán | 10 phép tính | Không giới hạn + xuất CSV |
| Crypto & Vàng (XAU, Lượng) | ❌ | ✅ |
| Hoàn thuế Tax-Free & phí thẻ | ❌ | ✅ |
| Quảng cáo | Banner + quảng cáo thưởng | **Không có quảng cáo** |

Bốn gói mua: **Travel Pass 14 ngày**, **PRO Monthly**, **PRO Yearly**, **PRO Lifetime**.

### Quảng cáo

- **Banner** (adaptive, ~50 dp) đặt cố định trên đầu, không che nội dung.
- **Quảng cáo có tặng thưởng** (rewarded): người dùng Free đang trong 6 giờ chờ sẽ thấy bảng lựa chọn *"Nâng cấp PRO"* hoặc *"Xem quảng cáo để cập nhật ngay"* — xem xong 3 giây là tỷ giá cập nhật tức thì.
- Không dùng quảng cáo xen kẽ (interstitial) để tránh làm phiền khi đang tính.

---

## Kiến trúc

```text
┌──────────────────────────────────────────────────────────────┐
│                      Web Application                         │
│  index.html · styles.css · app.js · calc-engine.js · data.js  │
└───────────────────────────┬──────────────────────────────────┘
                            │
        ┌───────────────────┴────────────────────┐
        │                                        │
  [PWA / Trình duyệt]                     [Android APK]
        │                                        │
        ▼                                        ▼
  ┌──────────────┐                    ┌────────────────────────┐
  │   sw.js      │                    │  WebViewAssetLoader    │
  │ Cache Storage│                    │  (& WebView an toàn)   │
  └──────────────┘                    └───────────┬────────────┘
                                                  │
                                                  ▼
                                       ┌────────────────────────┐
                                       │    MainActivity.java   │
                                       │  @JavascriptInterface  │
                                       └────┬──────────────┬────┘
                                            │              │
                                       ┌────▼─────┐  ┌─────▼──────┐
                                       │ Billing  │  │   AdMob    │
                                       │  v8.0.0  │  │ Banner +   │
                                       └──────────┘  │ Rewarded   │
                                                     └────────────┘
```

### Vai trò các tệp chính

| Tệp | Trách nhiệm |
| :--- | :--- |
| `index.html` | Bố cục 3 màn hình, modal (Tape, Paywall, Admin), CSP nghiêm ngặt |
| `styles.css` | Design system nền tối, responsive theo chiều cao, hỗ trợ banner |
| `calc-engine.js` | Bộ phân tích AST độc lập (UMD) — không `eval`, có unit test |
| `app.js` | Trạng thái ứng dụng, controller UI, i18n 6 ngôn ngữ, gọi cầu nối native |
| `data.js` | 12 nhóm đơn vị, 162 loại tiền tệ/crypto/vàng |
| `unit-names-i18n.js` | Tên đơn vị cho tiếng Nhật, Hàn, Trung, Tây Ban Nha |
| `sw.js` | Service Worker cho bản PWA (không đăng ký trong APK) |
| `privacy.html`, `terms.html` | Chính sách quyền riêng tư & Điều khoản sử dụng (VI/EN) |
| `app-ads.txt` | Khai báo nhà phát hành cho AdMob |
| `MainActivity.java` | WebView bảo mật, edge-to-edge, cầu nối JS ↔ Java, xử lý nút Back |
| `BillingManager.java` | Google Play Billing 8.0.0, 4 gói, khôi phục giao dịch |
| `AdMobManager.java` | UMP consent, banner thu gọn theo bề rộng, quảng cáo thưởng |

---

## Cấu trúc thư mục

```text
.
├── index.html / styles.css / app.js      # Web app
├── calc-engine.js / data.js              # Nhân tính toán & dữ liệu
├── unit-names-i18n.js                    # Bản dịch tên đơn vị
├── sw.js / manifest.json                 # PWA
├── privacy.html / terms.html             # Trang pháp lý
├── app-ads.txt                           # AdMob
├── docs/                                 # Ảnh chụp cho README & Play Store
├── scripts/
│   ├── check-version.ps1                 # Đối chiếu version ở 4 nơi
│   ├── sync-assets.ps1                   # Copy web → Android assets + SHA256
│   ├── i18n-audit.js                     # Kiểm tra thiếu khóa dịch
│   ├── hardcoded-audit.js                # Tìm chuỗi hardcode
│   ├── dom-audit.js                      # Đối chiếu id JS ↔ HTML
│   └── bridge-contract-audit.js          # Đối chiếu hàm JS ↔ Java
├── tests/                                # 26 unit test cho calc-engine
└── android/                              # Dự án Android (Gradle)
    ├── app/src/main/java/com/omnicalc/app/
    └── app/src/main/res/values/billing.xml
```

---

## Bắt đầu

### Yêu cầu

| Thành phần | Phiên bản |
| :--- | :--- |
| JDK | 17 |
| Android SDK | compileSdk / targetSdk 36, minSdk 24 |
| AGP / Gradle | 8.9.2 / 8.11.1 |
| Node.js | 18+ (chỉ để chạy test & script audit) |

### Chạy bản Web / PWA

Cần HTTP server (Service Worker không chạy với `file://`):

```bash
python -m http.server 8080
# hoặc
npx serve .
```

Mở `http://localhost:8080`.

### Build Android

```powershell
# 1. Đồng bộ web assets vào APK (kèm kiểm tra SHA256)
powershell -ExecutionPolicy Bypass -File .\scripts\sync-assets.ps1

# 2. Debug APK để thử trên máy
cd android
.\gradlew.bat assembleDebug

# 3. Bản phát hành (AAB) để tải lên Google Play
.\gradlew.bat bundleRelease
```

Kết quả: `android/app/build/outputs/bundle/release/app-release.aab`

> `bundleRelease` tự chạy bước **`verifyReleaseAdIds`** — build sẽ **thất bại** nếu còn ID quảng cáo test/placeholder, tránh phát hành nhầm.

---

## Kiểm thử & kiểm tra chất lượng

```bash
npm test                                  # 26 unit test cho calc-engine
node scripts/i18n-audit.js                # 137 khóa × 6 ngôn ngữ
node scripts/dom-audit.js                 # id trong app.js có trong index.html?
node scripts/bridge-contract-audit.js     # hàm JS nào thiếu bên Java?
node scripts/hardcoded-audit.js           # chuỗi chưa dịch
powershell -File scripts/check-version.ps1   # version khớp 4 nguồn
```

| Kiểm tra | Kỳ vọng hiện tại |
| :--- | :--- |
| Unit test | 26/26 pass |
| i18n | 137 khóa, 0 thiếu |
| Hợp đồng cầu nối JS ↔ Java | 0 hàm thiếu |
| Đồng bộ assets | SHA256 khớp 11/11 |
| Version | 1.7.0 khớp `index.html`, `package.json`, `build.gradle`, `manifest.json` |

---

## Cấu hình trước khi phát hành

Tất cả ID quảng cáo nằm trong **`android/app/src/main/res/values/billing.xml`**:

| Khóa | Ý nghĩa |
| :--- | :--- |
| `admob_app_id` | AdMob App ID |
| `admob_banner_unit_id` | Đơn vị quảng cáo Banner |
| `admob_rewarded_unit_id` | Đơn vị quảng cáo có tặng thưởng |

Bốn SKU cần tạo trên Play Console (khớp `billing.xml`):

```text
omnicalc_travel_pass_14d     Travel Pass 14 ngày (mua 1 lần)
omnicalc_pro_monthly         PRO 1 tháng (thuê bao)
omnicalc_pro_yearly          PRO 1 năm (thuê bao)
omnicalc_pro_lifetime        PRO trọn đời (mua 1 lần)
```

Các bước còn lại:

1. **Keystore**: cấu hình `android/keystore.properties` (file này **không** commit — đã nằm trong `.gitignore`). Sao lưu keystore ở nơi an toàn.
2. **app-ads.txt**: đã có Publisher ID; tải file lên **thư mục gốc** của website.
3. **Privacy / Terms**: đưa `privacy.html` và `terms.html` lên hosting công khai, dán URL vào Play Console.
4. **Affiliate**: thay `REPLACE_ME` trong `affiliates.js` bằng link thật (nếu dùng).
5. **Hồ sơ Play**: ảnh chụp, feature graphic 1024 × 500, mô tả, Data safety, content rating.

---

## Quy trình phát hành

1. Tăng `versionCode` / `versionName` ở `android/app/build.gradle`.
2. Cập nhật `index.html` (`.version-tag`), `package.json`, `manifest.json` cho khớp.
3. `powershell -File scripts/check-version.ps1` → phải báo khớp 4 nguồn.
4. `powershell -File scripts/sync-assets.ps1` → đồng bộ web vào APK.
5. `npm test` và các script audit → phải xanh.
6. `cd android && .\gradlew.bat bundleRelease`.
7. Upload `app-release.aab` → Internal testing → kiểm tra trên máy thật → Production.

Chi tiết từng bước xem tại [`HUONG_DAN_PHAT_HANH.md`](HUONG_DAN_PHAT_HANH.md) và [`RELEASE_CHECKLIST.md`](RELEASE_CHECKLIST.md).

---

## Lịch sử phiên bản

### v1.7.0 — versionCode 9
- Nâng `targetSdk`/`compileSdk` lên **36** (yêu cầu của Google Play), AGP 8.9.2, Gradle 8.11.1.
- **Play Billing 8.0.0** (API `QueryProductDetailsResult`, tự kết nối lại).
- **Quảng cáo có tặng thưởng** để mở khóa cập nhật tỷ giá cho bản Free.
- Bảng lựa chọn khi hết hạn mức: *mua PRO* hoặc *xem quảng cáo*.
- Hiển thị kiểu Samsung: biểu thức là dòng chính, kết quả trực tiếp ở dưới.
- Dấu phẩy hàng nghìn trên toàn bộ ứng dụng.
- Sửa lỗi phím `=` bị cắt trên màn hình thấp.
- Thêm trang **Điều khoản sử dụng**, sửa 2 hàm cầu nối thanh toán còn thiếu.

### v1.6.0
- Tách `calc-engine.js` thành module riêng có unit test.
- Thêm admin panel ẩn (chỉ bản debug) để kiểm thử PRO.
- Hoàn thiện 6 ngôn ngữ, dọn dark pattern trong paywall.

---

## Lộ trình

- **v1.8** — Widget màn hình chính theo dõi tỷ giá yêu thích.
- **v1.9** — Đồng bộ tỷ giá crypto thời gian thực (WebSocket).
- **v2.0** — Chia tiền hóa đơn bằng OCR camera.

---

## Giấy phép & liên hệ

Phát hành theo [MIT License](LICENSE).

- Email: **quanghuytt81@gmail.com**
- Chính sách quyền riêng tư: [`privacy.html`](privacy.html)
- Điều khoản sử dụng: [`terms.html`](terms.html)
