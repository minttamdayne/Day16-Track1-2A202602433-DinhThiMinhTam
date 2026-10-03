# Memo Teardown — Cursor

**Họ tên:** Đinh Thị Minh Tâm
**MSV:** 2A202602433
**Ngày chốt phân tích:** 03/10/2026; cửa sổ dự đoán: 03/04–03/10/2027.

**Vì sao chọn sản phẩm này:**
Tôi chọn Cursor vì AI không phải một tính năng phụ mà nằm ở trung tâm trải nghiệm phát triển phần mềm. Sản phẩm cũng có timeline công khai đủ dài để quan sát rõ sự dịch chuyển từ AI hỗ trợ viết code sang agent có thể nhận và thực hiện ngày càng nhiều phần của software-development workflow.

---

## §1. Timeline các cập nhật lớn

Qua timeline, tôi thấy Cursor không chỉ liên tục làm AI “code tốt hơn”, mà đang nâng dần **đơn vị công việc mà AI có thể đảm nhận**: từ một edit, sang một task, rồi đến một khối công việc dài hạn.

| Thời điểm | Cập nhật | Context lúc đó | Nguyên lý |
|---|---|---|---|
| **03/2024 (được bài 13/01/2025 xác nhận hồi cứu)** | Cursor bắt đầu dùng model riêng cho Tab, được tối ưu cho việc dự đoán chỉnh sửa code. [Nguồn](https://www.cursor.com/blog/tab-update) | Các general-purpose model có thể sinh code nhưng interaction trong editor cần độ trễ thấp và hiểu đúng editing behavior của developer. | **Wrapper → Moat:** thay vì chỉ wrap model bên ngoài, Cursor sở hữu capability chuyên biệt ở một interaction cốt lõi của coding workflow. |
| **13/01/2025** | Cursor giới thiệu Fusion và hướng tới Next Action Prediction: không chỉ sinh text mà còn dự đoán edit và vị trí developer có khả năng thao tác tiếp theo. [Nguồn](https://www.cursor.com/blog/tab-update) | Autocomplete giải quyết việc “gõ gì tiếp theo” nhưng chỉ là một phần của công việc edit code. | **x10:** loại bỏ cả thao tác khỏi workflow thay vì chỉ làm thao tác hiện tại nhanh hơn. |
| **04/06/2025** | Background Agent được mở cho toàn bộ người dùng trong Cursor 1.0. [Nguồn](https://cursor.com/changelog/1-0) | Agent bắt đầu đủ khả năng thực hiện task trong remote environment thay vì chỉ hỗ trợ developer khi họ đang trực tiếp code. | **x10 / đổi đơn vị giá trị:** từ “assist me while I work” sang “do the work while I am away”; giá trị chuyển từ edit sang delegated task. |
| **30/06/2025** | Cursor đưa Agents lên web và mobile; user có thể giao bug fix, feature hoặc câu hỏi codebase và review kết quả sau. [Nguồn](https://cursor.com/blog/agent-web) | Khi task đã có thể chạy bất đồng bộ, user không còn bắt buộc phải ngồi trước IDE trong toàn bộ quá trình. | **JTBD:** khi cần đưa một sửa lỗi tiến lên trong lúc rời máy, công việc vẫn là giao task và nhận kết quả để review; web/mobile bỏ ràng buộc địa điểm. Chỉ thêm kênh truy cập chưa đủ chứng minh switching cost tăng. |
| **29/10/2025** | Cursor 2.0 ra mắt cùng Composer và giao diện multi-agent, được thiết kế xoay quanh agents thay vì files. [Nguồn](https://cursor.com/blog/2-0) | Agentic coding trở thành workflow chính hơn; Cursor cũng bắt đầu sở hữu first-party agent model được train cùng code-search/editing tools. | **Wrapper → Moat:** huấn luyện model cùng công cụ tìm/sửa code cho phép tối ưu cả vòng thực thi. Đây là ứng viên lợi thế khó sao chép hơn giao diện gọi API; sở hữu model chưa tự chứng minh moat bền vững. |
| **24/02/2026** | Cloud Agents có Computer Use: agent có VM riêng, có thể chạy software, test thay đổi và tạo video/screenshot/log để developer review. [Nguồn](https://cursor.com/blog/agent-computer-use) | Viết code chưa đủ để chứng minh output tốt; agent cần sử dụng phần mềm mình tạo ra và kiểm tra kết quả. | **Định nghĩa “tốt”:** bổ sung chạy thử và artifacts để người review kiểm tra hành vi thực tế. Generate → execute → observe → revise là vòng phản hồi trong task; chưa có bằng chứng ở mốc này rằng mỗi lần dùng đều cải thiện model cho mọi user. |
| **10/09/2026** | Cursor ra mắt Projects: quản lý feature, migration hoặc full app, giữ context qua nhiều tháng và delegate cho nhiều subagents. [Nguồn](https://cursor.com/blog/projects) | Cursor cho rằng software development đang bước vào giai đoạn developer không còn cần quản từng agent riêng lẻ mà có thể chỉ đạo cả một body of work. | **x10:** giảm số lần người dùng phải giao lại context và quản từng task bằng coordinator cùng context dùng lại. Đơn vị giá trị chuyển sang một khối công việc nhiều PR; lợi ích còn phụ thuộc việc giảm công điều phối có lớn hơn công review hay không. |

| **23/09/2026** | Rollouts và Security Review nối review với theo dõi thay đổi sau deploy. [Nguồn](https://cursor.com/blog/rollouts-and-security-reviewer) | Khi tạo PR nhanh hơn, kiểm tra an toàn và phát hiện regression sau phát hành trở thành phần việc còn tốn công. | **Định nghĩa “tốt”:** chất lượng mở rộng từ chạy được trong sandbox sang hành vi production so với baseline; quyết định phản ứng còn phụ thuộc cấu hình và phê duyệt. |

### Vì sao chọn những mốc này?

Tôi chọn các mốc làm thay đổi **cách Cursor tạo giá trị hoặc đơn vị công việc mà AI đảm nhận**, thay vì chọn theo độ lớn của release announcement. Chuỗi mốc cho thấy sự dịch chuyển từ dự đoán edit → nhận task → thực thi bất đồng bộ → tự kiểm thử → điều phối cả khối công việc.

Tôi không tách mọi lần nâng cấp model thành mốc riêng: chỉ khi cập nhật đổi cơ chế tạo giá trị, mức giao việc hoặc tiêu chuẩn nghiệm thu thì mới giữ trong timeline. Rollouts được chọn vì mở rộng tiêu chuẩn chất lượng ra production, khác với kiểm thử trong VM ở Computer Use.

---

## §2. Tệp user & JTBD

|  | Early adopters | Tệp hiện tại |
|---|---|---|
| **Đặc điểm** | Developer tự phụ trách một repo hoặc feature, đã quen VS Code, thường tự đọc và sửa code trực tiếp, có quyền chọn editor và sẵn sàng thử hỗ trợ AI | Engineer phụ trách migration nhiều PR, feature liên quan nhiều module hoặc bảo trì repo chung; phải phối hợp reviewer, CI và người quản lý quyền truy cập/ngân sách |
| **JTBD chính** | Khi đã biết mình muốn sửa gì trong code, chuyển từ ý định sang một thay đổi đúng trong codebase nhanh hơn mà không phải tự gõ, tìm kiếm và chuyển context quá nhiều | Khi có bug, feature, migration hoặc task trên codebase lớn, giao một phần công việc cho AI thực hiện và kiểm thử để developer có output có thể review nhanh hơn |
| **Trước đó họ làm bằng cách nào** | VS Code + manual coding + Google/Stack Overflow + Copilot/chatbot + các extension AI riêng lẻ | Engineer đọc ticket → tìm hiểu codebase → edit nhiều file → chạy test → debug → tạo PR → review |

Các tệp trên là **giả thuyết segment theo hoàn cảnh công việc**, suy ra từ workflow mà sản phẩm hỗ trợ; không phải số liệu phân bố khách hàng hay nghiên cứu phỏng vấn. [Projects](https://cursor.com/blog/projects) minh họa migration nhiều PR; [Rollouts](https://cursor.com/blog/rollouts-and-security-reviewer) bổ sung nhu cầu theo dõi production của team.

### Dịch chuyển tệp

Các mốc **Background Agent → Web/Mobile Agents → Cursor 2.0 → Computer Use** tạo ra sự dịch chuyển rõ nhất.

Background Agent thay đổi interaction từ:

`AI giúp tôi khi tôi đang code`

sang:

`Tôi giao một task, AI làm và tôi quay lại review`.

Sau đó Web/Mobile làm workflow này không còn phụ thuộc vào IDE; Cursor 2.0 đặt agents thay vì files ở trung tâm giao diện; Computer Use tiếp tục nâng giá trị từ “AI viết code” sang “AI có thể thực thi, kiểm tra và đưa lại kết quả có bằng chứng”.

### Switching cost — 4 forces

**Push — vấn đề với cách cũ:**
Coding workflow bị phân mảnh giữa manual coding, search, chatbot và nhiều extension. Developer vẫn phải tự tìm context, chuyển giữa nhiều tool và thực hiện phần lớn các thay đổi multi-file.

**Pull — sức hút của Cursor:**
Cursor giảm khoảng cách từ intent đến working software. Giá trị tăng dần từ context-aware autocomplete sang agent có thể thực hiện cả task, chạy background, test và tạo output để review.

**Habit — thói quen giữ user ở cách cũ:**
Developer đã quen với shortcut, extension, debugger, Git workflow và muscle memory trong VS Code hoặc JetBrains. Cursor giảm lực cản này bằng trải nghiệm rất gần VS Code thay vì bắt user học một editor hoàn toàn mới.

**Anxiety — nỗi lo khi chuyển đổi:**
User có thể lo AI sửa sai code, mất kiểm soát, tạo chi phí khó dự đoán hoặc gây rủi ro bảo mật. Với enterprise, anxiety còn gồm privacy, governance và security. Vì vậy reviewable diffs, isolated environments, spend controls và administrative controls trở thành một phần quan trọng của product value.

**Đối chiếu hai tệp:** ở tệp tự sửa code, push là thao tác lặp lại, pull là Tab/Fusion (§1, 03/2024–01/2025), habit là editor và anxiety là edit sai. Ở tệp phối hợp nhiều PR, push là tồn đọng migration/review, pull là Projects và Rollouts (§1, 09/2026), habit là quy trình CI/review đã duyệt, anxiety là agent chạm production và vượt ngân sách. Switching cost lúc rời Cursor là công chuyển rules/context, dựng lại môi trường agent và xin duyệt integrations; chưa có dữ liệu để định lượng.

### Lực giữ user mạnh nhất

Ở giai đoạn chuyển **từ IDE cũ sang Cursor**, lực cản mạnh nhất theo tôi là **habit**. Developer có workflow rất sâu với IDE hiện tại.

Nhưng sau khi đã dùng Cursor, switching cost ngày càng chuyển sang **agentic workflow habit + context + team integrations**. Source code vẫn chủ yếu nằm trong Git repository nên Cursor không có kiểu data lock-in mạnh như Notion. Nếu các đối thủ tái tạo được cùng agent workflow với chất lượng tương đương, switching cost của Cursor có thể giảm đáng kể.

---

## §3. Ba dự đoán hướng đi trong 6–12 tháng tới

### Dự đoán 1 — Cursor sẽ tiếp tục chuyển từ “AI IDE” sang lớp orchestration cho software work
**Loại:** mở rộng tính năng / định vị sản phẩm

**Dự đoán:**
Trong 6–12 tháng tới, Cursor nhiều khả năng sẽ mở rộng Projects theo hướng để user giao những outcome ngày càng lớn hơn cho một hệ thống nhiều agent, thay vì phải tạo và quản từng agent/task riêng lẻ.

**Lập luận:**
Trajectory đã đi khá liên tục từ Tab → Background Agent → multi-agent → Computer Use → Projects. Cursor 2.0 đã chuyển UI từ file-centric sang agent-centric, còn Projects hiện được thiết kế để duy trì context qua nhiều tháng và delegate cho nhiều subagents. Cursor cũng mô tả đây là việc đưa developer lên một mức abstraction cao hơn. Vì vậy bước tiếp theo hợp lý không phải chỉ thêm một coding feature mới, mà là tăng khả năng **planning, orchestration, dependency management và verification** trên các body of work lớn hơn.

Điều này cũng khớp JTBD của tệp hiện tại: engineering team không chỉ muốn “code nhanh hơn” mà muốn **ship một kết quả phần mềm nhanh hơn**.

**Dấu hiệu kiểm chứng:** đến 03/10/2027 có changelog cho phép người phụ trách đặt dependency giữa các PR/task và thấy trạng thái bị chặn cùng điều kiện nghiệm thu ở cấp Project. Shared context và coordinator đã tồn tại; chỉ cải thiện tốc độ model không đủ xác nhận dự đoán. Nếu công review tăng nhanh hơn khối lượng hoàn thành, hướng orchestration có thể chậm lại.

### Dự đoán 2 — Cursor sẽ đầu tư mạnh hơn vào verifier, review và safety thay vì chỉ làm generator thông minh hơn
**Loại:** mở rộng capability / moat

**Dự đoán:**
Cursor nhiều khả năng sẽ mở rộng các lớp tự động kiểm chứng như testing, security review, rollout checks, code review và artifacts để agent có thể chứng minh rằng work của nó đủ tốt trước khi human review.

**Lập luận:**
Computer Use đã đóng một phần feedback loop: agent có thể chạy software mình tạo ra và cung cấp video, screenshot, log. Mốc 23/09/2026 ở §1 đã có Security Review và Rollouts. [Nguồn chính thức](https://cursor.com/blog/rollouts-and-security-reviewer). Vì vậy dự đoán ở đây là bước tích hợp và kiểm soát tiếp theo, không dự đoán lại tính năng đã ra mắt.

Khi agent nhận task ngày càng lớn, bottleneck không còn chỉ là **“AI có sinh được code không?”** mà thành:

`Làm sao biết output này đúng, an toàn và có thể merge?`

Điều này nối trực tiếp với nguyên lý **định nghĩa “tốt”** của Day 16: AI product cần biến đánh giá cảm tính thành thứ có thể kiểm tra và scale.

Đồng thời nó giải **anxiety force** ở §2. Nếu user không tin agent, delegation sẽ chạm trần dù model thông minh hơn.

**Dấu hiệu kiểm chứng:** đến 03/10/2027 có chính sách nghiệm thu do team cấu hình dùng chung cho test, security finding và rollout signal, kèm bằng chứng và bước phê duyệt trước hành động production. Rollouts đã có monitoring plan; dự đoán là nối các lớp kiểm tra thành một quy trình. False positive hoặc thiếu telemetry là lý do hướng này có thể không đạt kỳ vọng.

### Dự đoán 3 — Enterprise sẽ trở thành một battleground lớn hơn, với pricing và governance ngày càng gắn với agent usage
**Loại:** segment + mô hình kiếm tiền

**Dự đoán:**
Trong 6–12 tháng tới, Cursor nhiều khả năng tiếp tục phát triển pricing, quota và quản trị quanh mức độ sử dụng agent/model thay vì chỉ dựa vào một seat đồng nhất.

**Lập luận:**
[Pricing](https://cursor.com/pricing) phân biệt mức sử dụng và có pooled usage ở Enterprise. [Trang Enterprise](https://cursor.com/enterprise) mô tả seat kèm usage và giới hạn chi phí ở cấp team/user. Đây là nền tảng đã có, không phải dự đoán Cursor bỏ seat.

Điều này cho thấy buyer hiện không chỉ là developer. Cursor phải đồng thời thuyết phục:

- developer rằng AI hữu ích,
- engineering manager rằng productivity tăng,
- security rằng hệ thống đủ an toàn,
- finance rằng chi phí có thể dự đoán.

Nếu agent nhận ngày càng nhiều work, consumption giữa một “light user” và một “heavy agent user” sẽ khác nhau rất lớn. Vì vậy pricing và governance nhiều khả năng sẽ tiếp tục phản ánh **actual AI work consumed**, thay vì chỉ số seat.

**Nối §1–§2:** Background Agent và Projects làm lượng task mỗi người có thể giao phân hóa; Rollouts kéo thêm người chịu trách nhiệm production vào quyết định mua. Tệp nhiều PR ở §2 cần phân bổ chi phí và quyền theo công việc, còn anxiety là chi phí khó kiểm soát.

**Dấu hiệu kiểm chứng:** đến 03/10/2027 có báo cáo usage/budget theo Project và quyền giới hạn model hoặc hành động agent ở cùng cấp đó. Chỉ có thêm gói seat chưa đủ xác nhận. Nếu khách hàng ưu tiên hóa đơn đơn giản hoặc khó quy usage cho Project, Cursor có thể tiếp tục chủ yếu dùng giới hạn team/user.

---

## §4. AI Log

Chatgpt, Codex được sử dụng như công cụ hỗ trợ research và phản biện: gợi ý nguồn, tổng hợp thông tin, kiểm tra tính nhất quán và đề xuất các hướng lập luận. Tôi trực tiếp đọc nguồn gốc, lựa chọn cột mốc, quyết định cách revert nguyên lý, xác định tệp user/JTBD và chịu trách nhiệm với ba dự đoán cuối cùng.

| Công việc | Vai trò AI và người học | Tôi kiểm chứng/phán đoán lại như thế nào? |
|---|---|---|
| Khai phá nguồn và timeline ứng viên | AI hỗ trợ tìm các changelog, blog và gợi ý danh sách mốc ứng viên. Tôi lựa chọn những nguồn và mốc cần đọc tiếp. | Tôi mở lại nguồn gốc của từng mốc, kiểm tra ngày và nội dung thực tế. Chỉ giữ những mốc tôi cho rằng làm thay đổi đáng kể cách Cursor tạo giá trị, thay vì lấy toàn bộ changelog. |
| Chọn 7 cột mốc trong timeline | AI gợi ý cách nhóm các cập nhật theo trajectory. Việc quyết định mốc nào được giữ hoặc loại là của tôi. | Tôi dùng tiêu chí: mốc phải thay đổi unit of value, cách user tương tác hoặc hướng xây moat. Ví dụ, tôi loại Composer 2 khỏi timeline chính vì nó chủ yếu tiếp tục hướng sở hữu model đã xuất hiện ở Cursor 2.0. |
| Revert về nguyên lý | AI hỗ trợ nhắc lại và đề xuất mapping với các khái niệm Day 16 như x10, wrapper/moat, switching cost, vòng lặp học. Tôi chọn nguyên lý và viết lại lập luận. | Với mỗi mốc, tôi tự hỏi cơ chế nào khiến quyết định đó tạo giá trị và chỉ giữ principle mà tôi có thể tự giải thích. Tôi không dùng các nhãn chung như “để tăng trưởng” nếu không chỉ ra được cơ chế. |
| Xác định early adopters, user hiện tại và JTBD | AI hỗ trợ tổng hợp nguồn cộng đồng và đề xuất các cách phân nhóm. Tôi xác định tệp user và JTBD dựa trên hành vi, hoàn cảnh sử dụng và cách làm trước đó. | Tôi tránh mô tả chung như “developer” và tránh viết JTBD theo tính năng. Tôi đối chiếu segment shift với các mốc Background Agent, Web/Mobile, Cursor 2.0 và Computer Use. Các nhận định về segment vẫn được xem là suy luận từ bằng chứng công khai, không phải nghiên cứu user đại diện toàn bộ người dùng. |
| Phân tích switching cost – 4 forces | AI hỗ trợ đặt thông tin vào khung Push, Pull, Habit và Anxiety. Tôi quyết định lực nào quan trọng và giải thích lý do. | Tôi nhận thấy Habit là lực cản lớn khi developer chuyển từ IDE cũ, nhưng không kết luận Cursor có data lock-in mạnh vì source code chủ yếu vẫn nằm trong repository. Đây là phần phán đoán của tôi dựa trên cách sản phẩm vận hành. |
| Xây dựng 3 dự đoán | AI hỗ trợ brainstorm nhiều hướng có thể xảy ra. Tôi chọn ba prediction cuối cùng và tự nối chúng với §1–§2. | Tôi chỉ giữ dự đoán nếu có thể chỉ ra trajectory trong timeline và nhu cầu/constraint của user làm cơ sở. Các dự đoán được ghi rõ là suy luận cho 6–12 tháng tới, không phải thông tin Cursor đã công bố. |
| Kiểm tra fact và citation | AI hỗ trợ phát hiện link hoặc câu có nguy cơ thiếu nguồn. Tôi trực tiếp đối chiếu nguồn chính thức trước khi giữ claim trong memo. | Tôi phân biệt rõ: nguồn của Cursor chứng minh họ công bố gì, còn các kết luận như moat, segment shift hay nguyên nhân chiến lược là phần phân tích của tôi. Tôi không dùng nguồn để khẳng định những điều nguồn không chứng minh. |
| Rà soát memo theo rubric | AI hỗ trợ đóng vai trò reviewer, chỉ ra phần thiếu hoặc reasoning chưa rõ. Tôi quyết định có sửa hay không và chịu trách nhiệm với bản cuối. | Tôi tự kiểm lại 4 khối của rubric: 7 milestone có nguồn, JTBD theo việc cần làm, prediction dẫn được về phần trước và AI log phản ánh đúng quá trình thực tế. |
