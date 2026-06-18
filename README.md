# Ngày 16 — Student Lab (V4)

Phiên bản này giữ đúng nguyên tắc tối giản:

- **1 file `README` để điều hướng**
- **1 file cho Lab 1**
- **1 file cho Lab 2**

Ngoài ra, ở Lab 2 giảng viên sẽ gửi kèm thêm một **tài liệu tham khảo ngoài repo**:

- `Strategyn_JTBD_Playbook.pdf`

Quy tắc xuyên suốt: **không có bằng chứng = không có nhận định.**

---

## Hôm nay cần làm gì?

Trong repo nộp bài, bạn chỉ cần dùng 3 file:

```text
Day16-MãHọcViên-HọVàTên/
├── README.md
└── worksheet/
    ├── 01-case-analysis.md
    └── 02-jtbd-project-analysis.md
```

- `README.md`: file điều hướng + thông tin nộp bài
- `worksheet/01-case-analysis.md`: **vừa là guide, vừa là worksheet, vừa là file nộp của Lab 1**
- `worksheet/02-jtbd-project-analysis.md`: **vừa là guide, vừa là worksheet, vừa là file nộp của Lab 2**

Ngoài 3 file trong repo, ở **Lab 2** bạn cần mở thêm:

- `Strategyn_JTBD_Playbook.pdf`  
  Đây là **companion reference** giảng viên gửi kèm để bạn tra framework, ví dụ, và 8 bước của `job map`.  
  **Không bắt buộc** upload file PDF này lên repo cá nhân.

---

## Nộp bài thế nào?

### Tên kho GitHub

Cú pháp: **`Day16-MãHọcViên-HọVàTên`**  
Ví dụ: `Day16-A20-00045-NguyenVanA`

Mỗi học viên có 1 kho công khai riêng.

### Cần nộp gì hôm nay?

1. Điền đầy đủ `worksheet/01-case-analysis.md`
2. Điền đầy đủ `worksheet/02-jtbd-project-analysis.md`
3. Điền `README.md` gốc kho theo mẫu bên dưới
4. Nộp link repo qua LMS

### README mẫu ở repo nộp bài

```markdown
# Day16-A20-XXXXX-HoVaTen

## Thông tin học viên

- Mã học viên: A20-XXXXX
- Họ tên: Nguyễn Văn A
- Track: AI Product Strategy

## File nộp

- 🎯 [Lab 1 — Case Analysis](./worksheet/01-case-analysis.md)
- 🎯 [Lab 2 — JTBD Project Analysis](./worksheet/02-jtbd-project-analysis.md)

## Ghi chú

- Tài liệu tham khảo dùng cho Lab 2: `Strategyn_JTBD_Playbook.pdf` (giảng viên gửi kèm, không bắt buộc đưa vào repo).
```

---

## Người chấm sẽ nhìn gì trong Lab 1?

Người chấm sẽ nhìn 4 thứ trước:

1. **Bạn có 3-5 bằng chứng chốt đủ sắc không?**
2. **Bạn có viết được 4 nhận định bắt buộc không?**
3. **Bạn có nói được điều gì đã thay đổi vĩnh viễn không?**
4. **Verdict cuối của bạn có sắc hơn sau khi share trong bàn không?**

Nếu 4 điểm này rõ, bài sẽ mạnh hơn rất nhiều so với kiểu chỉ kể lại câu chuyện case.

---

## Người chấm sẽ nhìn gì trong Lab 2?

Người chấm sẽ nhìn 5 thứ trước:

1. **Bạn có xác định đúng `job executor` không?**
2. **`Core JTBD` của bạn có solution-free và đủ sắc không?**
3. **Bạn có viết được 3 `job stories` đủ cụ thể theo tình huống không?**
4. **Bạn có chỉ ra đúng bước đau nhất trong workflow và `AI leverage point` không?**
5. **Bạn có nói rõ assumption nào còn phải validate, thay vì giả vờ đã biết chắc không?**

Lab 2 mạnh khi nó giúp nhóm **bớt nhảy vào feature list quá sớm** và quay về câu hỏi gốc:
**user thực sự đang cố hoàn thành job gì, trong hoàn cảnh nào, và AI nên can thiệp ở đâu cho đáng tiền?**

---

## Cách dùng AI cho đúng

- AI chỉ nên giúp bạn **tìm nguồn, gom số, dựng nháp câu chữ**.
- Bạn vẫn phải **mở URL nguồn**, tự kiểm số liệu, và tự chốt verdict.
- Đừng để AI viết thay phần "điều gì đã thay đổi vĩnh viễn" cho bạn.
- Với Lab 2, đừng để AI **bịa `job`, bịa người dùng, hoặc nhảy thẳng sang list tính năng** khi bạn còn chưa làm rõ workflow.

---

## Ghi nhớ trước khi mở worksheet

Làm theo thứ tự này:

1. [01-case-analysis.md](./worksheet/01-case-analysis.md)
2. [02-jtbd-project-analysis.md](./worksheet/02-jtbd-project-analysis.md)

Toàn bộ hướng dẫn làm bài, danh sách đầu ra bắt buộc, gợi ý, share trong bàn, và checklist nộp bài đều nằm trong chính 2 file đó.
