<img width="1920" height="1080" alt="{17DBDE66-875B-47CB-A956-F5E7A880185B}" src="https://github.com/user-attachments/assets/8eff9b38-2775-4136-9ce8-71d8ac7679d6" /> 

<img width="1920" height="1080" alt="{4176590E-DCDD-48B4-9F1D-2F4905F950A7}" src="https://github.com/user-attachments/assets/6d3f8691-9678-46d4-97a3-2f88028e7394" />


# VisionBox — Hướng dẫn sử dụng

VisionBox là công cụ **OCR + dịch truyện tranh** (webtoon / manga / manhwa / manhua) bằng Google Gemini. Chỉ cần kéo ảnh vào, chọn ngôn ngữ, bấm nút — tool tự quét chữ trong bóng thoại rồi dịch sang ngôn ngữ bạn muốn.

> Inspired by MoeTruyen • Customized by Maditor

---

## 1. Chuẩn bị: Lấy API Key

Tool dùng Google Gemini nên cần API Key miễn phí từ Google:

1. Bấm nút **🔑 Get key** cạnh ô nhập API Key (góc trên bên phải màn hình) — nút này sẽ mở trang `https://aistudio.google.com/api-keys` để bạn tạo key.
2. Đăng nhập bằng tài khoản Google, tạo key mới, copy lại.
3. Dán vào ô **Gemini API Key** trong tool.
4. Bấm biểu tượng 👁 cạnh ô để hiện/ẩn key khi cần kiểm tra lại.

API Key sẽ được **lưu tự động** lại trên máy, không cần nhập lại mỗi lần mở tool.

⚠️ Không chia sẻ API Key của bạn cho người khác — ai có key đó dùng thì tính vào quota/tài khoản Google của bạn.

---

## 2. Chọn Model

Ở góc trên bên trái có ô **Model** để chọn model Gemini sẽ dùng để quét/dịch:

- Có sẵn vài model phổ biến (flash, flash-lite...) — model càng "flash-lite" thì càng nhanh/rẻ nhưng độ chính xác có thể thấp hơn model đầy đủ.
- Chọn **"Other model..."** nếu muốn tự gõ tên một model Gemini khác không có trong danh sách (ví dụ model mới Google vừa ra mà tool chưa kịp cập nhật).

---

## 3. Chọn ngôn ngữ

### Source language (ngôn ngữ gốc của ảnh)

| Lựa chọn   | Ngôn ngữ                | Cách đọc                                    |
|------------|-------------------------|---------------------------------------------|
| **Webtoon** | Hàn, Anh, Trung         | Từ trên xuống, trái sang phải               |
| **Manga**  | Nhật, Anh | Từ trên xuống, **phải sang trái** (chuẩn manga) |

👉 Ba lựa chọn đầu (Hàn/Anh/Trung) dành cho **webtoon** (đọc dọc, trái→phải). Riêng **Manga** dành cho định dạng đọc theo kiểu Nhật (phải→trái), và xử lý được cả nội dung tiếng Anh xen trong manga.

Chọn đúng loại này rất quan trọng vì nó quyết định **thứ tự đọc bóng thoại** khi OCR — chọn sai sẽ khiến câu thoại bị xáo trộn thứ tự.

### Translate to (ngôn ngữ muốn dịch sang)

Chọn ngôn ngữ đích: Vietnamese / English / Korean.

### Skip SFX

Bật công tắc này nếu muốn tool **bỏ qua các từ tượng thanh/hiệu ứng âm thanh** (SFX) như tiếng bước chân, tiếng va chạm, tiếng gió... (dạng chữ cách điệu vẽ ngoài khung thoại) — chỉ lấy đúng lời thoại trong bóng thoại/hộp thoại thật sự.

---

## 4. Thêm ảnh

Có 2 cách:

- Bấm **"+ Add images (max 100)"** để chọn ảnh từ máy (chọn được nhiều ảnh cùng lúc).
- Hoặc **kéo–thả** ảnh trực tiếp vào vùng làm việc.

Giới hạn tối đa **100 ảnh** mỗi lần làm việc. Ảnh trùng tên + trùng dung lượng với ảnh đang có sẵn trong danh sách sẽ tự động bị bỏ qua để tránh nhân đôi.

---

## 5. Xử lý ảnh

Mỗi ảnh sau khi thêm vào sẽ hiện thành một khối riêng gồm: ảnh gốc, cột **OCR** và cột **Translation**. Trên mỗi ảnh có các nút:

- **OCR** — quét chữ riêng ảnh này.
- **Translate** — dịch riêng ảnh này (cần OCR trước, nếu chưa có văn bản gốc thì tool sẽ nhắc chạy OCR trước).
- **Edit mode** — cho sửa tay trực tiếp nội dung OCR/dịch nếu Gemini quét/dịch chưa chuẩn. Bấm lại (khi đang ở chế độ sửa nút sẽ đổi thành "Done") để lưu lại.
- **✕** — xoá riêng ảnh đó khỏi danh sách.
- Biểu tượng **⤢** ở góc ảnh — chỉnh kích thước xem trước của riêng ảnh đó (kéo thanh trượt hoặc kéo góc dưới-phải của ảnh); bấm nút reset để về kích thước mặc định.

### Xử lý hàng loạt (batch)

