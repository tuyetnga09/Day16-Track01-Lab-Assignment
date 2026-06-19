# Lab 1 — Case Analysis (bản hoàn thiện)

**Người làm:** Phạm Thị Tuyết Nga — 2A202600877  
**Track:** AI Product Strategy  
**Ngày:** 18/06/2026  
**Case phân tích:** Nền tảng *trung tâm tri thức nội bộ* — tập trung tài liệu của tập đoàn + chatbot hỏi-đáp trên kho tài liệu đó, trả lời kèm trích dẫn nguồn rõ ràng.  
**AI shock:** Big Tech bundle tính năng "chat with your documents + citations" ngay vào bộ công cụ doanh nghiệp đã trả tiền (Microsoft 365 Copilot, Google Gemini/NotebookLM, ChatGPT Enterprise).

> Quy tắc: không có bằng chứng = không có nhận định. Các mốc/số dưới đây là sự kiện công khai — cần mở URL gốc xác minh trước khi nộp; chỗ chưa chắc đã đánh dấu ⚠️.

---

## Phần 1 — Thu thập thông tin

### 1.1. Case trước AI

| Hạng mục | Nội dung |
|---|---|
| **Sản phẩm là gì** | Nền tảng trung tâm tri thức nội bộ: gom toàn bộ tài liệu của tập đoàn (quy định, quy trình, hợp đồng, biểu mẫu, tài liệu kỹ thuật) về một nơi + chatbot hỏi-đáp trên chính kho đó, trả lời kèm **trích dẫn nguồn** (chỉ rõ lấy từ tài liệu nào, đoạn nào). |
| **User là ai** | Nhân viên trong tập đoàn (vận hành, nhân sự, pháp chế, kỹ thuật, CSKH…) cần tra cứu nhanh tài liệu/quy định để làm việc. Người trả tiền là IT / lãnh đạo khối; người dùng cuối là nhân viên. |
| **Họ trả tiền cho cái gì** | (1) Tìm kiếm **thuận lợi, nhanh** trong núi tài liệu;<br>(2) câu trả lời có **dẫn chứng rõ** để dám tin, dám hành động, giảm rủi ro làm sai quy định;<br>(3) gom tri thức rải rác về một mối, bớt phải hỏi nhau / lục tay. |
| **Sản phẩm thắng nhờ gì** | Làm được thứ nội bộ khó tự dựng: RAG trên dữ liệu nội bộ + trích dẫn + phân quyền + bảo mật; tìm kiếm **hiểu ngữ nghĩa** tốt hơn hẳn search keyword truyền thống (SharePoint/intranet cũ). |
| **JTBD lõi** | *"Giúp tôi tìm đúng thông tin trong kho tài liệu nội bộ thật nhanh, và cho tôi bằng chứng đáng tin để tôi dám hành động ngay."* |

### 1.2. AI shock — mốc Big Tech ra tính năng tương tự

| Mốc | Sự kiện | Vì sao là "shock" với sản phẩm này |
|---|---|---|
| 08/2023 | **ChatGPT Enterprise** ra mắt: hỏi-đáp trên dữ liệu công ty + bảo mật doanh nghiệp, không train trên data khách hàng | Phá lý do "chỉ specialist vendor mới đủ an toàn cho data nội bộ" |
| 11/2023 | **Microsoft 365 Copilot** GA, add-on ~$30/user/tháng trên tập khách hàng M365 sẵn có | Đối thủ không "bán mới" — chỉ bật switch trên user mình đang phục vụ |
| 2023 → nay | **Google NotebookLM** + **Gemini trong Workspace**: hỏi đáp trên tài liệu của bạn, **có trích dẫn nguồn** | Đúng y hệt tính năng lõi sản phẩm đang bán, nay đi kèm sẵn |
| Liên tục | RAG / "chat-with-docs" thành **commodity**: LangChain, LlamaIndex, API embedding ngày càng rẻ | Rào cản kỹ thuật từng là moat đã sụp — ai cũng dựng được bản "đủ tốt" |

### 1.3. Tác động quan sát được

| Khía cạnh | Tác động |
|---|---|
| **Adoption / usage** | Tính năng "chat tài liệu + trích dẫn" có sẵn ngay trong công cụ user *đã* trả tiền → user hỏi "vì sao còn cần một app riêng?" |
| **Pricing** | Bị ép giá: Big Tech bundle tính năng lõi gần như miễn phí / giá thấp so với giá specialist |
| **Doanh thu / ARR (rủi ro)** | Áp lực churn & khó upsell khi khách nói "đã có Copilot rồi" — *điền số nội bộ thực tế nếu có* |
| **Vị thế cạnh tranh** | Moat "khó làm RAG bảo mật" biến mất; entry point dịch về nơi user đang làm việc (Office/Workspace/Teams) |
| **Đối thủ phản ứng tốt hơn** | **Glean** (enterprise AI search) định giá tăng mạnh 2024 (⚠️ verify số) → phân khúc không chết, mà tái cấu trúc về phía tích hợp sâu |

