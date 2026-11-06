# Bài giảng 3D · THCS & Sinh học

15 bài trích từ “Sáng Ăn Khoai” — [`nclamvn/bai-giang`](https://github.com/nclamvn/bai-giang),
commit `b075043` (repo gốc ~240 MB, 3.425 file). Repo này chỉ giữ phần đã chọn,
tổng ~20 MB. **Không** gồm Cơ thể người 3D (143 MB) — bài đó nên là repo riêng nếu cần.

## Gồm những gì

| Nhóm | Bài |
|---|---|
| Bài học 3D Sinh học (3) | Hành Trình Vào Tế Bào (Sinh 10), Vào Ty Thể (Sinh 10), Neuron và xung thần kinh (Sinh 11) |
| Lộ trình (1) | Sinh học tế bào lớp 10 (`chu-de/sinh-hoc-te-bao/`) |
| Thư viện THCS 6–9 (7) | Luyện gang trong lò cao, Luyện kim (điện phân + nhiệt nhôm), Sản xuất xi măng, Các nhân tố hình thành đất, Hệ quả địa lí của chuyển động Trái Đất, Vòng tuần hoàn nước, Đai khí áp – đới gió – hoàn lưu ba vòng |
| Thư viện Sinh học (5) | Enzyme, Nguyên phân, Xung thần kinh, Hút/mất nước tế bào thực vật, Vận chuyển qua màng |
| Gói dạy thử 45 phút (2) | Tế Bào, Neuron (`giao-vien/`) |

Kèm theo: `shell/` (vỏ lên lớp chung), `design/` (font Be Vietnam Pro / Noto Serif /
JetBrains Mono, logo), `thu-vien/anh/` (ảnh dùng chung trong bài), `thu-vien/covers/`
(ảnh bìa), `src/` + `build.sh` (nguồn để dựng lại trang Tế Bào).

`thu-vien/catalog.vi.json` và `thu-vien/gdpt2018.json` đã rút gọn chỉ giữ các bài
trong repo này (catalog 54 → 12 bài; gdpt 57 mục → 15 mục gồm te-bao, ty-the, chu-de).

## Chạy

```bash
python3 -m http.server 8777   # mở http://localhost:8777
```

Mở bằng HTTP (không mở file trực tiếp) vì bài Tế Bào tải dữ liệu ribosome.

## Deploy

Site tĩnh thuần, không build, không backend:

- **GitHub Pages:** bật Pages từ nhánh `main`, thư mục `/` (đã có `.nojekyll`).
- **Vercel:** Import Git Repository, Framework Preset **Other**, Build Command
  **trống**, Output Directory `./`. Không chạy build.

## Giấy phép — đọc kỹ, không gán chung một giấy phép

- Bài Tế Bào / Ty Thể / Neuron, trang AR và công cụ: **MIT** (xem `LICENSE`).
- 12 bài thư viện (`thu-vien/`): **CC BY-NC 4.0** — bản tiếng Việt của Tongjiang Lab,
  chỉ dùng phi thương mại (xem `thu-vien/GHI-CONG.md`).
- Font Be Vietnam Pro, Noto Serif, JetBrains Mono: SIL Open Font License 1.1
  (xem `design/fonts/OFL-*.txt`).

## Lưu ý

- Thẻ og/canonical trong các file bài vẫn trỏ về `nclamvn.github.io/bai-giang/…`
  vì repo này chưa có domain mới. Site vẫn chạy; khi có domain mới thì build lại
  bằng `tools/build_pages.py` / `tools/the_chia_se.py` ở repo gốc.
- Các bài thư viện trỏ tới `thu-vien/shared/screen/section.css` nhưng file này
  không có trong repo gốc (mở live cũng 404) — link chết từ code gốc, không ảnh
  hưởng bài chạy.
- 3 trong 7 bài THCS cũng dạy trực tiếp ở lớp 10/12 (luyện kim, xi măng, bài đất):
  bộ lọc THCS nghĩa là “dùng được cho THCS”, không phải “chỉ có nội dung THCS”.