Ở thanh công cụ trên có 4 nút xử lý toàn bộ ảnh đã thêm:

- **OCR all** — quét chữ tất cả ảnh.
- **Translate all** — dịch tất cả ảnh đã có kết quả OCR (ảnh chưa OCR sẽ bị bỏ qua).
- **OCR + Translate all** — làm cả 2 bước liên tiếp cho từng ảnh.
- **Clear all** — xoá sạch toàn bộ ảnh (có hỏi xác nhận trước khi xoá).

Khi đang chạy hàng loạt, thanh tiến trình sẽ hiện số ảnh đã xong/tổng số. Bấm nút **×** trên thanh tiến trình để **dừng sau khi ảnh hiện tại xử lý xong** (không hủy giữa chừng ảnh đang chạy).

---

## 6. Xử lý khi gặp giới hạn tốc độ (lỗi 429)

Nếu gọi API quá nhanh/quá nhiều, Google có thể trả lỗi **429 (rate limit)**. Khi đó tool sẽ **tự động chờ và thử lại**, tối đa 6 lần, mỗi lần cách nhau 10 giây (tổng tối đa khoảng 1 phút), kèm thông báo nhỏ báo đang chờ.

Nếu không muốn đợi hết thời gian đó, một nút **"Stop retry"** sẽ xuất hiện cạnh trạng thái của ảnh đang bị chờ — bấm vào, xác nhận, tool sẽ dừng ngay lập tức và dừng luôn toàn bộ các ảnh còn lại trong hàng chờ xử lý.

---

## 7. Bảng tổng hợp (All OCR / All translations)

Sau khi có ít nhất 1 ảnh được xử lý, phía dưới sẽ xuất hiện 2 khung tổng hợp toàn bộ văn bản OCR và toàn bộ bản dịch của **tất cả** ảnh gộp lại — tiện để copy nguyên khối đi dùng chỗ khác. Mỗi khung có:

- **⟲ (Reload)** — nạp lại nội dung tổng hợp mới nhất từ tất cả ảnh (dùng khi bạn vừa sửa tay nội dung ở từng ảnh riêng lẻ và muốn cập nhật lại bảng tổng hợp).
- **Export** — xuất nội dung ra file **.txt** hoặc **.docx**, tool sẽ mở hộp thoại chọn nơi lưu file.
- **Edit mode** — sửa tay trực tiếp trên bảng tổng hợp, bấm "Done" để lưu.
- **Copy** — copy toàn bộ nội dung khung đó vào clipboard.

---

## 8. Nút danh sách ảnh (nổi, góc màn hình)

Nút tròn ☰ nổi trên màn hình mở ra bảng danh sách nhanh tất cả ảnh đã thêm, có chấm màu báo trạng thái (đang xử lý / xong / lỗi) — bấm vào 1 ảnh trong danh sách để cuộn nhanh tới ảnh đó. Bên dưới danh sách có 2 nút **↑ / ↓** để cuộn nhanh lên đầu/xuống cuối trang.

**Di chuyển nút này:** nhấn giữ và kéo nút tròn tới vị trí khác trên màn hình nếu nó đang che mất phần bạn cần thao tác — chỉ bấm nhẹ (không kéo) vẫn mở/đóng bảng danh sách bình thường. Vị trí sau khi kéo được nhớ lại cho lần mở tool sau.

---

## 9. Tự động lưu tạm (project autosave)

Để tránh mất công khi lỡ tắt tool giữa chừng, VisionBox tự lưu lại **kết quả OCR và bản dịch** (không lưu ảnh gốc để tránh file lưu quá nặng) mỗi khi:

- Thêm ảnh, xoá ảnh
- OCR/dịch xong một ảnh hoặc cả loạt
- Sửa tay nội dung

Ngoài ra cứ mỗi **5 phút** tool sẽ tự lưu lại một lần kèm thông báo nhỏ "Saving project..." → "Project saved." để bạn yên tâm là đang được lưu.

**Lưu ý quan trọng:** vì không lưu ảnh gốc, nên khi mở lại tool, ảnh sẽ **không tự hiện lại**. Muốn khôi phục kết quả OCR/dịch đã lưu, bạn cần **kéo/thả lại đúng những ảnh cũ đó** (cùng tên file, cùng dung lượng) — tool sẽ tự nhận ra và điền lại kết quả cũ ngay, không cần chạy OCR/dịch lại từ đầu. Lúc thêm ảnh vào, tool sẽ báo rõ ảnh nào được khôi phục thành công và ảnh nào từ phiên trước vẫn chưa được thêm lại.

---

## 10. Một vài lưu ý chung

- Cài đặt Model / ngôn ngữ / API Key được lưu tự động, không cần cấu hình lại mỗi lần mở tool.
- Nên tránh chạy quá nhiều ảnh liên tục với tài khoản API miễn phí để hạn chế gặp lỗi giới hạn tốc độ (429).
- Nếu OCR/dịch ra sai sót (tên riêng, thuật ngữ...), dùng **Edit mode** ở từng ảnh hoặc ở bảng tổng hợp để sửa tay trước khi export.
- Mọi thao tác quan trọng (xoá ảnh, xoá tất cả) đều có hộp thoại xác nhận trước khi thực hiện, tránh bấm nhầm mất dữ liệu.
