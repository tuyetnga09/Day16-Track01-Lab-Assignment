# Lab 2 — JTBD Project Analysis (bản hoàn thiện)

**Người làm:** Phạm Thị Tuyết Nga — 2A202600877  
**Track:** AI Product Strategy  
**Ngày:** 19/06/2026  
**Dự án / sản phẩm:** Nền tảng *trung tâm tri thức nội bộ* — tập trung tài liệu của tập đoàn + chatbot hỏi-đáp có trích dẫn nguồn.

> Quy tắc: không rõ job thì đừng bàn feature. Phân tích này nối tiếp Lab 1 — nơi kết luận moat phải dịch sang *trích dẫn audit-được + tích hợp sâu dữ liệu nội bộ*, thứ Copilot/Gemini phổ thông làm chưa tới.

---

## 1. Project slice + Market context

### 1.1. Lát cắt đã khoanh (Bước 0)

| Điểm khoanh | Nội dung |
|---|---|
| **1 nhóm người dùng** | Nhân viên tuyến đầu (CSKH / vận hành nghiệp vụ) — người trực tiếp tra quy định để xử lý công việc |
| **1 hoàn cảnh** | Đang xử lý một ca thực tế, cần biết *quy định/quy trình nội bộ nào áp dụng* — thường gấp, có khách hoặc deadline đứng chờ |
| **1 job cốt lõi** | Xác nhận đúng quy định áp dụng cho tình huống đang xử lý, đủ nhanh và đủ chắc để hành động |
| **1 workflow** | Hiểu ca → tìm văn bản đúng → chắc là bản còn hiệu lực → áp dụng → đóng ca |

- **Dự án của nhóm tôi là:** trung tâm tri thức nội bộ + chatbot hỏi-đáp có trích dẫn.
- **Lát cắt tôi chọn:** nhân viên tuyến đầu tra cứu quy định *ngay trong lúc xử lý một ca gấp*.
- **Vì sao chọn lát cắt này:** đây là tình huống job xuất hiện *dày đặc, có áp lực thời gian và rủi ro làm sai chính sách* — nơi giá trị "nhanh + có dẫn chứng để dám hành động" được cảm nhận rõ nhất.

### 1.2. Market context

1. **Ai đang gặp vấn đề:** nhân viên tuyến đầu trong tập đoàn lớn, nơi quy định/quy trình nhiều, rải rác, hay cập nhật.
2. **Hoàn cảnh:** đang phục vụ khách hoặc xử lý nghiệp vụ, gặp ca ngoại lệ/lần đầu, cần căn cứ ngay.
3. **Giải pháp thay thế hiện tại:** hỏi đồng nghiệp/sếp, tự lục SharePoint/intranet bằng keyword, hỏi ChatGPT chung, hoặc đoán theo trí nhớ.
4. **Vì sao bây giờ đáng giải:** LLM khiến hỏi-đáp-có-trích-dẫn trên tài liệu nội bộ trở nên khả thi & "đủ tốt"; đồng thời (Lab 1) Big Tech đang bundle tính năng này, nên phải thắng bằng độ tin & tích hợp sâu, không phải bằng "có chatbot".

> **Tóm tắt market context:** Nhân viên tuyến đầu phải ra quyết định đúng-quy-định dưới áp lực thời gian, trong khi tri thức nội bộ phân mảnh và hay thay đổi. Họ đang chắp vá bằng cách hỏi người và lục tay — chậm, không nhất quán, rủi ro áp dụng bản đã hết hiệu lực.

---

## 2. Job Executor + Core JTBD

### 2.1. Job executor

- **Job executor:** **Nhân viên tuyến đầu (CSKH / vận hành nghiệp vụ)** — người trực tiếp tra cứu để xử lý ca.
- **Vì sao là người này (không phải buyer):** IT/lãnh đạo khối là người *mua*, nhưng người *trực tiếp "thuê" giải pháp để hoàn thành job* là nhân viên đang cần căn cứ ngay tại chỗ. Job thành/bại đo ở họ.

### 2.2. Core JTBD

> **Xác nhận đúng quy định/thông tin nội bộ áp dụng cho tình huống đang xử lý, đủ nhanh và đủ chắc để hành động ngay tại chỗ.**

**Tự kiểm 3 tiêu chí:**
- ✅ Bỏ tool đi job vẫn còn (nhân viên vẫn phải tra đúng quy định để làm việc).
- ✅ Không có tên sản phẩm / AI / chatbot / app / màn hình trong câu.
- ✅ Mô tả điều user muốn hoàn thành (ra quyết định đúng & tự tin), không phải thứ product làm.

---

## 3. Ba Job Stories

