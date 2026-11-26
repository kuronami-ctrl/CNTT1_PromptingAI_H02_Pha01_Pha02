# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 08
- **Họ tên: NGUYỄN BÙI GIA BẢO**
- **Lớp: CNTT1**
- **Link repository Pha2:**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini): CHATGPT**

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt lịch khám ra JSON

**KET QUA AI**

```text
[
  {
    "ma_dich_vu": "TRAMRANG",
    "ngay_hen": "2026-12-17",
    "nguoi_lon": 2,
    "tre_em": 1,
    "khung_gio": "chieu",
    "ghi_chu": null
  },
  {
    "ma_dich_vu": "CAOVOI",
    "ngay_hen": "2027-01-06",
    "nguoi_lon": 3,
    "tre_em": 0,
    "khung_gio": null,
    "ghi_chu": "Một người bị tiểu đường"
  },
  {
    "ma_dich_vu": "TAYTRANG",
    "ngay_hen": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "khung_gio": "sang",
    "ghi_chu": "Một người dị ứng thuốc tê"
  }
]
```

**Link trò chuyện: https://chatgpt.com/share/6b07e553-ce94-83ec-900c-828afdfde37a**

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
BẢNG BÁO GIÁ – NHA KHOA NỤ CƯỜI
Dịch vụ: CAOVOI – Khám và cạo vôi răng

Số lượng khách: 6 người lớn, 2 trẻ em (7 tuổi, 11 tuổi) và 1 bé 4 tuổi.
Bước 1. Tiền người lớn
- Giá cạo vôi răng: 350.000 đồng/người.
- Số lượng: 6 người.
Phép tính:

6 × 350.000 = 2.100.000 đồng
Bước 2. Tiền trẻ em
- Trẻ 7 tuổi và 11 tuổi thuộc nhóm từ 6 đến 12 tuổi, tính 80% giá người lớn.
- Bé 4 tuổi được miễn phí.
Phép tính:
- Mỗi trẻ từ 6–12 tuổi: 350.000 × 80% = 280.000 đồng.
- Hai trẻ: 2 × 280.000 = 560.000 đồng.
- Bé 4 tuổi: 0 đồng.
Tổng tiền trẻ em:

560.000 + 0 = 560.000 đồng
Bước 3. Tiền dịch vụ
Tiền dịch vụ = Tiền người lớn + Tiền trẻ em.

Phép tính:

2.100.000 + 560.000 = 2.660.000 đồng
Bước 4. Giảm giá nhóm
- Nhóm có 6 người lớn, đạt điều kiện từ 5 người lớn trở lên.
- Mức giảm giá: 10% trên tổng tiền dịch vụ.
Phép tính:

2.660.000 × 10% = 266.000 đồng.

Tiền dịch vụ sau giảm:

2.660.000 - 266.000 = 2.394.000 đồng
Bước 5. Phụ thu chụp X-quang
- Số người chụp: 3 người.
- Phí mỗi phim: 150.000 đồng.
- Phí chụp X-quang không được giảm giá.
Phép tính:

3 × 150.000 = 450.000 đồng
Bước 6. Tổng tiền thanh toán
Tổng tiền = Tiền dịch vụ sau giảm + Phí chụp X-quang.

Phép tính:

2.394.000 + 450.000 = 2.844.000 đồng

KẾT QUẢ CUỐI CÙNG
TỔNG SỐ TIỀN KHÁCH HÀNG CẦN THANH TOÁN
2.844.000 đồng
Bằng chữ: Hai triệu tám trăm bốn mươi bốn nghìn đồng.
```

**Link trò chuyện: https://chatgpt.com/share/6b07e5c8-b1d0-83ec-9f4a-5120505bb3b4**

### b) Kiểm tra kết quả AI

Đúng

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
Bài làm của bạn cơ bản đã đúng hướng. Tuy nhiên, cần chỉnh một số điểm để Prompt Trạm 1 và câu lệnh viết tiếp hoạt động chính xác hơn.
a) Prompt Trạm 1 – Kết quả JSON dự kiến
{
  "loai_su_co": "tre_hen",
  "so_khach": 3,
  "so_lan_hen_bi_tre": 2,
  "tom_tat": "Gia đình 3 người phải chờ hơn 1 tiếng trong cả 2 lần hẹn."
}


b) Kiểm tra JSON đầu ra
1. Kiểm tra cấu trúc:
   - JSON hợp lệ.
   - Có đúng 4 trường.
   - loai_su_co là chuỗi.
   - so_khach là số nguyên.
   - so_lan_hen_bi_tre là số nguyên hoặc null.
   - tom_tat là chuỗi.
2. Kiểm tra nội dung:
   - Loại sự cố: tre_hen (đúng).
   - Số khách: 3 (đúng).
   - Số lần trễ hẹn: 2 (đúng).
   - Tóm tắt: Không quá 20 từ, đúng nội dung email.
c) Câu lệnh viết tiếp – Bản chỉnh sửa
Bạn nên viết rõ ràng hơn để AI không tự ý thay đổi nội dung email:
Hãy viết tiếp email từ đúng vị trí bị ngắt sau cụm từ "xin lỗi".

# YÊU CẦU
- Giữ nguyên toàn bộ nội dung email đã có.
- Không viết lại hoặc xóa nội dung phía trước.
- Nêu đúng mức đền bù được cung cấp trong JSON của Trạm 2.
- Không tự ý thay đổi hoặc đặt ra mức đền bù khác.
- Giọng điệu chân thành, lịch sự và chuyên nghiệp.
- Hoàn thành email với tổng độ dài dưới 150 từ.
- Chỉ viết phần nội dung tiếp nối, không giải thích.


Lưu ý: Câu lệnh ban đầu của bạn có cụm từ xin lỗi, nêu đúng mức đền bù trong JSON chưa rõ ràng về vị trí ngắt. Nên tách thành hai yêu cầu như bản chỉnh sửa để AI hiểu chính xác hơn.
```

**Link trò chuyện: https://chatgpt.com/share/6b07e789-dc20-83ec-b024-d5faf4ef29c7**

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
(Dán câu trả lời của AI vào đây (bấm nút Copy dưới câu trả lời) – xoá dòng này)
```

**Link trò chuyện: https://chatgpt.com/share/6b07e804-ea70-83ec-a367-aed46fff5336**
