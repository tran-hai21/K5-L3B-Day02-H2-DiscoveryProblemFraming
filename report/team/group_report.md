# Báo cáo nhóm — Day 02 Discovery & Problem Framing

> Bản chung của nhóm, viết trên repo do nhóm trưởng fork. Không copy file này sang repo cá nhân.
> Template chi tiết và prompt mẫu: [docs/01-worksheet.md](../../docs/01-worksheet.md). Bài mẫu: [docs/02-deliverable-example.md](../../docs/02-deliverable-example.md).

## 1. Thông tin nhóm

- Tên nhóm: H2
- Thành viên: xem `TEAM.md`
- Candidate problem được chọn (1 câu): Khi đến hạn khóa sổ học bạ điện tử cuối kỳ, tôi muốn tổng hợp dữ liệu học tập và nề nếp của từng học sinh để viết lời nhận xét phẩm chất - năng lực riêng biệt, để nộp đúng hạn mà không sao chép rập khuôn.
- Quyết định cuối: Go

---

## 2. Hội tụ nhóm (CP3)

### 2.1. Pitch

|   # | Người đưa ra | Candidate (Job Story ngắn)                                                                                                                                                                                                                                      | Actor                                                                                                                    | Bottleneck                                                                                                                                                                     | Câu hỏi phản biện nhận được (ai hỏi)                                                                                                                                                                                                                                                             |
| --: | ------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
|   1 | Hiếu         | Khi xử lý rác hằng ngày, tôi muốn biết nhóm rác và nơi bỏ, để tránh phân loại sai hoặc làm lại.<br>                                                                                                                                                             | Cư dân khu đô thị / chung cư có quy định phân loại rác.                                                                  | Bước tách rác - Xác định & tách nhóm rác (4 phút/lượt).                                                                                                                        | "Khó do người dân thiếu kiến thức hay do hệ thống thu gom chưa đồng bộ?" (Quân)                                                                                                                                                                                                                  |
|   2 | Hiếu         | Khi đi lại lúc mưa lớn, tôi muốn biết đường ngập hoặc có nguy cơ ngập, để chọn hành trình an toàn hơn.                                                                                                                                                          | Người đi làm, sinh viên, tài xế tại đô thị thường xuyên ngập úng.                                                        | Bước tìm tin ngập - Tìm thông tin ngập bị phân tán trên nhiều nguồn (7 phút/lượt).                                                                                             | "Dữ liệu điểm ngập có đủ mới và cập nhật kịp thời theo thời gian thực không?" (Thanh)                                                                                                                                                                                                            |
|   3 | Hiếu         | Khi tìm kiếm căn hộ để thuê/mua, tôi muốn tổng hợp và so sánh đa tiêu chí (giá, vị trí, tiện ích, pháp lý), để chọn được căn hộ phù hợp nhất mà không tốn công ghi chép thủ công.                                                                               | Người đi làm, gia đình trẻ có nhu cầu tìm thuê hoặc mua căn hộ tại đô thị.                                               | Bước chuẩn hóa và lập bảng so sánh - Chuẩn hóa và so sánh dữ liệu từ nhiều nguồn/trang web (15 phút/lượt).                                                                     | "Dữ liệu tin đăng bất động sản thường phân mảnh, thiếu chuẩn xác hoặc trùng lặp thì kiểm soát thế nào?" (Hải)                                                                                                                                                                                    |
|   4 | Thanh        | Khi tiếp nhận một codebase có sẵn, tôi muốn hiểu nhanh kiến trúc và luồng xử lý dữ liệu, để biết chính xác cần sửa code ở đâu.                                                                                                                                  | Developver                                                                                                               | Mất khoảng 60 - 120 phút để đọc code, lần theo dependency và hiểu luồng dữ liệu.                                                                                               | AI có thể xác định chính xác vị trí cần sửa trong codebase lớn không?(Hiếu)                                                                                                                                                                                                                      |
|   5 | Thanh        | Khi ôn thi, tôi muốn tổng hợp kiến thức từ slide, giáo trình và bài giảng, để không bỏ sót nội dung quan trọng.                                                                                                                                                 | Sinh viên                                                                                                                | Mất khoảng 3 - 5 giờ/môn để đọc, đối chiếu và tổng hợp tài liệu từ 8 - 12 chương.                                                                                              | Làm sao đảm bảo AI không bỏ sót kiến thức hoặc tóm tắt sai nội dung?(Quân)                                                                                                                                                                                                                       |
|   6 | Thanh        | Khi thử nghiệm nhiều model, tôi muốn tự động lưu accuracy, precision, recall, F1, latency và cost, để không phải ghi kết quả thủ công.                                                                                                                          | AI Engineer                                                                                                              | Mất khoảng 20 - 30 phút mỗi đợt thử nghiệm 3-5 model để ghi lại và tổng hợp metrics thủ công.                                                                                  | Tại sao cần AI khi MLflow hoặc Weights & Biases đã hỗ trợ ghi log và so sánh experiment?(Hải)                                                                                                                                                                                                    |
|   7 | Quân         | Khi nhận đề tài đồ án/khóa luận có nhiều paper dài (10–20 trang PDF), tôi muốn nhanh chóng trích xuất bài toán, phương pháp, bộ dữ liệu và kết quả benchmark chính của từng bài vào bảng đối chiếu, để chọn đúng baseline và viết tổng quan đề tài kịp tiến độ. | Sinh viên năm 4 ngành Khoa học Máy tính làm đồ án tốt nghiệp / nghiên cứu khoa học.                                      | Đọc sâu kiến trúc và đối chiếu kết quả thực nghiệm (70'/paper); dễ bị ngợp bởi thuật ngữ toán, phải đọc đi đọc lại để nhặt đúng con số so sánh.                                | "Paper toàn công thức toán với bảng biểu phức tạp, nếu AI hallucinate bịa số thì có mất thêm thời gian đi dò lại PDF gốc không?" (Thanh)                                                                                                                                                         |
|   8 | Quân         | Khi có nhiều bài tập lớn và đồ án dồn cùng một tuần hạn, tôi muốn nhanh chóng đánh giá độ khó kỹ thuật và sắp xếp thứ tự ưu tiên thực hiện, để không bỏ sót bài có hạn chót sớm và tối ưu hóa điểm số.                                                          | Sinh viên năm 4 ngành Khoa học Máy tính học song song nhiều môn chuyên ngành và đồ án.                                   | Ước lượng công sức và cân nhắc độ ưu tiên (25'/lần); dễ bị rối trí và tê liệt quyết định (decision paralysis) do không rõ task nào tốn nhiều thời gian debug/train model hơn.  | "Chỉ cần sort deadline theo thứ tự tăng dần là xong, với lại sinh viên trễ hạn là do lười chứ AI xếp lịch hộ thì chắc gì đã chịu làm theo?" (Hiếu)                                                                                                                                               |
|   9 | Quân         | Khi gặp lỗi code hoặc cần tài liệu tham khảo cũ đã từng trao đổi, tôi muốn tìm lại chính xác tin nhắn hướng dẫn, ảnh chụp lỗi hoặc snippet code trên Discord, để giải quyết ngay vấn đề kỹ thuật mà không cần hỏi lại mentor hay bạn bè.                        | Sinh viên năm 4 ngành Khoa học Máy tính sinh hoạt trong các nhóm lab nghiên cứu, kênh Discord môn học hoặc server đồ án. | Cuộn đọc ngữ cảnh và xác nhận đúng giải pháp (15'/lần); tìm kiếm mặc định chỉ trả về tin nhắn lẻ tẻ, không tóm tắt ngữ cảnh câu trả lời hoàn chỉnh nằm ở đâu trong luồng chat. | "Nếu người hỏi không nhớ đúng từ khóa thì tìm kiểu gì, và làm bot index chat có bị vi phạm quyền riêng tư của server không?" (Hải)                                                                                                                                                               |
|  10 | Hải          | Khi đến hạn khóa sổ học bạ điện tử cuối kỳ, tôi muốn tổng hợp dữ liệu học tập và nề nếp của từng học sinh để viết lời nhận xét phẩm chất - năng lực riêng biệt, để nộp đúng hạn mà không sao chép rập khuôn.                                                    | Giáo viên chủ nhiệm THPT (quản lý 40 - 45 học sinh/lớp).                                                                 | Soạn nhận xét cá nhân hóa từng học sinh - mất **360 phút / 45 em** (khoảng 8 phút/em).                                                                                         | làm thế nào để hệ thống đảm bảo nhận xét cá nhân hóa đúng với từng học sinh, tránh tạo ra những nhận xét chung chung hoặc sai lệch khi giáo viên chỉ cần rà soát trong thời gian ngắn? (Thanh)                                                                                                   |
|  11 | Hải          | Khi chuẩn bị kiểm tra giữa kỳ hoặc cuối kỳ, tôi muốn thiết kế câu hỏi bám sát ma trận 4 mức độ nhận thức kèm ngữ liệu thực tế, để nộp tổ chuyên môn duyệt đúng hạn mà không bị trùng lặp đề cũ.                                                                 | Giáo viên bộ môn THPT (Toán, Ngữ văn, KHTN, KHXH).                                                                       | Biên soạn câu hỏi trắc nghiệm bám sát 4 mức độ nhận thức - mất **180 phút / bộ đề 40 câu**.                                                                                    | Làm thế nào để đảm bảo các câu hỏi do AI tạo ra không chỉ đúng với ma trận 4 mức độ nhận thức về mặt hình thức, mà còn thực sự đánh giá đúng năng lực học sinh, có độ phân hóa phù hợp và không chứa sai sót về kiến thức chuyên môn? (Quân)                                                     |
|  12 | Hải          | Khi chuẩn bị giáo án cho tuần dạy mới, tôi muốn chuyển đổi nội dung sách giáo khoa thành 4 pha hoạt động học kèm phiếu học tập chi tiết, để đạt chuẩn thanh tra chuyên môn và học sinh có hoạt động rõ ràng trên lớp.                                           | Giáo viên bộ môn THPT (đặc biệt là giáo viên trẻ dưới 5 năm kinh nghiệm).                                                | Soạn chi tiết nội dung và câu lệnh cho 4 pha hoạt động dạy học - mất **80 phút / giáo án 2 tiết**.                                                                             | Làm thế nào để đảm bảo 4 pha hoạt động do AI thiết kế không chỉ đáp ứng yêu cầu về hình thức giáo án và hồ sơ thanh tra, mà còn phù hợp với trình độ thực tế của học sinh, điều kiện lớp học và thời lượng giảng dạy, tránh tình trạng giáo án đầy đủ nhưng khó triển khai trong thực tế? (Hiếu) |

### 2.2. Cluster

| Cluster                                   | Các candidate                          | Pattern chung                                                                                                                                                                                                                                              |
| ----------------------------------------- | -------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| A - Tác vụ sư phạm & giáo dục             | Candidate 10, 11, 12 (Hải)             | Giáo viên THPT chịu áp lực thời gian lớn từ các công việc hành chính sư phạm định kỳ lặp lại theo khuôn mẫu/quy chuẩn chặt chẽ (soạn nhận xét học bạ, đề thi ma trận 4 mức độ, giáo án 4 pha), tốn 80-360 phút/đợt nhưng vẫn đòi hỏi tính cá nhân hóa cao. |
| B - Bóc tách & tổng hợp tri thức kỹ thuật | Candidate 4, 5, 6 (Thanh); 7, 9 (Quân) | Developer, Kỹ sư AI và Sinh viên CNTT bị quá tải thông tin kỹ thuật lớn, phi cấu trúc (codebase nhiều file, slide/giáo trình ôn thi, metrics experiment, paper PDF, tin nhắn lỗi Discord); mất nhiều giờ đọc - lọc - đối chiếu thủ công.                   |
| C - Hỗ trợ ra quyết định & tối ưu cá nhân | Candidate 1, 2, 3 (Hiếu); 8 (Quân)     | Người dùng đô thị và sinh viên gặp khó khăn khi ra quyết định hàng ngày do thông tin phân tán, thiếu chuẩn hóa hoặc bị tê liệt quyết định khi có quá nhiều tiêu chí/nhiệm vụ (phân loại rác, tìm đường ngập, so sánh căn hộ, xếp lịch bài tập).            |

### 2.3. Opportunity Solution Tree rút gọn

Gốc là **1 outcome**. Nhánh là **opportunity** (nhu cầu, pain), không phải tính năng hay công cụ.

```text
OUTCOME: Giảm 70%–90% thời gian xử lý các tác vụ xử lý thông tin định kỳ lặp lại cho người dùng mục tiêu mà vẫn đảm bảo tính chính xác và cá nhân hóa.
├── Opportunity A: Giáo viên THPT cần hoàn thành nhận xét học bạ và kế hoạch bài dạy đúng hạn khóa sổ mà không bị rập khuôn hay kiệt sức.
├── Opportunity B: Developer và Sinh viên CNTT cần bóc tách nhanh thông số kỹ thuật cốt lõi từ codebase và paper nghiên cứu để kịp tiến độ công việc.
└── Opportunity C: Developer và Sinh viên CNTT cần bóc tách nhanh thông số kỹ thuật cốt lõi từ codebase và paper nghiên cứu để kịp tiến độ công việc.
```

Những ý đã gạch bỏ vì là solution đội lốt opportunity:

- Xây dựng chatbot AI tạo lời nhận xét học bạ tự động" (Solution đội lốt -> Đã loại vì đóng khung vào công cụ LLM chatbot; Opportunity thực sự: Cần giảm tải thời gian soạn nhận xét cá nhân hóa đúng hạn cho GVCN).
- Làm app quét ảnh nhận diện phân loại rác đô thị" (Solution đội lốt -> Đã loại vì đóng khung vào app Computer Vision; Opportunity thực sự: Cần biết nhanh nhóm rác và nơi bỏ đúng quy định tại nguồn).
- Xây dựng pipeline RAG bóc tách bảng số liệu từ paper PDF" (Solution đội lốt -> Đã loại vì đóng khung vào giải pháp RAG kỹ thuật; Opportunity thực sự: Cần trích xuất nhanh thông số benchmark đối chiếu baseline).

### 2.4. Chấm điểm shortlist (1–5)

| Candidate                                        | Actor rõ | Quy trình rõ | Pain có bằng chứng | Impact đo được | Vừa sức lab | So sánh được No AI/Rule/Workflow/Agent | Nhóm hiểu domain | Tổng |
| ------------------------------------------------ | -------: | -----------: | -----------------: | -------------: | ----------: | -------------------------------------: | ---------------: | ---: |
| #10 - Nhận xét học bạ THPT cá nhân hóa (Hải)     |        5 |            5 |                  5 |              5 |           5 |                                      4 |                4 |   34 |
| #7 - Trích xuất thông số paper nghiên cứu (Quân) |        5 |            4 |                  4 |              4 |           4 |                                      4 |                5 |   30 |
| #1 - Hỗ trợ phân loại rác tại nguồn (Hiếu)       |        4 |            4 |                  3 |              3 |           3 |                                      4 |                3 |   24 |

**Candidate được chọn:** Candidate #10 - Hỗ trợ giáo viên chủ nhiệm THPT soạn lời nhận xét học bạ điện tử cá nhân hóa (Hải)

**Vì sao chọn:**
- Điểm tổng shortlist cao nhất (34/35 điểm), đáp ứng xuất sắc cả 7 tiêu chí đánh giá.
- Actor & Quy trình cực kỳ rõ ràng: Giáo viên chủ nhiệm THPT (40-45 học sinh/lớp); quy trình 5 bước gắn liền với kỳ khóa sổ dữ liệu vnEdu/SMAS định kỳ.
- Bottleneck & Nỗi đau có bằng chứng thực tế: Mất 360 phút / 45 học sinh (8 phút/em); giáo viên thường kiệt sức 2-3 đêm cuối kỳ hoặc phải dùng mẫu câu rập khuôn sáo rỗng.
- Impact đo lường cụ thể: Giảm thời gian hoàn thành từ 480 phút xuống 45 phút (~90%).
- Tính khả thi cao trong lab: Dữ liệu đầu vào dạng bảng có cấu trúc kết hợp chuẩn hành văn sư phạm Thông tư 22 rất phù hợp để xây dựng giải pháp Workflow + LLM.

**Vì sao loại các candidate còn lại:**
- Loại Candidate #1 (Phân loại rác - 24/35): Phụ thuộc lớn vào hạ tầng thu gom rác bên ngoài; việc thu thập tập dữ liệu ảnh và kiểm thử Computer Vision trong thực tế vượt quá phạm vi và thời gian của buổi lab.
- Loại Candidate #7 (Trích xuất paper - 30/35): Bài toán thiết thực với sinh viên CNTT nhưng xử lý PDF chứa công thức toán và bảng biểu phức tạp có rủi ro cao bị hallucination số liệu thực nghiệm, mất nhiều thời gian rà soát lại so với bài toán học bạ.

**Xử lý bất đồng (nếu có):**
- Băn khoăn ban đầu: Nhóm phân vân giữa Candidate #10 (bài toán sư phạm của Hải) và Candidate #7 (bài toán đọc paper của Quân) vì các thành viên đều là dân kỹ thuật nên hiểu sâu nỗi đau đọc paper hơn.
- Thống nhất giải quyết: Hải đóng vai trò chuyên gia miền (domain expert) cung cấp mẫu dữ liệu thực tế và chuẩn Thông tư 22; cả nhóm thống nhất Candidate #10 có quy trình chuẩn hóa cao hơn, ranh giới rõ ràng và dễ demo thành công hơn trong lab.

---

## 3. Kiểm chứng + research giải pháp đã có (CP4)

### 3.1. Assumption Map

|   # | Giả định                                                                                                                                                               | Loại (Value / Usability / Feasibility / Viability) | Quan trọng (1–5) | Đã có bằng chứng (1–5) | Kiểm chứng trước? |
| --: | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------- | ---------------: | ---------------------: | ----------------- |
|   1 | GVCN THPT thực sự coi việc soạn nhận xét học bạ cuối kỳ là gánh nặng lớn và sẵn sàng dùng công cụ AI hỗ trợ nếu nhận xét thể hiện đúng tính cách/tiến bộ của học sinh. | Value                                              |                5 |                      3 | Có                |
|   2 | AI có thể tạo nhận xét chuẩn ngôn phong sư phạm Thông tư 22 dựa trên bảng điểm và ghi chú vắn tắt mà không bị rập khuôn hay sai lệch thông tin học sinh.               | Feasibility                                        |                5 |                      2 | Có                |
|   3 | Giáo viên dễ dàng tải file Excel/bảng điểm vnEdu/SMAS lên hệ thống và thao tác rà soát, chỉnh sửa nhanh mà không gặp rào cản công nghệ.                                | Usability                                          |                4 |                      3 | Không             |
|   4 | Quy định ngành và nhà trường cho phép ứng dụng công cụ hỗ trợ soạn thảo, miễn là giáo viên chịu trách nhiệm kiểm duyệt cuối cùng trước khi vào sổ.                     | Viability                                          |                4 |                      2 | Không             |
|   5 | Tiết kiệm ~80–90% thời gian (từ 360 phút xuống 45 phút/lớp) giúp GVCN giải tỏa kiệt sức cuối kỳ và nâng cao chất lượng đánh giá học sinh.                              | Value                                              |                5 |                      4 | Không             |
|   6 | Dữ liệu xuất từ vnEdu/SMAS có định dạng đủ chuẩn hóa để trích xuất tự động điểm số và nề nếp mà không cần xử lý thủ công phức tạp.                                     | Feasibility                                        |                4 |                      3 | Không             |




### 3.2. Kiểm chứng

Cách đã dùng: Phỏng vấn sâu 1:1 (3 GVCN THPT) kết hợp Khảo sát định lượng (22 giáo viên THPT)

Interview snapshot (mỗi buổi phỏng vấn một bảng, hoặc đặt file trong `report/assets/cp4-interview-snapshot-N.md`):

| Trường                                            | Nội dung                                                                                                                                                                                                                                                               |
| ------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Người được hỏi (vai trò, không ghi tên thật)      | Giáo viên chủ nhiệm lớp 11 trường THPT công lập (kinh nghiệm 8 năm giảng dạy, chủ nhiệm lớp 44 học sinh).                                                                                                                                                              |
| Câu nói đáng nhớ nhất (nguyên văn)                | "Đến đêm thứ ba ngồi gõ nhận xét học bạ, tôi kiệt sức đến mức chỉ muốn copy câu 'Chăm ngoan, có ý thức' dán cho tất cả các em còn lại cho xong trước giờ hệ thống khóa sổ."                                                                                            |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? | Cuối học kỳ 2 năm học trước: Cổng vnEdu mở hạn khóa điểm và nhận xét vào 23:59 Chủ Nhật. Cô phải chấm thi xong mới bắt đầu viết nhận xét cho 44 học sinh, thức trắng 2 đêm liền từ thứ Sáu đến Chủ Nhật, mắt mỏi nhừ và căng thẳng vì sợ sót em có hoàn cảnh đặc biệt. |
| Hiện đang xử lý bằng cách nào (workaround)?       | Tạo 1 file Excel lưu sẵn khoảng 10 mẫu câu chung chung phân loại theo mức học lực (Tốt, Khá, Đạt, Chưa đạt), sau đó copy vào hệ thống rồi cố gắng sửa thêm 1 vài chữ cho các học sinh cá biệt hoặc có chuyển biến rõ rệt.                                              |
| Mất bao lâu, bao lần?                             | Mất khoảng 6-8 giờ (khoảng 360-480 phút) mỗi đợt cuối kỳ, làm 2 lần/năm học (học kỳ 1 và cuối năm). Thường phải dồn làm liên tục vào ban đêm ngoài giờ lên lớp.                                                                                                        |
| Insight / opportunity rút ra                      | GVCN không hề muốn nhận xét sáo rỗng vì rất thương học sinh, nhưng bị áp lực deadline đè bẹp. Giáo viên không cần một chatbot tự do mà cần một quy trình tự động ráp dữ liệu điểm + hạnh kiểm ra bản nháp chuẩn Thông tư 22 để họ chỉ việc duyệt và tinh chỉnh.        |

Tổng hợp:

| Nguồn                   |                                                      Số người / số mẫu | Tín hiệu xác nhận                                                                                                                                                                                         | Tín hiệu phản bác                                                                                                                                    |
| ----------------------- | ---------------------------------------------------------------------: | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| Phỏng vấn 1:1           |                                             3 giáo viên chủ nhiệm THPT | 100% (3/3) khẳng định viết nhận xét học bạ là việc mệt mỏi nhất cuối kỳ; mong muốn có công cụ gợi ý lời văn đúng chuẩn quy định nhưng vẫn thể hiện nét riêng của từng em.                                 | 1/3 lo ngại nếu AI viết quá hoa mỹ hoặc dùng từ ngữ không đúng thực tế sẽ bị phụ huynh phản ánh hoặc tổ chuyên môn nhắc nhở.                         |
| Khảo sát (Survey)       |                             22 giáo viên THPT (18 người từng làm GVCN) | 86.4% (19/22) mất trên 5 giờ cho mỗi đợt nhận xét học bạ; 90.9% (20/22) thừa nhận từng phải dùng mẫu câu rập khuôn để kịp hạn; 81.8% sẵn sàng dùng công cụ tự động hóa nếu tiết kiệm được >70% thời gian. | 13.6% (3/22) e ngại việc tải dữ liệu điểm học sinh lên công cụ online có thể vi phạm bảo mật dữ liệu học đường hoặc giao diện quá phức tạp khó dùng. |
| Quan sát / Log / Ticket | 5 đợt khóa sổ thực tế trên diễn đàn giáo viên & nhóm hỗ trợ vnEdu/SMAS | Các bài đăng hỏi xin "bộ mẫu nhận xét học bạ theo Thông tư 22" thu hút hàng nghìn lượt tải và thảo luận vào mỗi tuần cao điểm khóa sổ (tháng 12 và tháng 5).                                              | Nhiều giáo viên phản ánh các bộ template Excel macro/Mail Merge trên mạng hay bị lỗi font tiếng Việt, lỗi định dạng khi paste vào hệ thống vnEdu.    |

**Nhóm đã sửa problem thế nào sau kiểm chứng:**
• Chuyển trọng tâm từ "sinh nhận xét tự động bằng chatbot tự do" sang "Quy trình trích xuất dữ liệu bảng điểm + sinh nhận xét bám sát ma trận năng lực/phẩm chất của Thông tư 22 kèm cơ chế Human-in-the-loop (giáo viên duyệt từng em)".
• Bổ sung yêu cầu bảo mật: Không yêu cầu tải lên họ tên đầy đủ/thông tin định danh nhạy cảm của học sinh (chỉ xử lý theo mã số/ID hoặc xử lý trực tiếp trên trình duyệt của giáo viên).
• Cung cấp định dạng xuất tương thích 1-click để copy trực tiếp vào vnEdu/SMAS mà không bị vỡ định dạng hay lỗi font.
### 3.3. Research giải pháp đã có

| Công cụ / case / pattern                                     | Link                                     | Giải bước nào trong quy trình?                 | Điểm mạnh                                                                                                | Khoảng trống / rủi ro                                                                                                                                    | Bài học cho nhóm                                                                                                                                         |
| ------------------------------------------------------------ | ---------------------------------------- | ---------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Excel Template + VLOOKUP / Mail Merge (Cộng đồng GV chia sẻ) | Diễn đàn GV                              | Bước 3: Soạn lời nhận xét học sinh             | Miễn phí, xử lý offline bảo mật dữ liệu, điền hàng loạt rất nhanh theo thang điểm có sẵn.                | Nhận xét máy móc, sáo rỗng; các học sinh cùng mức điểm bị trùng lặp 100% câu chữ; không phản ánh được phẩm chất hay tiến bộ riêng.                       | Phải giữ được ưu điểm xử lý dạng bảng hàng loạt nhưng đưa AI vào để đa dạng hóa văn phong và lồng ghép ghi chú thực tế của GVCN.                         |
| Tính năng "Gợi ý nhận xét" trên vnEdu / SMAS                 | https://vnedu.vn                         | Bước 3 & 5: Soạn và nhập nhận xét vào hệ thống | Tích hợp trực tiếp trên nền tảng chính thức của trường/Sở, không lo lỗi định dạng hay xung đột phần mềm. | Ngân hàng câu nghèo nàn, cứng nhắc; không tự động đối chiếu điểm số với nề nếp; giáo viên vẫn phải thao tác chọn thủ công từng em.                       | Định vị giải pháp như một công cụ hỗ trợ chuẩn bị dữ liệu (Copilot), tối ưu định dạng đầu ra để dán nhanh 1-click vào vnEdu thay vì thay thế nền tảng.   |
| ChatGPT / Claude (Sử dụng prompt thủ công trên Web Chat)     | https://chatgpt.com \| https://claude.ai | Bước 3 & 5: Soạn và nhập nhận xét vào hệ thống | Lời văn tự nhiên, uyển chuyển, cá nhân hóa linh hoạt theo từng đặc điểm học sinh nếu biết cách prompt.   | Thao tác thủ công từng em rất chậm (40–45 lần copy-paste); dễ rò rỉ thông tin cá nhân; văn phong dễ lệch chuẩn Thông tư 22 nếu thiếu kinh nghiệm prompt. | Xây dựng Batch Workflow tự động xử lý cả lớp cùng lúc với System Prompt chuẩn hóa sư phạm, loại bỏ thao tác chat thủ công và bảo mật danh tính học sinh. |

---

## 4. Quy trình trước/sau (CP5)

### 4.1. Quy trình hiện tại

Sơ đồ (ASCII, Mermaid hoặc link ảnh trong `report/assets/`):

```text
• QUY TRÌNH HIỆN TẠI (Tổng: 480 phút / 45 HS):
  [1. Xuất dữ liệu: 15'] (Con người - Xuất bảng điểm tổng hợp & nề nếp từ vnEdu/SMAS) 
  → [2. Phân loại: 45'] (Con người - Đọc & lọc nhóm học sinh Giỏi/Khá/TB/Yếu, nề nếp tốt/cá biệt) 
  → [3. Soạn nhận xét: 360'] (Con người - Soạn lời nhận xét thủ công từng em, ~8'/em) ← [BOTTLENECK] 
  → [4. Rà soát trùng lặp: 40'] (Con người - Đọc đối chiếu tránh trùng lặp từ ngữ giữa các học sinh) 
  → [5. Nhập liệu sổ: 20'] (Con người - Copy-paste từng lời phê vào hệ thống vnEdu/SMAS).

```



### 4.2. Quy trình tương lai

Ghi rõ bước nào **Rule**, bước nào **AI**, bước nào **con người**, **boundary** ở đâu, **phương án quay về** khi AI sai.

```text
• QUY TRÌNH TƯƠNG LAI (Mục tiêu: 45 phút / 45 HS - Giảm ~90%):
  [1. Tải bảng điểm: 5'] (Con người - Tải file Excel ẩn danh hóa PII của học sinh) 
  → [2. Phân tích & Trích xuất đặc trưng: 5'] (Rule - Tự động phân loại dải điểm & tổng hợp điểm trừ/nề nếp) 
  → [3. Sinh bản nháp nhận xét: 10'] (AI/LLM - Sinh lời nhận xét cá nhân hóa bám sát chuẩn phẩm chất - năng lực Thông tư 22) 
  → [4. Rà soát & Tinh chỉnh: 20'] (Con người [Human-in-the-loop] - GVCN duyệt từng em, điều chỉnh theo quan sát thực tế) 
  → [5. Xuất & Đồng bộ: 5'] (Rule - Xuất file tương thích 1-click import hoặc copy hàng loạt vào vnEdu/SMAS).
```




---

## 5. Problem Statement v0 (CP5)

• PROBLEM STATEMENT v0:
  - Actor: Giáo viên chủ nhiệm THPT (quản lý 40-45 học sinh/lớp).
  - Bối cảnh: 1–2 tuần trước hạn khóa sổ học bạ điện tử vnEdu/SMAS học kỳ 1 & cuối năm.
  - Pain point: Mất 360-480 phút/đợt để viết nhận xét thủ công cho 45 em, giáo viên kiệt sức, nhận xét rập khuôn sáo rỗng ("Chăm ngoan, cần cố gắng"), mất tính sư phạm định hướng.
  - Hướng tiếp cận v0 ban đầu: Sử dụng chatbot AI tự do để gõ prompt tạo nhận xét từng em.


Phản biện nhận được (từ AI hoặc nhóm khác) và nhóm có đồng ý không:

-

---

## 6. Mức can thiệp AI (CP6)

### 6.1. Ma trận độ mơ hồ × độ phức tạp

Bài của nhóm nằm ở ô: Độ mơ hồ: Trung bình (Medium Ambiguity) × Độ phức tạp: Trung bình - Cao (Medium-High Complexity)

Vì sao: 
• Về độ mơ hồ (Trung bình): Khung đánh giá được định hình rất chặt chẽ bởi Thông tư 22 (ma trận phẩm chất, năng lực, mức xếp loại), nhưng đầu ra là văn bản tự nhiên mang tính sư phạm cá nhân hóa nên cần độ linh hoạt ngôn ngữ, không thể giải quyết triệt để chỉ bằng mẫu câu ghép cố định.
• Về độ phức tạp (Trung bình - Cao): Cần tích hợp nhiều nguồn dữ liệu (điểm số nhiều môn, nề nếp, điểm cộng/trừ, ghi chú riêng của GVCN), trích xuất đặc trưng và sinh lời nhận xét nhất quán, sau đó cho phép giáo viên tinh chỉnh và xuất dữ liệu tương thích với vnEdu/SMAS.

### 6.2. So sánh 4 mức

| Mức                       | Phương án cho bài của nhóm                                                                                                                                                              | Đủ khi nào                                                                                                                                                   | Rủi ro                                                                                                                                             | Chọn? |
| ------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------- | ----- |
| **No AI** (sửa quy trình) | Xây dựng bộ tài liệu hướng dẫn và bảng mẫu Excel gồm 15–20 mẫu câu nhận xét phân loại sẵn theo mức học lực để giáo viên tự tra cứu, sao chép.                                           | Đủ khi lớp có sĩ số rất ít (<15 HS) hoặc giáo viên có nhiều thời gian, không bị áp lực khóa sổ gấp.                                                          | Vẫn tốn 6–8 giờ gõ/copy thủ công; lời phê rập khuôn sáo rỗng, triệt tiêu tính cá nhân hóa sư phạm.                                                 | Không |
| **Rule**                  | Dùng Google Sheets / Excel hàm lồng (IF, VLOOKUP) hoặc Macro để ghép chuỗi câu tự động theo dải điểm và hạnh kiểm.                                                                      | Đủ khi chỉ cần tạo báo cáo hành chính cơ học, không yêu cầu đánh giá năng lực/phẩm chất chi tiết.                                                            | Văn phong ghép nối cứng nhắc, rời rạc; học sinh cùng điểm số sẽ có lời nhận xét y hệt nhau; không hiểu được ghi chú riêng của GV.                  | Không |
| **Workflow**              | Quy trình phối hợp: Trích xuất bảng điểm (Rule) → Phân tích đặc trưng (Rule) → LLM sinh lời phê cá nhân hóa theo Thông tư 22 (AI) → GVCN duyệt/sửa (Human) → Xuất dữ liệu vnEdu (Rule). | Đủ và tối ưu cho bài toán: Quy trình nhiều bước rõ ràng, kết hợp thế mạnh xử lý logic của Rule và thế mạnh ngôn ngữ tự nhiên của AI, có GVCN chốt chặn cuối. | Nguy cơ AI dùng từ quá hoa mỹ nếu prompt lỏng lẻo; phụ thuộc vào độ chuẩn của file Excel đầu vào. Có thể kiểm soát tốt qua kiểm duyệt.             | Chọn  |
| **Agent**                 | Hệ thống tự động dùng tool đăng nhập vnEdu/SMAS, tự phân tích đa nguồn, tự quyết định nội dung và tự submit nhận xét không cần con người.                                               | Chỉ phù hợp khi hệ thống có toàn quyền tự chủ và không có ràng buộc pháp lý/trách nhiệm giáo dục.                                                            | Over-engineering (phức tạp không cần thiết); vi phạm nghiêm trọng quy chế sư phạm (GVCN phải chịu trách nhiệm); rủi ro rò rỉ tài khoản và dữ liệu. | Không |

**Mức chọn:** Workflow (Rule-based trích xuất + AI sinh gợi ý + Human-in-the-loop phê duyệt)

**Vì sao không chọn mức đơn giản hơn:** Vì No AI và Rule-based chỉ giải quyết được khâu ghép câu cơ học, sinh ra các nhận xét rập khuôn, thiếu ngữ cảnh và không thể hiện được sự tiến bộ hay tính cách riêng biệt của học sinh theo tinh thần Thông tư 22. AI (LLM) là mắt xích bắt buộc để tạo văn phong sư phạm tự nhiên, biến thiên linh hoạt và khích lệ người học, trong khi cấu trúc Workflow đảm bảo tính an toàn, kiểm soát được luồng dữ liệu và giữ vai trò quyết định tối cao của giáo viên.

### 6.3. AI Canvas rút gọn

| Thành phần                                                        | Nội dung                                                                                                                                                                                                                                                                                                                                                                  |
| ----------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Prediction** — AI dự đoán / tạo ra gì?                          | Bản nháp lời nhận xét học bạ cá nhân hóa (2–3 câu, 50–90 từ/học sinh) bám sát ma trận năng lực và phẩm chất theo Thông tư 22/2021/TT-BGDĐT, kết hợp giữa kết quả học tập và nề nếp rèn luyện.                                                                                                                                                                             |
| **Judgment** — con người cân nhắc, quyết định gì?                 | Giáo viên chủ nhiệm (GVCN) đánh giá và quyết định:<br>1. Lời nhận xét có phản ánh đúng thực tế tính cách, nỗ lực và tiến bộ của học sinh hay không?<br>2. Giọng điệu có đúng mực sư phạm, mang tính khích lệ, xây dựng hay không?<br>3. Quyết định: Phê duyệt (Approve), Chỉnh sửa nhanh (Edit), hoặc Yêu cầu tạo lại kèm ghi chú (Regenerate).                           |
| **Action** — hành động cuối cùng là gì, ai làm?                   | GVCN xuất danh sách lời phê đã duyệt ra định dạng chuẩn (1-click export) và đồng bộ/dán trực tiếp vào cổng học bạ điện tử vnEdu/SMAS để hoàn tất thủ tục khóa sổ đúng hạn.                                                                                                                                                                                                |
| **Outcome** — đo kết quả bằng gì?                                 | 1. Thời gian xử lý: Giảm từ 360–480 phút xuống ≤ 45 phút/lớp 45 học sinh (tiết kiệm ~90% thời gian).<br>2. Độ cá nhân hóa & sư phạm: 100% học sinh có lời phê riêng biệt; tỷ lệ trùng lặp văn bản < 5%.<br>3. Tỷ lệ chấp thuận: ≥ 80% lời phê được duyệt ngay hoặc chỉ cần chỉnh sửa nhẹ (< 3 từ).<br>4. An toàn: 0 sự cố lộ lọt dữ liệu định danh học sinh (PII).        |
| **Input** — AI cần dữ liệu đầu vào gì mỗi lần chạy? Có sẵn không? | 1. Dữ liệu bắt buộc: Điểm tổng kết các môn, xếp loại học lực, số buổi nghỉ học, xếp loại hạnh kiểm từ file xuất Excel của vnEdu/SMAS.<br>2. Dữ liệu bổ trợ: Ghi chú vắn tắt của GVCN (nếu có, ví dụ: "nhiệt tình văn nghệ", "tiến bộ môn Anh").<br>→ Tính sẵn có: Đã có sẵn 100% trên hệ thống quản lý học đường định kỳ.                                                 |
| **Feedback** — lấy phản hồi ở đâu để cải thiện?                   | 1. Lịch sử chỉnh sửa (diff log): So sánh văn bản AI sinh ra và phiên bản GVCN chỉnh sửa cuối cùng để tinh chỉnh prompt/rules.<br>2. Hành động của người dùng: Tần suất bấm "Tạo lại" (Regenerate) hoặc tỷ lệ chỉnh sửa >50% độ dài để phát hiện các mẫu câu chưa đạt.<br>3. Đánh giá cuối đợt: Nút chấm sao (1–5★) và phản hồi nhanh của GVCN sau khi khóa sổ thành công. |


### 6.4. Hai câu hỏi của Google PAIR

- Người dùng muốn **được hỗ trợ (augment)** hay **giao hẳn việc (automate)**? Bằng chứng:
	• Người dùng muốn được HỖ TRỢ (AUGMENT), tuyệt đối không giao hẳn việc (automate).
	• Bằng chứng thực tế:
	1. Trách nhiệm sư phạm: 100% (3/3) GVCN phỏng vấn khẳng định học bạ là hồ sơ pháp lý đi theo học sinh suốt đời và gắn với trách nhiệm của giáo viên, nên họ bắt buộc phải kiểm duyệt từng từ.
	2. Bản chất nút thắt: GVCN không lười đánh giá mà chỉ bị kiệt sức ở khâu tìm từ ngữ diễn đạt (drafting fatigue) cho 45 em trong 2–3 đêm. Họ cần AI tạo bản nháp gợi ý ban đầu để tiết kiệm thời gian suy nghĩ, sau đó tự tay tinh chỉnh.
	3. Khảo sát CP4: 81.8% giáo viên mong muốn có trợ lý sinh bản nháp thông minh, nhưng 100% phản đối việc để hệ thống tự động đẩy dữ liệu vào vnEdu/SMAS mà không qua kiểm duyệt.
- AI sai kiểu nào tệ hơn, **báo nhầm** hay **bỏ sót**? Vì sao, và thiết kế đã xử lý thế nào:
	-  Kiểu sai TỆ HƠN: BÁO NHẦM / ẢO GIÁC (False Positive / Hallucination — nhận xét sai lệch thành tích, gán nhầm khuyết điểm hoặc dùng từ ngữ thiếu chuẩn mực sư phạm).
	- Vì sao: Một lời nhận xét sai về hạnh kiểm hoặc bịa đặt kết quả học tập sẽ gây khiếu nại nghiêm trọng từ phụ huynh, ảnh hưởng tâm lý học sinh và khiến giáo viên bị kỷ luật chuyên môn. Trong khi đó, việc "bỏ sót" (chưa nêu hết ưu điểm) ít gây hại hơn nhiều và giáo viên có thể bổ sung nhanh trong 5–10 giây.
	- Cách thiết kế xử lý:
		1. Strict Grounding & Rule Constraint: Khống chế prompt nghiêm ngặt, chỉ cho phép AI sinh lời phê dựa trên dữ liệu điểm số/nề nếp thực tế đã trích xuất, tuyệt đối không bịa đặt sự kiện ngoại khóa hay thành tích không có trong dữ liệu.
		2. Bộ lọc quy chuẩn Thông tư 22: Chặn hoàn toàn các tính từ tiêu cực mang tính định kiến; bắt buộc dùng cấu trúc khích lệ, mang tính xây dựng.
		3. Cơ chế Human-in-the-loop bắt buộc: Giao diện hiển thị trực quan lời phê kèm nguồn dữ liệu tương ứng (highlight điểm mạnh/cần cố gắng) để GVCN rà soát trong 15–20 giây/em trước khi bấm duyệt.

---

## 7. Problem Statement v1 + tiêu chí đánh giá (CP6)

| Trường                                          | Nội dung                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| ----------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Actor**                                       | Giáo viên chủ nhiệm (GVCN) các trường Trung học Phổ thông (THPT), phụ trách lớp từ 40–45 học sinh.                                                                                                                                                                                                                                                                                                                                                                             |
| **Quy trình**                                   | Quy trình 5 bước hoàn chỉnh (tổng 45'):<br>[1. Tải bảng điểm: 5'] (Con người - Xuất file Excel từ vnEdu/SMAS, ẩn PII)<br>→ [2. Trích xuất đặc trưng: 5'] (Rule - Phân loại dải điểm & tổng hợp điểm thi đua)<br>→ [3. Sinh bản nháp nhận xét: 10'] (AI - Sinh lời phê chuẩn phẩm chất/năng lực Thông tư 22)<br>→ [4. Rà soát & Tinh chỉnh: 20'] (Human-in-the-loop - GVCN duyệt từng em)<br>→ [5. Xuất dữ liệu: 5'] (Rule - Xuất file chuẩn 1-click hoặc copy vào vnEdu/SMAS). |
| **Bottleneck**                                  | Khâu soạn thảo lời phê cá nhân hóa từng học sinh: Mất 360 phút / 45 em (~8 phút/em), gây quá tải và cạn kiệt từ ngữ diễn đạt vào 2–3 đêm sát giờ khóa sổ.                                                                                                                                                                                                                                                                                                                      |
| **Impact**                                      | • Giáo viên kiệt sức vì dồn việc ban đêm; căng thẳng tâm lý trước áp lực thời hạn khóa cổng phần mềm.<br>• Nhận xét học bạ bị rập khuôn sáo rỗng ("Chăm ngoan, cần cố gắng hơn"), làm mất tính định hướng sư phạm và giá trị của học bạ điện tử GDPT 2018.<br>• Nguy cơ trễ hạn khóa sổ bị nhà trường nhắc nhở, xếp loại thi đua cuối kỳ bị hạ.                                                                                                                                |
| **Success Metric** (baseline → target, cách đo) | • Baseline → Target: Tổng thời gian hoàn thành nhận xét 1 lớp giảm từ 480 phút xuống dưới 45 phút (tiết kiệm ~90%).<br>• Tiêu chí chất lượng: 100% học sinh có lời phê riêng biệt, độ chấp thuận của GVCN đạt ≥80%, tỷ lệ trùng lặp văn bản giữa các em < 5%.<br>• Cách đo: Bấm giờ thực tế trước/sau quy trình; đo tỷ lệ chỉnh sửa (diff log) và kiểm tra trùng lặp văn bản tự động.                                                                                          |
| **Boundary**                                    | • Không tải lên thông tin định danh cá nhân (PII: Họ tên, ngày sinh, CCCD, địa chỉ); chỉ xử lý qua mã định danh học sinh (Mã HS / STT).<br>• Không tự động sinh nhận xét cho các trường hợp đặc biệt (học sinh hòa nhập, có biến cố gia đình); hệ thống gắn cờ để GVCN tự tay viết.<br>• Không tự động can thiệp ghi đè dữ liệu lên cổng vnEdu/SMAS; luôn yêu cầu thao tác xác nhận chủ động từ giáo viên.                                                                     |
| **AI intervention point**                       | Can thiệp tại Bước 3: Đọc các đặc trưng học tập & nề nếp đã được trích xuất để sinh ra đoạn văn nhận xét gợi ý (draft) chuẩn ngôn phong sư phạm Thông tư 22 cho từng học sinh.                                                                                                                                                                                                                                                                                                 |
| **Mức chọn**                                    | Workflow (Rule-based tiền xử lý + AI/LLM sinh bản nháp + Human-in-the-loop phê duyệt + Rule-based xuất file)                                                                                                                                                                                                                                                                                                                                                                   |
| **Rủi ro & người kiểm tra**                     | • Rủi ro: AI ảo giác (hallucination) tạo thông tin sai lệch dữ liệu điểm; hoặc dùng từ ngữ quá hoa mỹ, thiếu tự nhiên.<br>• Người kiểm tra: GVCN trực tiếp rà soát 100% trên giao diện trước khi xuất file; Tổ trưởng chuyên môn / Ban giám hiệu phúc tra xác suất theo quy chế chuyên môn.                                                                                                                                                                                    |

**Thay đổi so với v0 và lý do:**

| Trường                                   | v0                                                                                               | v1                                                                                                                                        | Vì sao đổi                                                                                                                                        |
| ---------------------------------------- | ------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| Giải pháp & Mức can thiệp                | Chatbot AI hội thoại tự do (GV gõ prompt thủ công cho từng học sinh).                            | Workflow tự động hóa pipeline: Trích xuất bảng điểm → LLM sinh lời phê theo ma trận Thông tư 22 → GVCN duyệt từng em (Human-in-the-loop). | GVCN không có thời gian gõ prompt lặp lại 45 lần; chatbot tự do dễ sinh lan man, sai thể thức sư phạm và thiếu tính hệ thống.                     |
| Ranh giới bảo mật dữ liệu (Boundary)     | Chưa có ranh giới bảo mật (tải trực tiếp file bảng điểm chứa họ tên, ngày sinh lên tool online). | Thiết lập ranh giới nghiêm ngặt: Ẩn danh hóa 100% PII (chỉ xử lý qua Mã HS / STT); tuyệt đối không tải dữ liệu định danh cá nhân lên AI.  | Tuân thủ quy định bảo vệ dữ liệu ngành giáo dục; giải tỏa lo ngại của giáo viên về rủi ro lộ lọt thông tin học sinh ra bên ngoài.                 |
| Đầu ra & Tích hợp (Output & Integration) | Chỉ hiển thị đoạn văn thô trên màn hình, giáo viên phải copy-paste thủ công từng em.             | Cung cấp định dạng xuất file Excel chuẩn và nút Copy 1-click tương thích hoàn toàn với giao diện nhập liệu của vnEdu/SMAS.                | Giáo viên phản ánh các template trôi nổi hay bị lỗi font tiếng Việt và vỡ định dạng khi dán vào vnEdu, gây ức chế và tốn thời gian căn chỉnh lại. |


**Tiêu chí đánh giá đầu ra của AI (3–5 tiêu chí):**

|   # | Tiêu chí                                                                      | Đạt khi                                                                                                                                                                                  | Không đạt khi                                                                                                                             |
| --: | ----------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
|   1 | Độ chính xác dữ liệu & Không ảo giác (Data Grounding & Zero Hallucination)    | 100% dữ liệu về học lực, các môn thế mạnh, điểm tiến bộ và nề nếp khớp hoàn toàn với bảng điểm gốc; tuyệt đối không bịa đặt thành tích hay lỗi vi phạm không có trong hồ sơ.             | Nhầm lẫn điểm số, gán sai hạnh kiểm/vi phạm hoặc tự suy diễn các thành tích ngoại khóa không có trong dữ liệu.                            |
|   2 | Chuẩn mực ngôn phong sư phạm Thông tư 22 (Pedagogical Tone & Compliance)      | Tuân thủ nghiêm ngặt ma trận phẩm chất - năng lực theo TT 22/2021/TT-BGDĐT; ngôn từ mang tính khích lệ, tích cực, xây dựng; độ dài tối ưu 50–90 từ (2–3 câu), không vượt giới hạn ký tự. | Dùng từ ngữ tiêu cực, phán xét, gây tổn thương tâm lý học sinh; câu văn cộc lốc hoặc quá sáo rỗng, vi phạm giới hạn ký tự của vnEdu/SMAS. |
|   3 | Tính cá nhân hóa & Độ đa dạng ngôn ngữ (Personalization & Linguistic Variety) | Mỗi học sinh có nhận xét riêng biệt thể hiện sự chuyển biến và ghi chú riêng của GV; tỷ lệ trùng lặp nguyên văn (overlap) giữa các nhận xét trong cùng lớp < 5%.                         | Các học sinh cùng khung điểm có lời nhận xét rập khuôn y hệt nhau; không thể hiện được tính cách hay sự tiến bộ riêng.                    |

---

## 8. Quyết định (CP6)

### 8.1. Bốn rủi ro

| Rủi ro          | Câu hỏi                                                           | Mức độ rủi ro (Thấp = an toàn / TB / Cao = nguy hiểm) | Lý do / bằng chứng                                                                                                                                                                                                                                                                                                                                    |
| --------------- | ----------------------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Value**       | Người dùng có thật sự cần và sẽ dùng không?                       | Thấp                                                  | • Nhu cầu cực kỳ cấp bách và có thật: Khảo sát CP4 chỉ ra 86.4% GVCN mất trên 5 giờ/đợt; 81.8% sẵn sàng áp dụng ngay nếu tiết kiệm được >70% thời gian.<br>• Áp lực deadline khóa sổ vnEdu định kỳ gây kiệt sức cao; GV có động lực rất lớn để giải phóng khỏi áp lực viết lặp lại.                                                                   |
| **Usability**   | Người dùng có dùng được, có hiểu và sửa được đầu ra của AI không? | Thấp                                                  | • Luồng thao tác tối giản: Tải file Excel → Xem bản nháp trên bảng duyệt trực quan → Sửa nhanh hoặc bấm duyệt → Xuất file 1-click.<br>• GVCN không cần học viết prompt phức tạp; chỉ đóng vai trò người biên tập và kiểm duyệt nội dung theo đúng chuyên môn quen thuộc.                                                                              |
| **Feasibility** | Có đủ dữ liệu, công cụ, kỹ năng để làm không?                     | Thấp                                                  | • Bảng điểm vnEdu/SMAS có cấu trúc chuẩn hóa cao trên toàn quốc, dễ trích xuất bằng Python/JavaScript.<br>• Năng lực LLM hiện tại hoàn toàn vượt trội trong việc tổng hợp dữ liệu bảng và sinh văn phong sư phạm tiếng Việt khi được cung cấp bộ prompt chuẩn Thông tư 22; hoàn toàn khả thi để hoàn thiện trong lab.                                 |
| **Viability**   | Có hợp chi phí, pháp lý, quy định tổ chức không? Ai vận hành?     | Thấp                                                  | • Tuân thủ pháp lý & quy định bảo mật: Đã loại bỏ hoàn toàn PII (họ tên, ngày sinh); hệ thống chỉ xử lý theo Mã HS / STT ẩn danh.<br>• Hợp lệ quy chế sư phạm: Cơ chế Human-in-the-loop đảm bảo GVCN chịu trách nhiệm thẩm định cuối cùng trước khi vào sổ.<br>• Chi phí cực thấp (< 1.000 VNĐ / lớp 45 học sinh), hoàn toàn khả thi về mặt vận hành. |

### 8.2. Kết luận

**Quyết định:** Go

**Lý do:** Cả 4 trụ cột rủi ro (Value, Usability, Feasibility, Viability) đều ở mức Thấp (An toàn). Nhu cầu người dùng cực kỳ cấp bách và đã được kiểm chứng bằng số liệu thực tế (86.4% GVCN mất >5h/đợt; 81.8% sẵn sàng áp dụng). Giải pháp Workflow có cấu trúc rõ ràng, tính khả thi cao, vừa vặn để triển khai và demo thành công trong phạm vi lab.

**Nếu Go — pilot nhỏ nhất:** Xây dựng bản MVP thử nghiệm trên 1 file Excel chứa dữ liệu của 1 lớp học thực tế (45 HS đã ẩn danh PII); hệ thống sinh nhận xét cho 10 học sinh tiêu biểu đại diện các dải năng lực (Xuất sắc, Khá, Trung bình, Có khuyết điểm nề nếp) để GVCN chấm điểm độ tự nhiên và thời gian duyệt thực tế.

**Nếu Not Yet — cần kiểm chứng gì trước:** (Không áp dụng do quyết định Go. Dự phòng: Nếu cần kiểm chứng thêm, sẽ thử nghiệm tính tương thích của các định dạng file xuất Excel khác nhau giữa vnEdu và SMAS).

**Nếu No-Go — nên làm gì thay AI:**  (Không áp dụng do quyết định Go. Phương án dự phòng No-AI: Cung cấp file Google Sheets tích hợp sẵn 20 mẫu câu thả xuống (Data Validation) phân loại theo học lực kết hợp hàm INDEX/MATCH).

**Ngưỡng dừng** (nếu sau … mà … thì quay về …): Nếu sau khi thử nghiệm pilot trên 45 học sinh mà tỷ lệ chấp thuận của GVCN < 65% (phải sửa lại quá nhiều) HOẶC xảy ra tình trạng AI hallucination bịa đặt số liệu điểm số vượt quá 0%, thì lập tức dừng pipeline AI và quay về hoàn thiện công cụ Rule-based bán tự động trên Google Sheets.

---

## 9. Hạn chế và hướng tiếp theo

- Hạn chế về phạm vi dữ liệu: Mô hình AI chỉ suy luận dựa trên các chỉ số định lượng (điểm các môn, điểm trừ nề nếp, số buổi vắng) và ghi chú ngắn; chưa thể tự thấu hiểu các yếu tố tâm lý, hoàn cảnh gia đình đặc biệt hay sự tiến bộ âm thầm của học sinh nếu GVCN không trực tiếp bổ sung ghi chú.
- Thách thức định dạng & bảo mật: File xuất từ các hệ thống quản lý học đường (vnEdu, SMAS) có thể khác nhau về cấu trúc cột, tiêu đề và bảng mã font tiếng Việt giữa các địa phương; đồng thời phải duy trì kỷ luật ẩn danh hóa PII nghiêm ngặt trên máy trạm của giáo viên để ngăn ngừa rò rỉ dữ liệu.
- Hướng phát triển tiếp theo: (1) Phát triển Chrome Extension hỗ trợ tự động điền trực tiếp vào bảng web vnEdu/SMAS mà không cần thao tác tải file Excel qua lại; (2) Tích hợp bộ gợi ý biện pháp giáo dục/kế hoạch kèm cặp cá nhân hóa cho học sinh yếu kém; (3) Mở rộng thư viện quy chuẩn sang cấp THCS (Thông tư 22) và Tiểu học (Thông tư 27).

## 10. Tài liệu tham khảo

-