| # | When (trigger) | I want to (motivation) | So I can (outcome) | Story cho thấy điều gì |
|---|---|---|---|---|
| JS1 | đang trên điện thoại với khách, gặp ca ngoại lệ về chính sách (hoàn tiền/bảo hành) | tìm ngay điều khoản áp dụng và biết nó nằm ở văn bản nào | trả lời dứt khoát mà không hứa sai chính sách | job xuất hiện realtime, áp lực cao → tốc độ + dẫn chứng là sống còn |
| JS2 | mới onboarding, lần đầu gặp một nghiệp vụ | nắm đúng các bước bắt buộc và ngoại lệ của quy trình | làm đúng ngay từ lần đầu, không phải đi hỏi vòng quanh | đối thủ thật là "hỏi đồng nghiệp" → phải nhanh và đáng tin hơn người |
| JS3 | nghe quy định vừa được cập nhật | chắc mình đang đọc đúng phiên bản mới nhất | không áp dụng nhầm chính sách đã hết hiệu lực | "đúng phiên bản/hiệu lực" là pain riêng, Big Tech generic hay bỏ sót |

---

## 4. Current Alternatives + JTBD Lite Map

### 4.1. Current alternatives

| Alternative | User thuê nó để làm gì | Làm tốt gì | Fail ở đâu | Switching cost |
|---|---|---|---|---|
| Hỏi đồng nghiệp / sếp | lấy câu trả lời kèm ngữ cảnh nhanh | có kinh nghiệm, hiểu ca | làm phiền người khác, không phải lúc nào cũng có, tam sao thất bản | Thấp |
| Lục SharePoint/intranet bằng keyword | tự tìm văn bản gốc | luôn sẵn, là nguồn chính thống | kết quả nhiễu, không biết bản mới/cũ, tốn thời gian | Thấp |
| ChatGPT / Gemini chung | hỏi nhanh cho tiện | diễn đạt mượt | không có data nội bộ, dễ bịa, không trích nguồn nội bộ, rủi ro bảo mật | Thấp |
| Đoán theo trí nhớ / không làm gì | xử lý cho nhanh | nhanh nhất | rủi ro sai chính sách cao nhất | Thấp |

> **Nếu project biến mất hôm nay, user quay về:** chủ yếu **hỏi đồng nghiệp** + **lục keyword** — nhanh nhưng chậm hơn, kém nhất quán và dễ dùng nhầm bản cũ.

### 4.2. JTBD Lite Map (workflow xác nhận quy định áp dụng)

| Step | User đang cố làm gì | Hôm nay dùng gì | Friction / pain | Mức đau |
|---|---|---|---|---|
| Define | hiểu ca cần loại quy định nào | tự suy luận | đôi khi không biết mình cần tra gì | Med |
| **Locate** | **tìm đúng văn bản/đoạn áp dụng** | **keyword search / hỏi người** | **nhiễu kết quả, mất thời gian, dễ trật** | **High** |
| Prepare | gom & đối chiếu các điều khoản liên quan | mở nhiều file cùng lúc | rời rạc, dễ sót điều kiện kèm theo | Med |
| **Confirm** | **chắc đây là bản mới nhất, đúng ngữ cảnh** | **đoán theo trí nhớ / hỏi lại** | **không có dấu hiệu phiên bản/hiệu lực rõ** | **High** |
| Execute | áp dụng / trả lời khách | nói/nhập trực tiếp | nếu bước trên sai thì sai theo | Med |
| Monitor | soát ngoại lệ, điều kiện kèm | tự nhớ | dễ bỏ sót case đặc thù | Med |
| Modify | điều chỉnh cho ca đặc thù | hỏi cấp trên | chậm, phụ thuộc người | Low/Med |
| Conclude | đóng ca, lưu căn cứ đã dùng | ghi tay / bỏ qua | thiếu vết để audit về sau | Low/Med |

**Bước đau nhất #1:** **Locate** — tìm đúng đoạn trong kho phân mảnh.
**Bước đau nhất #2:** **Confirm** — chắc chắn đang dùng bản còn hiệu lực.

> **Vì sao đây là nơi đáng chú ý nhất:** Đa số thời gian và rủi ro dồn vào Locate + Confirm. Sai ở hai bước này dẫn thẳng tới *áp dụng sai chính sách* — hậu quả nặng nhất trong môi trường tuân thủ. Đây cũng đúng JTBD lõi: "nhanh + chắc".

---

## 5. AI Leverage Point + Product Hypothesis

### 5.1. AI leverage point

