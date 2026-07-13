# 🎬 Reel Studio — Trình dựng reel bất động sản

Web app chạy **hoàn toàn trong trình duyệt** để ghép nhiều clip dọc thành một reel quảng cáo cao cấp: chuyển cảnh mượt, chữ vàng ánh kim + trắng theo phong cách sang trọng, xuất ra file video đăng thẳng Facebook / YouTube / TikTok.

Clip của bạn **không được upload lên bất kỳ máy chủ nào** — mọi xử lý diễn ra ngay trên máy.

## ✨ Tính năng

- Kéo thả nhiều clip cùng lúc, mỗi clip là một cảnh; đổi thứ tự / xoá dễ dàng
- Nhập chữ cho từng cảnh: tiêu đề (vàng, in hoa) + dòng phụ (trắng)
- 2 kiểu chữ: **Chữ dưới** (cảnh nội dung) và **Tên dự án + CTA** (cảnh mở/đóng)
- Xem trước trực tiếp: phát, tua, chuyển cảnh crossfade, chữ fade in/out
- Tuỳ chỉnh: màu nhấn, độ dài chuyển cảnh, lớp tối đáy, khung 9:16 / 1:1 / 16:9
- Lưu / nạp bộ chữ để tái dùng cho dự án sau *(khi chạy trong môi trường hỗ trợ lưu trữ)*
- Xuất reel kèm âm thanh ngay trong trình duyệt

## 🚀 Dùng thử

Mở **[Reel Studio](https://<TÊN-GITHUB>.github.io/<TÊN-REPO>/)** *(cập nhật link sau khi bật GitHub Pages)*, hoặc tải file `index.html` về và mở bằng trình duyệt.

### Ba bước

1. **Thêm clip** — kéo các clip vào (dạng dọc 9:16 cho đẹp nhất)
2. **Nhập chữ** — chọn cảnh rồi gõ tiêu đề + dòng phụ
3. **Xuất reel** — bấm nút, tải file về

## 📤 Định dạng xuất

App xuất ra `.webm` (Facebook / YouTube nhận thẳng). Với **TikTok**, nên đổi sang `.mp4`:

```bash
ffmpeg -i reel.webm -c:v libx264 -crf 20 -c:a aac -movflags +faststart reel.mp4
```

## 🌐 Bật GitHub Pages (để có link chạy trực tiếp)

Sau khi push repo lên GitHub:

1. Vào **Settings → Pages**
2. Mục **Source**: chọn nhánh `main`, thư mục `/ (root)`
3. Lưu lại → sau ~1 phút app sẽ chạy tại `https://<tên-github>.github.io/<tên-repo>/`

## 🛠 Công nghệ

HTML + CSS + JavaScript thuần (không cần build). Xử lý video/âm thanh bằng Canvas API, WebAudio và MediaRecorder. Font: Playfair Display + Be Vietnam Pro.

## 📄 Giấy phép

[MIT](LICENSE)
