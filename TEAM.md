# Team

> Điền file này trên repo chung do nhóm trưởng fork. Nhóm điền phần **Thông tin nhóm** và **Thành viên**. Mỗi người tự điền phần của mình trong **Cá nhân**. Không copy file này sang repo khác.

## Thông tin nhóm

- Tên nhóm: H2
- Candidate problem nhóm chọn (1 câu): Hỗ trợ GVCN THPT soạn nhận xét học bạ cá nhân hóa từ dữ liệu học tập và nề nếp, có giáo viên duyệt trước khi nhập sổ.
- Quyết định cuối (Go / Not Yet / No-Go): Go — thử nghiệm phạm vi nhỏ.

## Thành viên

| STT | Họ và tên       | MSSV        | Vai trò trong nhóm                                                                                                                                   | Tài khoản GitHub                  |
| --: | --------------- | ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------- |
|   1 | Đỗ Minh Thanh   | 2A202603793 | Đề xuất problem kỹ thuật; phản biện; tổng hợp khảo sát, xác định vấn đề; đối chiếu quy trình và Problem Statement.                                   | https://github.com/thd050810      |
|   2 | Nguyễn Đức Hiếu | 2A202603772 | Phản biện, vẽ quy trình trước/sau, viết Success Metric                                                                                               | [Hie24](https://github.com/Hie24) |
|   3 | Trần Thanh Hải  | 2A202603740 | Đề xuất problem nhận xét học bạ; phỏng vấn GVCN, research giải pháp; xây dựng quy trình trước/sau, Problem Statement, AI Canvas; chốt quyết định Go. | https://github.com/tran-hai21     |
|   4 | Nguyễn Mạnh Quân | 2A202603776 | Đề xuất problem, phản biện, khảo sát | [osgi23](https://github.com/osgi23) |


Không ghi email hay số điện thoại vào bảng này, vì repo có thể để public.

Gợi ý vai trò (một người có thể giữ nhiều vai): điều phối thời gian, ghi chép, người phản biện chính, phụ trách kiểm chứng (phỏng vấn/survey), phụ trách research, vẽ quy trình, viết Problem Statement.

## Phân công theo checkpoint

| Checkpoint                                 | Người chính     | Người hỗ trợ                                            | Sản phẩm                                       |
| ------------------------------------------ | --------------- | ------------------------------------------------------- | ---------------------------------------------- |
| CP3 — Hội tụ nhóm                          | Trần Thanh Hải  | Đỗ Minh Thanh; Nguyễn Đức Hiếu; Nguyễn Mạnh Quân        | Cluster, cây OST, bảng chấm điểm               |
| CP4 — Kiểm chứng                           | Nguyễn Mạnh Quân| Đỗ Minh Thanh                                           | Assumption map, snapshot hoặc survey           |
| CP4 — Research                             | Trần Thanh Hải  | Đỗ Minh Thanh; Nguyễn Mạnh Quân                         | Bảng research có link                          |
| CP5 — Quy trình trước/sau                  | Nguyễn Đức Hiếu | Trần Thanh Hải; Đỗ Minh Thanh                           | Quy trình + bảng before/after                  |
| CP5 — Problem Statement v0                 | Đỗ Minh Thanh   | Nguyễn Đức Hiếu (Success Metric); Đỗ Minh Thanh; Nguyễn Mạnh Quân         | Problem Statement v0                           |
| CP6 — Mức can thiệp + Problem Statement v1 | Nguyễn Mạnh Quân| Nguyễn Đức Hiếu (Workflow/Agent, metric); Đỗ Minh Thanh; Nguyễn Mạnh Quân | Ma trận, AI Canvas, eval, Problem Statement v1 |
| CP6 — Quyết định                           | Trần Thanh Hải  | Đỗ Minh Thanh; Nguyễn Đức Hiếu; Nguyễn Mạnh Quân        | 4 rủi ro + Go/Not Yet/No-Go                    |


## Cá nhân

Mỗi thành viên thêm một mục theo mẫu dưới đây, tiêu đề là `HoVaTen-MSSV`.

### DoMinhThanh-2A202603793

**Phần việc phụ trách:**

- Tự tìm ý tưởng, scan 10 problem và chọn 3 Problem Cards cá nhân để pitch.
- Phản biện các candidate của nhóm về độ chính xác dữ liệu, tính cá nhân hóa và công sức kiểm tra đầu ra.
- Tổng hợp khảo sát, xác định vấn đề và đối chiếu với quy trình, bottleneck, metric và boundary.
- Hoàn thiện báo cáo cá nhân và phần đóng góp của mình trong báo cáo nhóm; dùng AI hỗ trợ định dạng, chuyển sơ đồ và đối chiếu tài liệu. Tôi quyết định nội dung cá nhân cuối cùng; kết luận nhóm do cả nhóm thống nhất.

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Đưa ra 3 candidate: hiểu codebase có sẵn, tổng hợp tài liệu ôn thi và tổng hợp metrics experiment; tương ứng candidate #4, #5, #6 trong bảng pitch chung.
- Hỏi Hiếu liệu dữ liệu ngập có đủ mới để hỗ trợ chọn đường; hỏi Hải cách bảo đảm nhận xét đúng từng học sinh khi thời gian duyệt ngắn; hỏi Quân về nguy cơ AI bịa số liệu paper và công sức kiểm tra lại PDF.
- Tiếp nhận phản biện của Hiếu về việc chỉ đúng file/hàm trong codebase lớn, của Quân về tóm tắt tài liệu chính xác và của Hải về phương án dùng MLflow/Weights & Biases thay cho AI.
- Đối chiếu kết quả khảo sát nhóm để làm rõ nhu cầu giảm công soạn lời nhận xét, đồng thời giữ yêu cầu đúng dữ liệu và giáo viên duyệt. Phần đóng góp của tôi là tổng hợp và xác định vấn đề, không nhận toàn bộ hoạt động phỏng vấn là công việc cá nhân.
- Phân biệt thời gian soạn nhận xét 360 phút với tổng quy trình 480 phút/lớp; đối chiếu mục tiêu 45 phút và bước giáo viên rà soát trong quy trình tương lai.
- Đối chiếu phương án Workflow và ranh giới can thiệp: Rule xử lý bảng dữ liệu, AI gợi ý lời văn, giáo viên sửa/duyệt, rồi mới xuất file.
- Hoàn thiện 3 quy trình nháp cá nhân bằng Mermaid màu tối, thể hiện từng bước, thời gian và bottleneck.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- [Báo cáo cá nhân](report/individual/2A202603793_DoMinhThanh.md): mục 2 có 10 problem; mục 3 có top 3, Problem Cards và sơ đồ; mục 4 ghi đóng góp CP3–CP6; mục 5 ghi cách dùng AI; mục 6 là Reflection.


**Điều mình học được từ phần nhóm:**

- Pain có thật chưa đủ để kết luận cần AI: ghi và so sánh metrics có thể dùng công cụ thông thường trước khi cân nhắc LLM.
- Khi tổng hợp khảo sát, cần nối actor, bối cảnh, bottleneck và tác động để xác định một vấn đề cụ thể; không bắt đầu bằng tên giải pháp.
- Phải tính cả công sức kiểm tra và sửa đầu ra khi so sánh trước/sau. Bản nháp tạo nhanh chưa bảo đảm tổng thời gian công việc giảm.
- Với bài toán nhận xét học bạ, AI hỗ trợ diễn đạt; giáo viên kiểm tra dữ liệu, cân nhắc hoàn cảnh học sinh và quyết định nội dung cuối cùng.

### NguyenDucHieu-2A202603772

**Phần việc phụ trách:**

- Đóng góp 25% công việc nhóm.
- CP3: Pitch, phản biện, gom candidate và đánh giá bài phân loại rác.
- CP5: Trình bày quy trình trước/sau và phần Success Metric.
- CP6: Phân biệt Workflow/Agent, bổ sung metric cho Problem Statement v1.

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Chuẩn bị 5 problem và 3 Problem Card; bài phân loại rác vào shortlist, đạt 24/35 điểm.
- Đặt câu hỏi cho Thanh về xác định vị trí sửa code, Hải về giáo án sát thực tế và Quân về ưu tiên deadline.
- Trình bày quy trình hiện tại 480 phút/lớp và quy trình mục tiêu 45 phút/lớp; đánh dấu bottleneck và bước giáo viên duyệt.
- Viết Success Metric gồm thời gian, tỷ lệ duyệt và cách đo; làm rõ lý do Workflow phù hợp hơn Agent.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- [Báo cáo cá nhân — CP1, CP2 và đóng góp nhóm](report/individual/2A202603772_NguyenDucHieu.md), mục 2–4.
- Commit báo cáo cá nhân: `9f6301e`.
- [Bảng làm việc nhóm](https://docs.google.com/spreadsheets/d/1tuysS72h8ppkgcZ_ZOAsRUt2-Rr6lKC585fAPVwCIKo/edit?usp=sharing), các tab `CP3, CP4` và `CP5, CP6`.

**Điều mình học được từ phần nhóm:**

- Chọn bài toán dựa trên pain, phạm vi và khả năng đo; nhận diện rác chưa đủ nếu hạ tầng thu gom không phù hợp.
- Metric cần đo cả thời gian và chất lượng; AI chỉ viết nháp, giáo viên vẫn kiểm tra và quyết định.

### TranThanhHai-2A202603740

**Phần việc phụ trách:**

- Đề xuất và bảo vệ problem nhận xét học bạ cuối kỳ; pitch 3 Problem Cards cá nhân.
- Phản biện candidate của các thành viên; gom cluster, xây Opportunity Solution Tree và chấm điểm shortlist.
- Phụ trách kiểm chứng: phỏng vấn GVCN, tổng hợp khảo sát và research các giải pháp đã có.
- Xây dựng quy trình trước/sau, Problem Statement v0 → v1, AI Canvas, ma trận mức can thiệp và chốt quyết định Go.

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Pitch Card #1 — viết nhận xét học bạ theo Thông tư 22, phân tích bottleneck 360 phút/45 học sinh; card đạt 34/35 điểm và trở thành Candidate #10 của nhóm.
- Phỏng vấn sâu 1:1 một GVCN lớp 11, tổng hợp khảo sát 22 giáo viên: giáo viên chỉ muốn được hỗ trợ (augment), kiên quyết không giao việc duyệt nhận xét cho máy; template Excel/Mail Merge hiện có bị vỡ font và rập khuôn.
- Đóng góp 3 candidate vào Cluster A (tác vụ sư phạm), cùng nhóm xây OST với outcome giảm 70–90% thời gian tác vụ định kỳ và gạch bỏ các giải pháp đội lốt cơ hội.
- Vẽ quy trình hiện tại 480 phút/lớp và quy trình tương lai 45 phút/lớp, phân định rõ bước nào do Rule, AI hay giáo viên đảm nhận.
- Bổ sung tiêu chí chất lượng vào Problem Statement v1: độ trùng lặp văn bản < 5%, tỷ lệ giáo viên duyệt ≥ 80%, ẩn danh hóa PII trước khi gửi lên mô hình.
- Lập luận loại No AI/Rule/Agent để chọn mức Workflow, hoàn thiện AI Canvas, phân tích 4 rủi ro sản phẩm và đề xuất pilot 1 lớp với ngưỡng dừng khi tỷ lệ duyệt dưới 65%.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- [Báo cáo cá nhân](report/individual/2A202603740_TranThanhHai.md): mục 2 có 6 problem; mục 3 có top 3, Problem Cards và quy trình nháp; mục 4 ghi đóng góp CP3–CP7; mục 5 ghi cách dùng AI; mục 6 là Reflection.
- [Báo cáo nhóm](report/team/group_report.md): mục 2 (CP3), mục 3 (CP4), mục 4–5 (CP5), mục 6–8 (CP6).
- Commit báo cáo cá nhân: `d353087`.

**Điều mình học được từ phần nhóm:**

- Một vấn đề kỹ thuật "thời thượng" chưa chắc là bài toán AI tốt; bài toán tốt cần ranh giới dữ liệu rõ, quy trình lặp lại và tác động đo được.
- Người dùng muốn được hỗ trợ để bớt kiệt sức, không muốn bị thay thế; ranh giới Human-in-the-loop là yêu cầu đạo đức và pháp lý, không chỉ là lựa chọn thiết kế.
- Tốc độ nhanh mà chất lượng đầu ra kém thì không có giá trị, nên metric phải đo cả thời gian, độ cá nhân hóa và tỷ lệ duyệt.
- Viết Problem Statement khó nhất là giữ kỷ luật tách vấn đề khỏi giải pháp; khi gạt bỏ lớp vỏ công nghệ, bài toán mới rõ và dễ đánh giá.

### NguyenManhQuan-2A202603776

**Phần việc phụ trách:**
Đóng góp 25% công việc nhóm.
- CP3: Pitch 3 Problem Card cá nhân (Card #1 về paper lọt shortlist top 2 với 30/35 điểm); phản biện các candidate khác; đồng thuận chọn bài học bạ.
- CP4: Phụ trách chính phần Research giải pháp kỹ thuật đã có (test ChatGPT/Claude web chat, phân tích Excel Mail Merge và gợi ý vnEdu).
- CP5: Thiết lập ranh giới kỹ thuật (Boundary) và cơ chế dự phòng (Fallback) về Google Sheets.
- CP6: Xây dựng bộ 3 tiêu chí đánh giá đầu ra (Eval criteria), trả lời câu hỏi Google PAIR, phân tích tính khả thi/chi phí và thiết lập ngưỡng dừng an toàn.

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):
- Chuẩn bị 5 problem scan và 3 Problem Card: Card #1 (Bóc tách paper PDF), Card #2 (Ưu tiên bài tập dồn deadline), Card #3 (Tìm snippet/lời giải Discord).
- Đặt câu hỏi phản biện cho Hiếu về rào cản hạ tầng rác thải; Thanh về tóm tắt ôn thi; Hải về tính phân hóa và độ chính xác của câu hỏi kiểm tra.
- Tiếp nhận phản biện của Thanh về rủi ro ảo giác số liệu paper và nhận thấy chi phí kiểm tra lại PDF quá cao; chủ động rút bài cá nhân để ủng hộ chọn bài toán học bạ của Hải vì dữ liệu bảng Excel chuẩn hóa hơn.
- Hoàn thiện bảng Research giải pháp có sẵn: thử nghiệm nhập dữ liệu vào ChatGPT/Claude để chứng minh rào cản thao tác lặp 45 lần, nguy cơ lộ PII và văn phong lệch chuẩn Thông tư 22 
→ khẳng định cần giải pháp Batch Workflow.
- Xác định điểm can thiệp AI tại Bước 3 và thiết lập cơ chế fallback tự động chuyển về Rule-based template trên Google Sheets nếu AI gặp lỗi.
- Đóng góp vào Problem Statement v1: bổ sung ranh giới ẩn danh hóa 100% PII, gắn cờ các ca học sinh đặc biệt; thiết kế 3 tiêu chí eval

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):
- Báo cáo cá nhân: mục 2 scan; mục 3 có 3 Problem Cards; mục 4 đóng góp CP3–CP6; mục 5 dùng AI; mục 6 Reflection.
- Báo cáo nhóm group_report.md: Bảng pitch CP3 (Candidate #7, #8, #9); Shortlist CP3; Bảng research CP4 (mục 3.3); Tiêu chí đánh giá eval (mục 7) và Ngưỡng dừng an toàn (mục 8.2).

**Điều mình học được từ phần nhóm:**
- Bài toán AI tốt không phải bài toán dùng công nghệ phức tạp, mà cần ranh giới dữ liệu rõ ràng, quy trình chuẩn mực và đo lường được giá trị thực tế.
- Tách bạch rõ ràng giữa Nhu cầu người dùng và Giải pháp kỹ thuật khi dựng cây OST; không để công nghệ dẫn dắt định nghĩa bài toán.
- Trong giáo dục, người dùng chỉ muốn được hỗ trợ soạn nháp (Augment), tuyệt đối không giao phó việc đánh giá con người cho AI (Automate); luôn phải có cơ chế Human-in-the-loop và phương án fallback an toàn.
