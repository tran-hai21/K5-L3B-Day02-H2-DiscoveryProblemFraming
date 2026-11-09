# Báo cáo cá nhân — 2A202603772_NguyenDucHieu

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Nguyễn Đức Hiếu       
- MSSV: 2A202603772
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: H2
- Link repo nhóm: https://github.com/tran-hai21/K5-L3B-Day02-H2-DiscoveryProblemFraming.git

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Tốn thời gian | Khi dạy lớp có nhiều trình độ, tôi muốn soạn bài tập theo nhóm năng lực, để học sinh luyện tập đúng mức. | Giáo viên THCS | TALIS 2024: giáo viên THCS Việt Nam soạn bài **11,2 giờ/tuần**; **40,6%** có nhu cầu cao về phương pháp học tập cá nhân hóa. [S1] |
| 2 | Cần đọc, tổng hợp nhiều thông tin | Khi tiếp nhận người cao tuổi dùng nhiều thuốc, tôi muốn đối chiếu lịch sử thuốc với hồ sơ nhập viện, để phát hiện thông tin thiếu hoặc mâu thuẫn. | Dược sĩ lâm sàng, bác sĩ | Nghiên cứu tại Việt Nam: **32,3%/192 bệnh nhân** có sai khác thuốc ngoài chủ ý khi nhập viện. [S2] |
| 3 | Pain từ người khác | Khi di chuyển lúc mưa lớn, tôi muốn biết đường có nguy cơ ngập, để tránh nguy hiểm và quay đầu. | Người đi làm, sinh viên, tài xế | Kịch bản Hà Nội 2026: mưa **70–100 mm/giờ → 84 điểm ngập**; trên **100 mm/giờ → 220 điểm**. Không phải số điểm ngập thực tế. [S3] |
| 4 | Lặp lại | Khi xử lý rác hằng ngày, tôi muốn biết đúng nhóm rác và nơi bàn giao, để tránh phân loại lại hoặc bỏ sai. | Cư dân đô thị, nhân viên thu gom | Năm 2025: khoảng **69.400 tấn rác/ngày**, đô thị **37.250 tấn/ngày**; chưa phản ánh tỷ lệ phân loại sai. [S4] |
| 5 | Cần đọc, tổng hợp nhiều thông tin | Khi mua căn hộ, tôi muốn so sánh giá, diện tích và chi phí các căn tương đương, để chọn phù hợp ngân sách. | Người mua nhà lần đầu | Hà Nội 2025: giá căn hộ sơ cấp trung bình **100 triệu đồng/m²**, tăng **40%** so với 2024; là bối cảnh thị trường. [S5] |

