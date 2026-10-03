# Memo Teardown — Grammarly

**Họ tên:** Đinh Thị Minh Tâm  
**MSV:** 2A202602433  
**Ngày chốt phân tích:** 03/10/2026

**Vì sao chọn sản phẩm này:**  
Tôi chọn Grammarly vì đây là một sản phẩm AI có lịch sử đủ dài để quan sát nhiều lần thay đổi cách tạo giá trị: từ sửa lỗi ngữ pháp cho sinh viên, sang trợ lý viết xuất hiện ở mọi nơi người dùng gõ, rồi mở rộng sang generative AI, agent và nền tảng productivity. Trường hợp này cũng phù hợp để phân tích switching cost vì Grammarly không sở hữu nơi người dùng viết, mà phải tạo giá trị ngay bên trong workflow đã tồn tại.

---

## §1. Timeline các cập nhật lớn

Qua timeline, tôi thấy Grammarly liên tục nâng **đơn vị giá trị**: từ sửa một lỗi → cải thiện cách một thông điệp được tiếp nhận → hỗ trợ cả vòng đời viết → hỗ trợ hoàn thành công việc rộng hơn viết. Đồng thời, chiến lược phân phối nhất quán là đưa AI đến nơi người dùng đã làm việc thay vì bắt họ chuyển sang một công cụ riêng.

