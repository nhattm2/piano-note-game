# 🎹 Đoán Nốt Nhạc

Web game giúp người học piano luyện đọc tên nốt trên khuông nhạc (khóa Sol, khóa Fa).
Chỉ gồm một file `index.html`: không cần build, không cần thư viện.

## Tính năng

- **3 chế độ chơi:** ⏱️ 60 giây (sai bị trừ 3 giây), ❤️ Sinh tồn (3 mạng), 🧘 Luyện tập (không áp lực)
- **Khóa nhạc:** khóa Sol, khóa Fa hoặc trộn cả hai
- **Độ khó:** Dễ (nốt nằm trong khuông), Vừa (thêm 1 dòng kẻ phụ), Khó (nhiều dòng kẻ phụ), hoặc *Tăng dần* theo cấp
- **Tên nốt:** Đô Rê Mi hoặc C D E
- Phát âm thanh piano (Web Audio), highlight vị trí nốt trên bàn phím đàn
- Trả lời sai sẽ hiện mẹo nhớ (ví dụ: dòng kẻ khóa Sol là Mi – Sol – Si – Rê – Fa), và nốt sai sẽ được hỏi lại sau đó
- Có chuỗi combo 🔥, thưởng điểm khi trả lời nhanh ⚡, lên cấp, pháo giấy, lưu kỷ lục
- Trả lời bằng bàn phím máy tính: `C D E F G A B` hoặc `1`–`7`; `Esc` để kết thúc lượt, `Enter` để bắt đầu

## Chạy thử trên máy

```bash
cd piano-note-game
python3 -m http.server 8000
# mở http://localhost:8000
```

(Mở trực tiếp file `index.html` bằng trình duyệt cũng chạy được.)

## Deploy lên GitHub Pages

```bash
cd piano-note-game
git init
git add .
git commit -m "Đoán Nốt Nhạc game"
git branch -M main
git remote add origin https://github.com/<username>/piano-note-game.git
git push -u origin main
```

Sau đó vào repo trên GitHub, chọn **Settings → Pages → Build and deployment**:
- Source: **Deploy from a branch**
- Branch: **main**, thư mục **/ (root)**, rồi bấm **Save**

Khoảng 1 phút sau, game sẽ chạy tại `https://<username>.github.io/piano-note-game/`.