### 1.4. Bảng bằng chứng chốt

| # | Bằng chứng / số liệu | Vì sao quan trọng | Nguồn (tự verify) |
|---|---|---|---|
| E1 | Microsoft 365 Copilot GA 01/11/2023, ~$30/user/tháng | Đối thủ chỉ bật switch trên user mình đang phục vụ | [Microsoft Blog](https://www.microsoft.com/en-us/microsoft-365/blog/2023/09/21/announcing-microsoft-365-copilot-general-availability-and-microsoft-365-chat/) · [CNBC](https://www.cnbc.com/2023/09/21/microsoft-365-copilot-software-becomes-available-to-enterprises-nov-1.html) |
| E2 | ChatGPT Enterprise ra mắt 28/08/2023, có bảo mật doanh nghiệp | Phá lý do "chỉ specialist mới an toàn cho data nội bộ" | [OpenAI](https://openai.com/index/introducing-chatgpt-enterprise/) · [CNBC](https://www.cnbc.com/2023/08/28/openai-chatgpt-enterprise-launches.html) |
| E3 | Google NotebookLM + Gemini Workspace, hỏi-đáp có trích dẫn | Đúng tính năng lõi sản phẩm đang bán, nay bundled | [Google Blog](https://blog.google/technology/ai/notebooklm-google-ai/) · [TechCrunch](https://techcrunch.com/2023/12/08/googles-ai-assisted-notebooklm-note-taking-app-now-open-users-us/) |
| E4 | Glean (enterprise AI search): Series D $2.2B (đầu 2024) → Series E $4.6B + vượt $100M ARR (09/2024) → Series F $7.2B (06/2025) | Bằng chứng phân khúc tái cấu trúc, không xóa sổ — tiền dồn về lớp tích hợp sâu | [Glean](https://www.glean.com/blog/glean-series-d) · [CNBC](https://www.cnbc.com/2024/09/10/ai-powered-search-startup-glean-doubles-valuation-in-new-funding-round.html) · [TechCrunch](https://techcrunch.com/2025/06/10/enterprise-ai-startup-glean-lands-a-7-2b-valuation/) |
| E5 | RAG thành commodity (LangChain/LlamaIndex, API rẻ) | Rào cản kỹ thuật — moat cũ — đã sụp | [LlamaIndex](https://www.llamaindex.ai/) · [LangChain](https://www.langchain.com/) |

---

## Phần 2 — Phân tích

### Nhận định 1 — Trước AI, sản phẩm thắng nhờ giả định gì? JTBD là gì?

JTBD của user: *tìm đúng thông tin nội bộ thật nhanh và có bằng chứng đáng tin để dám hành động.* Sản phẩm thắng nhờ **3 giả định**: (a) dựng RAG + trích dẫn an toàn trên dữ liệu nội bộ là việc khó, cần vendor chuyên; (b) search keyword nội bộ truyền thống quá tệ nên có chỗ cho giải pháp tốt hơn; (c) user chấp nhận mở một app riêng để tra cứu.
*Bằng chứng đỡ:* E5.

### Nhận định 2 — Sau AI, kỳ vọng user đổi ở đâu? JTBD đổi thật hay chỉ đổi cách hoàn thành?

**JTBD không đổi** — user vẫn cần "tìm nhanh + có dẫn chứng để dám hành động". Cái đổi là **cách hoàn thành job** và **kỳ vọng**:
- Dịch chuyển kỳ vọng mạnh nhất: *"Làm xong giúp tôi — ngay trong nơi tôi đang làm việc"*, không phải "đưa tôi một app riêng để đi tra".
- Competitive dynamic mạnh nhất: **platform risk + build-copy cycle tăng tốc** — Big Tech bước xuống app layer và copy tính năng lõi trong vài tháng.
*Bằng chứng đỡ:* E1, E2, E3.

### Nhận định 3 — Cục diện mới: ai thay thế ai? Phân khúc bị xóa sổ hay tái cấu trúc?

Phân khúc **không bị xóa sổ mà bị tái cấu trúc**. Lớp "chat với tài liệu chung" bị Big Tech nuốt nhờ phân phối sẵn có. Giá trị dịch từ *"biết làm RAG"* sang *"tích hợp sâu hệ thống nội bộ + phân quyền chi tiết + chất lượng & độ tin cậy của trích dẫn ở mức audit được + workflow chuyên ngành"*. Giả định hết đúng: "RAG + trích dẫn là việc khó nên phải mua specialist".
*Bằng chứng đỡ:* E1, E4.

### Nhận định 4 — Ai đang thắng trong phân khúc đó và thắng nhờ gì?

- **Big Tech (Microsoft/Google/OpenAI)** thắng lớp phổ thông nhờ **distribution** — bán thêm trên user đã có sẵn, giá bundle.
- **Glean và lớp enterprise-AI chuyên sâu** thắng nhờ **đi sâu**: kết nối nhiều nguồn dữ liệu nội bộ, phân quyền theo người, chất lượng trả lời trên dữ liệu đặc thù — thứ Big Tech làm chưa tới.
*Bằng chứng đỡ:* E4.

---

## Verdict cuối

1. **Case yếu đi vì:** tính năng lõi (RAG + trích dẫn) bị Big Tech bundle vào công cụ user đã trả tiền → moat "khó làm" và entry point app-riêng biến mất.
2. **Điều thay đổi vĩnh viễn:** hỏi-đáp-có-dẫn-chứng trở thành **tiện ích mặc định trong luồng làm việc**, không còn là một sản phẩm riêng để bán. Chuẩn mới trong đầu user là "phải có sẵn ngay chỗ tôi đang làm".
3. **Cứu được không:** **Có, nhưng phải đổi rất mạnh** — bỏ cạnh tranh ở "chat tài liệu chung" (thua về distribution), dồn moat sang **tích hợp sâu hệ thống nội bộ + dữ liệu đặc thù + phân quyền + độ tin cậy trích dẫn audit-được**. So với Glean, sản phẩm đang chậm ở distribution và độ sâu tích hợp.

**Bài học cho dự án của nhóm:** khi giá trị lõi của bạn là thứ Big Tech có thể bundle, đừng dựng moat trên "làm được tính năng đó" — hãy dựng trên tích hợp sâu, dữ liệu đặc thù và niềm tin/độ kiểm chứng mà platform phổ thông không với tới.

---

*Lưu ý kiểm chứng trước khi nộp: bổ sung số liệu usage/ARR nội bộ thật của sản phẩm nếu có — đây là bằng chứng người chấm đánh giá cao nhất.*

---

## Nguồn tham khảo (đã đối chiếu)

**E1 — Microsoft 365 Copilot ($30/user/tháng, GA 01/11/2023)**
- Microsoft 365 Blog (chính thức): https://www.microsoft.com/en-us/microsoft-365/blog/2023/09/21/announcing-microsoft-365-copilot-general-availability-and-microsoft-365-chat/
- CNBC: https://www.cnbc.com/2023/09/21/microsoft-365-copilot-software-becomes-available-to-enterprises-nov-1.html

**E2 — ChatGPT Enterprise (ra mắt 28/08/2023)**
- OpenAI (chính thức): https://openai.com/index/introducing-chatgpt-enterprise/
- CNBC: https://www.cnbc.com/2023/08/28/openai-chatgpt-enterprise-launches.html
- TechCrunch: https://techcrunch.com/2023/08/28/openai-launches-a-chatgpt-plan-for-enterprise-customers/

**E3 — Google NotebookLM / Gemini (hỏi-đáp trên tài liệu, có trích dẫn nguồn; GA Mỹ 12/2023)**
- Google Blog (chính thức): https://blog.google/technology/ai/notebooklm-google-ai/
- TechCrunch: https://techcrunch.com/2023/12/08/googles-ai-assisted-notebooklm-note-taking-app-now-open-users-us/

**E4 — Glean (định giá tăng nhanh; bằng chứng phân khúc tái cấu trúc)**
- Glean Series D — $2.2B (chính thức): https://www.glean.com/blog/glean-series-d
- CNBC — Series E, định giá $4.6B (09/2024): https://www.cnbc.com/2024/09/10/ai-powered-search-startup-glean-doubles-valuation-in-new-funding-round.html
- TechCrunch — Series F, $7.2B (06/2025): https://techcrunch.com/2025/06/10/enterprise-ai-startup-glean-lands-a-7-2b-valuation/

**E5 — RAG / "chat-with-docs" thành commodity**
- LlamaIndex: https://www.llamaindex.ai/
- LangChain: https://www.langchain.com/