| **Thời điểm** | **Cập nhật** | **Context lúc đó** | **Nguyên lý** |
|---|---|---|---|
| **2009** | Grammarly ra mắt dưới dạng online editor trả phí, ban đầu tập trung vào grammatical error correction cho sinh viên. [Nguồn](https://www.grammarly.com/blog/company/grammarly-12-year-history/) | Nhu cầu ban đầu là giúp người học viết tiếng Anh đúng hơn và tự tin hơn; sản phẩm còn nằm trong một bề mặt riêng thay vì đi theo user sang các ứng dụng khác. | **Vertical AI:** bắt đầu từ một job hẹp, có domain và tiêu chuẩn chất lượng tương đối rõ: phát hiện/sửa lỗi trong writing. Domain focus giúp hệ thống học sâu một loại công việc trước khi mở rộng. |
| **2015** | Grammarly phát hành Chrome extension miễn phí và chuyển từ subscription-only sang freemium; công ty ghi nhận user growth tăng mạnh sau bước này. [Nguồn](https://www.grammarly.com/blog/company/grammarly-12-year-history/) | Người dùng viết ở email, mạng xã hội và nhiều website khác nhau; bắt họ copy nội dung vào editor riêng tạo thêm friction. | **x10 + Switching cost:** thay vì yêu cầu user đổi workflow, Grammarly đi vào workflow có sẵn. Freemium giảm rào cản thử sản phẩm, còn extension giảm interaction cost vì giá trị xuất hiện ngay nơi user đang viết. |
| **2019** | Grammarly ra mắt Tone Detector, chuyển từ chỉ kiểm tra correctness sang phân tích cách thông điệp có thể được người đọc cảm nhận. [Nguồn](https://www.grammarly.com/blog/product/new-features-2019/) | Viết “đúng ngữ pháp” chưa đồng nghĩa với giao tiếp hiệu quả; email có thể đúng nhưng vẫn quá lạnh, quá gay gắt hoặc không đúng ý người gửi. | **Định nghĩa “tốt”:** quality của writing được mở rộng từ đúng/sai ngữ pháp sang outcome giao tiếp như tone và delivery. Product bắt đầu tối ưu cho mục tiêu của người viết chứ không chỉ lỗi bề mặt. |
| **15/11/2021** | Grammarly for Windows và Mac đưa trợ lý viết vào nhiều ứng dụng desktop như Microsoft Office, Slack, Discord và trình duyệt. [Nguồn](https://www.grammarly.com/blog/product/introducing-grammarly-for-mac-windows/) | Công việc viết bị phân tán qua nhiều ứng dụng; browser extension không bao phủ toàn bộ workflow trên desktop. | **Switching cost / Distribution moat:** Grammarly tiếp tục “đi theo user” thay vì sở hữu editor. Lợi thế không chỉ nằm ở model sửa câu mà còn ở lớp phân phối có mặt trên nhiều bề mặt nơi writing xảy ra. |
| **08/03/2023** | Grammarly công bố GrammarlyGO/generative AI, hỗ trợ tạo mới, rewrite, điều chỉnh tone, độ dài và đưa ra prompt theo context. [Nguồn](https://www.grammarly.com/blog/product/grammarlygo-augmented-intelligence/) | Generative AI làm cho việc tạo văn bản từ đầu trở nên khả thi ở quy mô lớn. Grammarly trước đó chủ yếu can thiệp ở giai đoạn revision. | **x10 / mở rộng JTBD:** đơn vị giá trị chuyển từ “sửa thứ tôi đã viết” sang “giúp tôi từ ý tưởng đến bản nháp rồi tiếp tục chỉnh”. Đây là mở rộng từ revision sang conception + composition, không chỉ thêm một nút chatbot. |
| **08–10/2024** | Grammarly ra mắt Authorship, theo dõi phần nào của tài liệu được người dùng gõ, được dán, được AI tạo hoặc AI chỉnh sửa, thay vì chỉ cố đoán bằng AI detector. [Nguồn](https://www.grammarly.com/blog/company/grammarly-launches-grammarly-authorship/) | Generative AI làm tăng anxiety trong giáo dục: sinh viên muốn chứng minh quá trình làm bài, còn giảng viên cần minh bạch về việc AI được dùng như thế nào. | **Vertical AI + định nghĩa “tốt”:** trong education, “bài viết tốt” không chỉ là output hay mà còn cần provenance và tính minh bạch. Grammarly biến một constraint của domain thành product capability thay vì chỉ cạnh tranh khả năng sinh văn bản. |
| **18/08/2025** | Grammarly công bố AI-native docs và tám specialized AI agents cho các job như tìm nguồn, kiểm tra originality, dự đoán phản ứng người đọc và đánh giá theo rubric. [Nguồn](https://www.grammarly.com/blog/company/grammarly-launches-ai-agents/) | Một general chatbot buộc user tự biết nên prompt gì; trong writing/education, nhiều job có tiêu chuẩn và workflow riêng. | **Vertical AI / Architect:** tách một assistant tổng quát thành các agent chuyên job, đưa domain judgment vào từng workflow. Product chuyển từ “gợi ý câu” sang hệ thống nhiều tác nhân hỗ trợ các bước khác nhau của writing process. |
| **05/11/2025** | Công ty đổi tên thành Superhuman và ra Superhuman Go, kết hợp Grammarly, Coda, Superhuman Mail và một lớp agent hoạt động xuyên các ứng dụng; Grammarly vẫn tiếp tục là sản phẩm cốt lõi trong suite. [Nguồn](https://www.grammarly.com/blog/company/announcing-company-rebrand-to-superhuman/) | Khi model nền tảng ngày càng dễ tạo text, một writing wrapper đơn thuần có nguy cơ bị commoditize. Trong khi đó, Grammarly đã có lớp phân phối hoạt động ở rất nhiều ứng dụng và có thể dùng lớp này cho nhiều agent hơn writing. | **Wrapper → Moat:** mở rộng moat từ “AI viết tốt” sang workflow distribution + context + agent ecosystem. Đây là pivot về phạm vi: từ writing assistant sang productivity platform, nhưng lợi thế kế thừa vẫn là hiện diện trong flow of work. |

### Vì sao chọn những mốc này?

Tôi chọn các mốc làm thay đổi **job mà Grammarly nhận, bề mặt sản phẩm hoặc tiêu chuẩn giá trị**, thay vì chọn mọi feature release. Chuỗi mốc cho thấy ba lần nâng abstraction rõ nhất: grammar correction → communication assistance → generative/agentic productivity.

Tôi cân nhắc nhưng không đưa **mở rộng hỗ trợ thêm 17 ngôn ngữ vào 03/2026** thành milestone chính. Đây là một bước mở rộng segment quan trọng, nhưng về cơ chế tạo giá trị nó chủ yếu scale mô hình “real-time writing support wherever you write” sang nhiều ngôn ngữ hơn, chưa thay đổi product logic mạnh bằng GrammarlyGO, Authorship hay agent platform. Tôi dùng nó như bằng chứng hỗ trợ cho hướng mở rộng thị trường, không xem là một pivot riêng.

---

## §2. Tệp user & JTBD

|  | **Early adopters** | **Tệp hiện tại** |
|---|---|---|
| **Đặc điểm** | Sinh viên/người học viết tiếng Anh thường xuyên, lo lỗi ngữ pháp và plagiarism, sẵn sàng dùng một online editor riêng để kiểm tra bài trước khi nộp | Knowledge worker hoặc thành viên team viết email, docs, chat và tài liệu khách hàng trong nhiều ứng dụng; đồng thời Grammarly vẫn phục vụ sinh viên/giảng viên qua Education |
| **JTBD chính** | Khi chuẩn bị bài viết quan trọng bằng tiếng Anh, phát hiện và sửa lỗi trước khi nộp để diễn đạt đúng và tự tin hơn | Khi phải giao tiếp và hoàn thành công việc qua nhiều ứng dụng, tạo/chỉnh nội dung đúng mục đích, đúng giọng điệu và có đủ context mà không phải liên tục chuyển sang công cụ AI khác |
| **Trước đó họ làm bằng cách nào** | Tự proofread, dùng spell checker cơ bản, nhờ bạn bè/giảng viên đọc lại, hoặc dùng công cụ plagiarism riêng | Dùng spell checker tích hợp + ChatGPT/LLM riêng + copy/paste giữa email/docs/chat + tìm thông tin hoặc style guide ở các công cụ khác |

Các tệp trên được dùng như **segment theo hoàn cảnh công việc**, không phải khẳng định về tỷ trọng người dùng. Nguồn lịch sử của Grammarly xác nhận sản phẩm ban đầu tập trung vào sinh viên và grammatical error correction, sau đó mở rộng sang mass-market consumers và business. Hiện Grammarly được định vị cho cá nhân, professionals/teams và education.

### Dịch chuyển tệp

Mốc **2015 Chrome + freemium** là bước dịch chuyển lớn đầu tiên: Grammarly không còn yêu cầu user đến một editor riêng mà xuất hiện ngay trong nơi họ viết, mở rộng từ sinh viên sang mass-market use.

Mốc **Desktop 2021** tiếp tục mở rộng bề mặt từ browser sang nhiều ứng dụng làm việc. **GrammarlyGO 2023** nâng job từ sửa lỗi sang tạo và rewrite nội dung. Đến **AI Agents 2025** và **Superhuman Go**, phạm vi tiếp tục mở từ “viết tốt hơn” sang “hoàn thành nhiều task trong flow of work”.

Nói cách khác, segment shift không chỉ là từ “student → professional”; quan trọng hơn là shift từ một người **chủ động mang văn bản đến Grammarly** sang một người **đang làm việc trong công cụ khác và mong AI xuất hiện đúng lúc, đúng context**.

### Switching cost — 4 forces

**Push — vấn đề với cách cũ:**  
Proofreading thủ công tốn thời gian; spell checker cơ bản bắt lỗi nhưng không xử lý clarity, tone hay mục tiêu giao tiếp. Với generative AI, một pain mới là phải copy/paste context sang chatbot rồi quay lại ứng dụng chính.

**Pull — sức hút của Grammarly:**  
Grammarly cung cấp feedback theo thời gian thực ngay nơi user viết; sau GrammarlyGO và agents, sức hút mở rộng sang drafting, rewrite, research, feedback và các task có context. Giá trị cốt lõi không chỉ là “AI thông minh hơn”, mà là **ít phải rời flow hơn**.

**Habit — thói quen giữ user ở giải pháp cũ:**  
User đã quen spell checker trong Word/Google Docs, dùng ChatGPT riêng, hoặc tự proofread. Đây là lý do chiến lược “works where you work” quan trọng: Grammarly cố giảm yêu cầu thay đổi habit thay vì bắt user chuyển hoàn toàn sang một editor mới.

**Anxiety — nỗi lo khi dùng Grammarly/AI:**  
User có thể sợ suggestion làm mất giọng văn, sửa sai context, khiến nội dung trở nên giống nhau, hoặc lo privacy khi công cụ đọc nội dung trong nhiều ứng dụng. Trong education còn có anxiety về academic integrity; trong enterprise có thêm governance và dữ liệu tổ chức. Authorship, user control, privacy controls và reviewable suggestions là các cách sản phẩm giảm lực này.

### Đối chiếu hai tệp

Ở early adopters, **push** là lỗi ngữ pháp/plagiarism và thiếu tự tin; **pull** là correction tốt hơn; **habit** là tự proofread; **anxiety** là tin hay không tin suggestion.

Ở tệp hiện tại, **push** lớn hơn ở context switching và khối lượng communication; **pull** là AI có mặt xuyên workflow và ngày càng có thể làm nhiều bước hơn; **habit** là dùng Word/Docs/ChatGPT riêng; **anxiety** chuyển sang voice, accuracy, privacy và governance.

### Lực giữ user mạnh nhất

Theo tôi, lợi thế giữ user của Grammarly hiện không phải **data lock-in** mạnh. Người dùng vẫn sở hữu email, document và file ở ứng dụng khác.

Lực đáng chú ý hơn là **workflow habit + ubiquitous distribution**: user đã quen nhận suggestion ngay tại nơi đang viết. Với team/enterprise, style guide, brand tone, organizational knowledge và admin configuration có thể làm switching cost tăng thêm.

Nếu Microsoft, Google hoặc một general AI assistant cung cấp chất lượng tương đương và xuất hiện tự nhiên hơn ngay trong cùng workflow, lợi thế này có thể suy giảm. Vì vậy Grammarly/Superhuman phải tiếp tục làm lớp context + orchestration + trust dày hơn, thay vì chỉ dựa vào khả năng rewrite.

---

## §3. Ba dự đoán hướng đi trong 6–12 tháng tới

> Các phần dưới đây là dự đoán của tôi dựa trên trajectory ở §1 và user/JTBD ở §2, không phải roadmap Grammarly/Superhuman đã công bố.

### Dự đoán 1 — Grammarly/Superhuman sẽ tiếp tục dịch từ “writing assistance” sang lớp proactive agent orchestration trong flow of work

**Loại:** mở rộng tính năng / định vị sản phẩm

**Dự đoán:**  
Trong 6–12 tháng tới, Superhuman Go nhiều khả năng sẽ có thêm các workflow trong đó nhiều agent phối hợp để thực hiện một outcome xuyên ứng dụng, thay vì chủ yếu đưa suggestion hoặc chờ user chọn từng agent.

**Lập luận:**  
Trajectory đi từ browser extension → desktop “works where you work” → GrammarlyGO → specialized agents → Superhuman Go. Trong 2026, Superhuman tiếp tục mở rộng partner-agent ecosystem. Điều này cho thấy strategic asset đang dịch từ “một model viết tốt” sang **lớp phân phối + context + orchestration**.

JTBD của tệp hiện tại cũng ủng hộ hướng này: knowledge worker không muốn quản nhiều tool; họ muốn công việc được tiến lên ngay trong flow hiện tại.

**Dấu hiệu kiểm chứng:**  
Đến 03/10/2027, Go có workflow mà một trigger trong email/doc có thể tự gọi nhiều agent/connector nối tiếp và tạo ra hành động ở ứng dụng khác, với bước review/approval rõ ràng. Chỉ thêm nhiều agent riêng lẻ nhưng user vẫn phải tự điều phối từng agent chưa đủ xác nhận dự đoán.

**Điều có thể làm dự đoán sai:**  
Nếu người dùng thấy proactive agent quá intrusive hoặc enterprise hạn chế quyền truy cập/action vì privacy, Superhuman có thể phải giữ sản phẩm ở mức suggestion hơn là autonomous workflow.

---

### Dự đoán 2 — Provenance/Authorship sẽ mở rộng từ academic integrity sang trust layer cho nội dung do nhiều AI agent cùng tạo

**Loại:** moat / trust infrastructure

**Dự đoán:**  
Grammarly Authorship nhiều khả năng sẽ tiếp tục mở rộng khả năng attribution để giải thích rõ **ai/agent nào tạo hoặc chỉnh phần nào**, và logic provenance này có thể được dùng ngoài education trong các workflow cần audit hoặc accountability.

**Lập luận:**  
Authorship 2024 đã thay đổi cách tiếp cận từ “đoán văn bản có phải AI không” sang theo dõi quá trình tạo nội dung. Đến 2026, Superhuman đã bổ sung agent-specific attribution trong Authorship. Khi một document có thể được tác động bởi Grammarly, partner agents và các external AI tools, câu hỏi không còn chỉ là “AI hay human?” mà là **AI nào, làm gì, ở bước nào và ai chịu trách nhiệm review**.

Điều này nối trực tiếp với **Anxiety** ở §2: adoption càng tăng thì trust/provenance càng trở thành điều kiện để education và enterprise cho phép dùng AI sâu hơn.

**Dấu hiệu kiểm chứng:**  
Đến 03/10/2027, Authorship hoặc một capability kế thừa có audit trail chi tiết theo agent/tool và có policy/reporting cho organization ngoài classroom. Chỉ cải thiện AI detector score sẽ không đủ xác nhận.

**Điều có thể làm dự đoán sai:**  
Nếu doanh nghiệp không coi provenance là pain đủ lớn hoặc các platform lớn tự cung cấp audit trail chuẩn hóa, đây có thể trở thành feature hỗ trợ thay vì moat.

---

### Dự đoán 3 — Enterprise moat sẽ tập trung nhiều hơn vào organizational context, permissions và governance

**Loại:** segment / moat / enterprise

**Dự đoán:**  
Trong 6–12 tháng tới, Grammarly/Superhuman nhiều khả năng sẽ mở rộng cơ chế để agent dùng organizational knowledge có kiểm soát, đồng thời tăng admin controls về agent permission, connector access, data boundary và action approval.

**Lập luận:**  
Grammarly Business đã đi từ correction cá nhân sang style guide, brand tone và Knowledge Share; Superhuman Go tiếp tục kéo context từ nhiều ứng dụng để hỗ trợ work. Nhưng càng nhiều context và action, **Anxiety** càng tăng: AI có được đọc CRM không, có được gửi email không, có được tạo ticket hay chỉnh tài liệu không?

Với tệp enterprise ở §2, buyer không chỉ là end user. Security, IT và management cùng tham gia quyết định. Do đó moat không chỉ là chất lượng writing mà là khả năng kết hợp **useful context + governance + trust**.

**Dấu hiệu kiểm chứng:**  
Đến 03/10/2027, admin có thể quy định agent/connector nào được dùng cho từng nhóm, dữ liệu nào được truy cập và hành động nào cần approval; đồng thời analytics cho thấy usage theo workflow hoặc agent, không chỉ theo seat.

**Điều có thể làm dự đoán sai:**  
Nếu khách hàng ưu tiên AI đơn giản, ít cấu hình và không muốn một platform trung gian truy cập nhiều hệ thống, Superhuman có thể phải giới hạn độ sâu của integrations.

---

## §4. AI Log

ChatGPT được sử dụng như công cụ hỗ trợ research, tổng hợp nguồn và phản biện. Tôi trực tiếp quyết định storyline, lựa chọn mốc, xác định JTBD, đánh giá 4 forces và chịu trách nhiệm với ba dự đoán cuối cùng.

| **Công việc** | **Vai trò AI và người học** | **Tôi kiểm chứng/phán đoán lại như thế nào?** |
|---|---|---|
| Khai phá nguồn và timeline ứng viên | AI hỗ trợ tìm lịch sử sản phẩm, blog/changelog và các mốc lớn. Tôi quyết định mốc nào cần đọc và giữ. | Tôi ưu tiên nguồn chính thức của Grammarly/Superhuman để xác nhận ngày và nội dung; Product Hunt/review chỉ dùng như nguồn bổ sung về cách user nhìn sản phẩm. |
| Chọn 8 cột mốc | AI gợi ý nhiều candidate milestones. Tôi chọn các mốc làm thay đổi job, distribution hoặc tiêu chuẩn giá trị của sản phẩm. | Tôi loại các update chỉ mở rộng phạm vi nhưng chưa đổi product logic, ví dụ mở thêm 17 ngôn ngữ năm 2026, khỏi timeline chính. |
| Revert nguyên lý | AI gợi ý mapping với x10, switching cost, wrapper/moat, Vertical AI và định nghĩa “tốt”. Tôi chọn mapping cuối và viết lại theo cơ chế. | Tôi chỉ giữ nguyên lý nếu có thể giải thích “vì sao quyết định này tạo giá trị”, không dùng các nhãn chung như “để tăng trưởng”. |
| Xác định early adopter và current segment | AI hỗ trợ tổng hợp lịch sử và positioning hiện tại. Tôi chọn segment theo hoàn cảnh công việc thay vì demographic. | Tôi dựa vào nguồn lịch sử xác nhận Grammarly ban đầu tập trung vào students, rồi mở sang mass market/business; current segment được mô tả như giả thuyết theo workflow, không phải tỷ trọng khách hàng. |
| Viết JTBD và 4 forces | AI hỗ trợ đặt thông tin vào framework. Tôi quyết định abstraction level và lực quan trọng. | Tôi loại cách viết theo feature như “user cần GrammarlyGO”; JTBD phải mô tả việc user cần hoàn thành. Tôi cũng không coi Grammarly có data lock-in mạnh khi document vẫn nằm ở ứng dụng khác. |
| Xây dựng ba dự đoán | AI hỗ trợ brainstorm các hướng tương lai. Tôi chọn prediction và nối về §1–§2. | Mỗi dự đoán phải có trajectory, user/constraint, dấu hiệu kiểm chứng và điều kiện phản bác. Tôi không trình bày prediction như fact đã xảy ra. |
| Kiểm tra fact/citation | AI hỗ trợ phát hiện claim cần nguồn. Tôi đối chiếu nguồn trước khi giữ chi tiết trong memo. | Tôi phân biệt nguồn chứng minh Grammarly đã ra gì với suy luận của tôi về moat, switching cost hay motive chiến lược. |
| Rà soát theo rubric | AI hỗ trợ đóng vai reviewer. Tôi quyết định chỉnh sửa cuối. | Tôi tự kiểm đủ 8 mốc có nguồn, principle có tên và cơ chế, JTBD theo job, 3 prediction dẫn về phần trước và AI Log nêu rõ ranh giới. |