**Nếu có dùng AI để gợi ý thêm:** Chưa xác nhận ý nào tự scan, ý nào do AI gợi ý; cần bổ sung lịch sử thực tế.

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Phân loại rác (#4) | Quy trình đơn giản, dễ quan sát và thử No AI. | Khó do kiến thức hay hệ thống thu gom? |
| 2 | Tìm đường tránh ngập (#3) | Tác động rõ, dễ tiếp cận người dùng. | Có dữ liệu ngập đủ cập nhật không? |
| 3 | So sánh căn hộ (#5) | Quy trình rõ, có thể khảo sát tin đăng. | Tin đăng có chính xác, đủ thông tin không? |

### Problem Card #1

| Trường | Nội dung |
|---|---|
| Job Story | Khi xử lý rác hằng ngày, tôi muốn biết nhóm rác và nơi bỏ, để tránh phân loại sai hoặc làm lại. |
| Actor | Cư dân khu đô thị/chung cư có quy định phân loại rác. |
| Thời điểm / bối cảnh | Trước khi mang rác đến điểm tập kết. |
| Quy trình hiện tại (3–7 bước) | Thu gom → Tra hướng dẫn → Xác định nhóm, tách rác → Đóng gói → Bàn giao; xem thời gian ở sơ đồ dưới. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3: xác định và tách nhóm rác, **4 phút/lượt**. |
| Impact (nếu không giải thì sao) | Tốn thời gian, phân loại sai và phải xử lý lại. |
| Success metric (baseline → target) | Phân loại: **4 → dưới 2 phút/lượt**, đúng **ít nhất 9/10 vật mẫu**. Dự kiến bấm giờ trước/sau và chấm theo hướng dẫn địa phương. |
| Phương án không dùng AI | Nhãn thùng, bảng ví dụ và hướng dẫn hình ảnh; thử trước AI. |
| Giả thuyết về AI (nếu có) | Nhận dạng vật qua ảnh, gợi ý nhóm rác theo quy định địa phương. |
| Cảm nhận nhanh | Rule hoặc Workflow; chưa chốt. |

**Boundary:** Không gợi ý trái quy định; rác nguy hại cần hướng dẫn chính thức.

**Giả định:** Có nơi tiếp nhận rác đã phân loại; nếu thiếu, cần giải quyết khâu thu gom trước.

Quy trình nháp hiện tại:

```text
GIẢ ĐỊNH — 13 phút/lượt
[1 Thu gom: 2'] → [2 Tra hướng dẫn: 3']
→ [3 Xác định nhóm, tách rác: 4'] ← BOTTLENECK
→ [4 Đóng gói: 2'] → [5 Bàn giao: 2']
```

### Problem Card #2

| Trường | Nội dung |
|---|---|
| Job Story | Khi đi lại lúc mưa lớn, tôi muốn biết đường ngập hoặc có nguy cơ ngập, để chọn hành trình an toàn hơn. |
| Actor | Người đi làm, sinh viên, tài xế ở đô thị thường ngập. |
| Thời điểm / bối cảnh | Trước khi đi hoặc khi gặp đường ngập. |
| Quy trình hiện tại (3–7 bước) | Kiểm tra thời tiết → Xem bản đồ → Tìm thông tin ngập → So sánh tuyến → Quyết định; xem thời gian ở sơ đồ dưới. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3: tìm thông tin ngập phân tán, **7 phút/lượt**. |
| Impact (nếu không giải thì sao) | Mất thời gian tra cứu, có thể quay đầu hoặc đi vào vùng nguy hiểm. |
| Success metric (baseline → target) | Chuẩn bị và quyết định: **17 → dưới 8 phút/lượt**. Dự kiến bấm giờ cùng tình huống trước/sau; không đề xuất tuyến có cảnh báo ngập chính thức còn hiệu lực. |
| Phương án không dùng AI | Bản đồ điểm ngập và cảnh báo theo quy tắc. |
| Giả thuyết về AI (nếu có) | Tóm tắt cảnh báo từ nguồn được phép, nêu tuyến cần kiểm tra thêm. |
| Cảm nhận nhanh | Rule hoặc Workflow; phụ thuộc dữ liệu cập nhật. |

**Boundary:** Không khẳng định đường an toàn khi thiếu dữ liệu; không hướng dẫn vượt vùng ngập sâu.

Quy trình nháp hiện tại:

```text
GIẢ ĐỊNH — 17 phút/lượt
[1 Kiểm tra thời tiết: 2'] → [2 Xem bản đồ: 4']
→ [3 Tìm thông tin ngập: 7'] ← BOTTLENECK
→ [4 So sánh tuyến: 3'] → [5 Quyết định: 1']
```

### Problem Card #3

| Trường | Nội dung |
|---|---|
| Job Story | Khi mua căn hộ, tôi muốn đối chiếu giá, diện tích và chi phí các căn tương đương, để lọc nhanh lựa chọn phù hợp. |
| Actor | Người mua căn hộ lần đầu. |
| Thời điểm / bối cảnh | Tìm hiểu và lập danh sách căn phù hợp. |
| Quy trình hiện tại (3–7 bước) | Tìm tin → Lọc căn → Chuẩn hóa thông tin → Xác minh → Lập bảng; xem thời gian ở sơ đồ dưới. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3: chuẩn hóa giá/m² và đặc điểm, **20 phút/5 tin**. Bước lọc cũng 20 phút; cần đo để chốt bước nghẽn. |
| Impact (nếu không giải thì sao) | Tốn thời gian, dễ bỏ tiêu chí hoặc tính sai chi phí. |
| Success metric (baseline → target) | **75 → dưới 45 phút/5 tin**. Dự kiến bấm giờ cùng bộ tin trước/sau; bảng đủ giá/m², diện tích, vị trí, chi phí và nhãn chưa xác minh. |
| Phương án không dùng AI | Google Sheets có công thức giá/m² và tiêu chí cố định. |
| Giả thuyết về AI (nếu có) | Trích xuất thông tin tin đăng thành bảng; người dùng đối chiếu nguồn. |
| Cảm nhận nhanh | Rule hoặc Workflow; thử bảng tính trước. |

**Boundary:** Không xác nhận pháp lý, cam kết đầu tư hoặc tự quyết định mua.

Quy trình nháp hiện tại:

```text
GIẢ ĐỊNH — 75 phút/5 tin đăng
[1 Tìm tin: 10'] → [2 Lọc căn: 20']
→ [3 Chuẩn hóa thông tin: 20'] ← BOTTLENECK
→ [4 Xác minh: 15'] → [5 Lập bảng: 10']
```

### Card muốn pitch nhất

- Card số: **#1 — Phân loại rác sinh hoạt**.
- Vì sao: Phạm vi cụ thể, dễ quan sát cư dân và kiểm tra bằng 10 vật mẫu.
- Câu hỏi muốn nhóm phản biện: Nếu thiếu thùng phân loại hoặc thu gom vẫn trộn rác, hỗ trợ nhận biết nhóm rác có giải đúng bottleneck không?

**Trạng thái:** Ưu tiên pitch ở CP3; chưa quyết định Go về AI.

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Lượng rác toàn quốc chưa chứng minh lỗi phân loại. | Ghi nhận theo bản nháp. | Tách số liệu bối cảnh; đề xuất quan sát 5–10 cư dân. |
| Chưa rõ lỗi do kiến thức hay hạ tầng. | Cần kiểm chứng. | Thêm giả định có quy trình thu gom phân loại. |
| Bảng hướng dẫn có thể đủ. | Ưu tiên No AI theo bản nháp. | Thêm nhãn thùng và hướng dẫn hình ảnh. |
| Chưa đo thời gian; card #3 có hai bước cùng 20 phút. | Cần xác nhận thực tế. | Gắn nhãn giả định, thêm cách đo và lưu ý bước nghẽn. |


---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Trình bày 3 bài toán: phân loại rác, tránh ngập và so sánh căn hộ. | Phân loại rác vào shortlist, đạt 24/35 điểm. |
| Phản biện bài của bạn khác | Hỏi Thanh về độ chính xác khi tìm vị trí sửa code; Hải về giáo án phù hợp thực tế lớp học; Quân về việc xếp deadline và khả năng làm theo lịch. | Giúp thảo luận tập trung vào tính đúng, tính khả thi và hành vi sử dụng. |
| Nhận phản biện | Tiếp nhận câu hỏi về hạ tầng thu gom, dữ liệu ngập và độ tin cậy tin căn hộ. | Bổ sung điều kiện áp dụng và yêu cầu kiểm tra dữ liệu cho các phương án. |
| Gom cluster / cây OST | Xếp 3 candidate của mình vào cluster hỗ trợ ra quyết định; viết lại pain phân loại rác để tách khỏi ý tưởng app. | Phân biệt nhu cầu người dùng với giải pháp đề xuất. |
| Chọn candidate problem | Đánh giá sự phụ thuộc hạ tầng của bài phân loại rác và ghi lý do không chọn. | Làm rõ hạn chế của candidate đạt 24/35 điểm. |
| Kiểm chứng / research | | |
| Quy trình nhóm | Phụ trách trình bày sơ đồ trước/sau, ghi thời gian từng bước và đánh dấu bottleneck. | Có bản quy trình 480 → 45 phút/lớp, tách rõ Rule, AI và giáo viên. |
| Problem Statement | Phụ trách phần Success Metric: thời gian hoàn thành, tỷ lệ duyệt và cách đo. | Metric có baseline, target và cách kiểm tra chất lượng. |
| Mức can thiệp AI | Viết phần phân biệt Workflow với Agent dựa trên quy trình đã vẽ. | Làm rõ AI chỉ viết nháp trong các bước cố định, không cần tự quyết hành động. |
| Quyết định | | |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP5–6 Problem Statement | Tóm tắt v0 → v1, kiểm tra metric và boundary. | Làm rõ actor, chất lượng và quyền quyết định của giáo viên. | AI không biết đầy đủ ngữ cảnh từng học sinh. | Giữ yêu cầu bám dữ liệu và giáo viên kiểm tra từng em. |
| CP6 Mức can thiệp / quyết định | Hỗ trợ tổng hợp lập luận Workflow và Go. | Liên kết mức can thiệp với pilot, rủi ro và ngưỡng dừng. | Kết luận trong bảng chưa được kiểm chứng bằng pilot. | Giới hạn Go ở thử nghiệm nhỏ, giữ phương án quay về Rule. |

---

## 6. Reflection (CP7)

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

Tôi học được rằng vấn đề quen thuộc chưa chắc là vấn đề phù hợp nhất để chọn. Các card của Thanh, Quân và Hải giúp tôi chú ý hơn đến actor, bước nghẽn và khả năng đo, thay vì chỉ nhìn vào ý tưởng có vẻ hữu ích.

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

Nhóm từng mô tả cơ hội bằng các tên như chatbot nhận xét, app quét rác và pipeline RAG. Khi rà cây OST, chúng tôi chuyển về nhu cầu thật: giảm thời gian, tránh sai và hoàn thành đúng hạn, rồi mới bàn cách giải quyết.

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**

Ban đầu tôi ưu tiên phân loại rác vì dễ tiếp cận người dùng. Câu hỏi của Quân về hạ tầng thu gom khiến tôi nhìn lại: nhận biết đúng chưa đủ nếu rác vẫn bị trộn. Tôi đồng ý chọn học bạ vì phạm vi quy trình rõ hơn.

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

Điều khiến tôi chú ý là giáo viên cần giảm công viết nhưng vẫn muốn tự duyệt từng nhận xét. Kết quả nhóm tổng hợp cho thấy tốc độ phải đi cùng độ đúng và bảo mật. Tôi hiểu giá trị của bản nháp có thể sửa hơn là giao toàn bộ việc cho AI.

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

Khó nhất với tôi là viết đủ cụ thể mà không đưa giải pháp vào problem. Metric cũng cần đo chất lượng, không chỉ thời gian. Với mục tiêu 480 xuống 45 phút/lớp, vẫn phải kiểm tra nhận xét đúng dữ liệu và tính cả thời gian giáo viên sửa.

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

Tôi sẽ đo baseline sớm, thử phương án đơn giản và hỏi về hành vi đã xảy ra. Tôi cũng sẽ diễn đạt câu hỏi deadline trung lập hơn, tránh quy kết người dùng lười. Với học bạ, tôi muốn kiểm tra kỹ thời gian duyệt và ngưỡng dừng pilot.

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.

Bài toán nhóm chọn là GVCN mất nhiều thời gian viết nhận xét riêng cho 40–45 học sinh. Quy trình gồm xuất dữ liệu, phân loại, viết, rà soát và nhập sổ; bước viết chiếm 360/480 phút. Mục tiêu là 45 phút/lớp, đo thời gian trước/sau và tỷ lệ giáo viên duyệt. Boundary là loại thông tin định danh khỏi đầu vào, không bịa dữ liệu và không tự ghi đè hệ thống. Nhóm chọn Workflow vì các bước cố định, AI chỉ viết nháp và giáo viên duyệt từng em. Quyết định Go dành cho pilot nhỏ; nếu tỷ lệ duyệt dưới 65% hoặc có bịa dữ liệu điểm thì dừng và quay về Rule.

---

## 7. Tài liệu tham khảo