| Step | AI giúp bằng cách nào | Vì sao AI hợp ở đây | Rủi ro chính |
|---|---|---|---|
| **Locate** | hiểu ngữ nghĩa câu hỏi → trả lời kèm **trích dẫn đúng đoạn/văn bản nguồn** | search ngữ nghĩa + tổng hợp là đúng thế mạnh LLM; thay thế trực tiếp việc lục keyword & hỏi người | AI bịa hoặc trỏ sai đoạn → mất niềm tin |
| **Confirm** | gắn **metadata phiên bản/hiệu lực**, cảnh báo bản cũ, luôn dẫn nguồn để user tự kiểm | đây là điểm Big Tech generic làm yếu → cơ hội tạo moat | nếu metadata hiệu lực sai → user áp dụng nhầm |

> **AI leverage point quan trọng nhất:** trả lời ở bước **Locate** *bắt buộc kèm trích dẫn đoạn nguồn*, và ở **Confirm** *gắn cảnh báo phiên bản/hiệu lực*.
> **Vì sao không phải bước khác:** Execute/Conclude pain thấp hơn và đã có cách làm chấp nhận được; nhồi AI vào đó không đổi được kết quả job.

### 5.2. Product hypothesis

> **Nếu** giúp **nhân viên tuyến đầu** xác nhận đúng quy định ở bước **Locate + Confirm**, **bằng cách** trả lời có *trích dẫn đoạn nguồn* + *cảnh báo phiên bản hiệu lực*, **thì** họ sẽ chuyển từ *"hỏi đồng nghiệp / lục keyword"* sang dùng sản phẩm, **vì** nhanh hơn và **chắc hơn** — dám hành động ngay mà không sợ áp dụng sai chính sách.

**Tín hiệu sớm nếu hypothesis đúng:**
1. Tỷ lệ câu trả lời được user mở link trích dẫn để xác nhận tăng (tin & dùng được).
2. Giảm số lần "hỏi đồng nghiệp/sếp" cho cùng loại nghiệp vụ; thời gian xử lý ca giảm.

---

## 6. Assumptions to Validate + Verdict

### 6.1. Assumptions

| # | Assumption | Vì sao rủi ro | Bằng chứng đang có | Validate tiếp thế nào |
|---|---|---|---|---|
| A1 | Đúng job executor là nhân viên tuyến đầu (không phải knowledge manager) | nếu sai, cả workflow vẽ sai | quan sát định tính | phỏng vấn 5–7 nhân viên tuyến đầu |
| A2 | Pain Locate/Confirm đủ đau & đủ thường xuyên | nếu hiếm, không đáng làm | giả định | đo tần suất tra cứu/ca, thời gian trung bình mỗi lần |
| A3 | User sẽ bỏ thói quen "hỏi đồng nghiệp" | thói quen xã hội rất dính | chưa có | thử nghiệm có giám sát, đo tỷ lệ chuyển đổi hành vi |
| A4 | AI trích dẫn đủ chính xác để user tin | citation sai làm sập niềm tin | chưa đo | đo precision của trích dẫn trên bộ câu hỏi thật |
| A5 | User đủ tin để hành động dựa trên câu trả lời trong môi trường tuân thủ | rủi ro pháp lý/chính sách | chưa có | A/B có vs không có cảnh báo hiệu lực; khảo sát mức độ tin |

### 6.2. Assumption nguy hiểm nhất

> **A4 + A5 — niềm tin vào trích dẫn.** Nếu user không tin trích dẫn đủ để bỏ việc đọc bản gốc / hỏi người, toàn bộ hypothesis sập. Đây *cũng chính là moat* đã chỉ ra ở Lab 1: thắng Big Tech không bằng "có chatbot" mà bằng *độ tin & tính audit-được của câu trả lời trên dữ liệu nội bộ*.

### 6.3. Verdict cuối (version nộp)

- **Job executor:** nhân viên tuyến đầu (CSKH / vận hành) trực tiếp tra quy định để xử lý ca.
- **Core JTBD:** xác nhận đúng quy định áp dụng cho tình huống đang xử lý, đủ nhanh và đủ chắc để hành động ngay.
- **2 bước đau nhất:** Locate (tìm đúng đoạn) + Confirm (đúng phiên bản/hiệu lực).
- **AI leverage point chính:** trả lời ở Locate kèm trích dẫn đoạn nguồn + cảnh báo hiệu lực ở Confirm.
- **Product hypothesis:** giúp Locate + Confirm có dẫn chứng & cảnh báo phiên bản → user rời "hỏi người/lục keyword" vì nhanh hơn và chắc hơn.
- **Assumption cần validate đầu tiên:** A4 — độ chính xác & độ tin của trích dẫn (đo precision citation trên câu hỏi thật).

---

*Câu hỏi khó tự kiểm (theo playbook): nếu bỏ AI đi, job "xác nhận đúng quy định để dám hành động" vẫn còn — nên đây là job thật, không phải chỗ nhét AI. AI chỉ là cách hoàn thành job nhanh & chắc hơn ở Locate + Confirm.*
