# Track1_Day18_2A202602560_TaVietCuong — README

## 1. Thông tin cá nhân và nhóm
- **MHV:** 2A202602560
- **Họ tên:** Tạ Việt Cường
- **Tên nhóm:** FinTech
- **Thành viên (3 người):** Tạ Việt Cường — Nguyễn Văn Thăng — Nguyễn Anh Dũng
- **Case:** Case A — AI Tutor: Diagnostic Refresher
- **Vai trò Day 17:** Người phỏng vấn
- **Trách nhiệm Day 18:** Option B (Tự chọn từ sơ đồ nền) + Màn 0 common context + Human–AI Decision Table + facilitate Tester 1 (cả A/B/C)

## 2. Hypothesis Problem (nhóm dùng trong Day 18, nối từ Day 17)
> Khi đang học bài mới trên VLearn mà bị mắc kẹt ở đoạn không hiểu (ví dụ: làm sai quiz cuối bài), người học gặp khó khăn trong việc hiểu tiếp bài để làm được bài tập vì không xác định được mình đang thiếu khái niệm nền nào nên ôn lan man / sai chỗ, dẫn đến tốn 30–60 phút mà vẫn không hiểu, làm sai tiếp và dễ bỏ dở bài.

- Evidence hỗ trợ: Practice Note 1 (01/10, bài RAG): sai 2 lần câu chunking + top-k, xem slide 8-10, Google "RAG chunk overlap bao nhiêu là đủ", xem YouTube 18' về embedding, hỏi bạn cùng phòng, mất ~60 phút vẫn sai, tắt máy bỏ bài.
- Chưa chứng minh: (1) Pain A vs Pain B (hổng nền vs đứt mạch), (2) tần suất ≥2 lần/tháng và hậu quả >15', (3) user có tự ôn + quay lại nếu được chỉ đúng chỗ không.
- Chi tiết: xem `three-option-design-sheet.md` Chặng 1.

## 3. Three Solution Options (cùng task/outcome/fixture, khác mechanism)
- **Task chung:** Hiểu tiếp để làm đúng quiz RAG và quay lại bài cũ trong <10 phút.
- **Fixture chung:** Slide 8-10 tóm tắt, 2 câu quiz sai (Chunk overlap 0 từ & Top-k=1), lịch sử xem video embedding 18 phút.
- **Option A — AI gợi ý dẫn dắt (Dũng build):** Màn 1: Trạng thái trước kích hoạt (banner mời gọi khi học viên bị kẹt) → Màn 2 (Tích hợp): Phần trên là AI Chẩn đoán gợi ý Chunk Overlap, Phần dưới là Thao tác lựa chọn của người học (Chấp nhận / Đổi sang câu Top-k / Từ chối).
- **Option B — Đối thoại 2 chiều & Quyền User (Cường build):** Luồng chat 2 chiều Người ↔ AI. Người học nắm quyền cao nhất, sở hữu bộ **Nút chỉnh sửa / Kiểm soát** (Đổi sang ví dụ đời thực, Bảng so sánh 0 từ vs 50 từ, Tóm tắt siêu ngắn, Đổi chủ đề) và ô tự sửa ghi chú.
- **Option C — Tự động ngầm & Duyệt ngoại lệ (Thăng build):** AI chạy ngầm Event Logs ngay khi sai quiz và chuẩn bị sẵn gói giải pháp 60s. Người dùng kiểm soát tại 2 chốt: **Điểm Duyệt kết quả (Approve & Apply)** và **Điểm Can thiệp qua ngoại lệ (Exception-based Override)** khi AI đoán sai.
- Distance check và Human–AI Decision Table: xem `three-option-design-sheet.md` Chặng 2-3.
- Link prototype & Bản trình chiếu Infographic: xem [`prototype-link.md`](file:///d:/VinUni/LabTrack1-03/Track1_Day18_2A202602560_TaVietCuong/prototype-link.md) hoặc mở trực tiếp bản infographic sống động tại [`present.html`](file:///d:/VinUni/LabTrack1-03/Track1_Day18_2A202602560_TaVietCuong/present.html).

## 4. Đóng góp của tôi trong nhóm
- Chốt Evidence Snapshot Chặng 1 từ Note Day 17 của mình + Hypothesis Problem mang sang.
- Thiết kế và build **Option B** (Luồng đối thoại 2 chiều + Bảng công cụ chỉnh sửa quyền hạn User) + **Màn 0 Trang chủ chung** chia sẻ 70% bối cảnh (HTML trong `prototype/`).
- Viết Human–AI Decision Table hàng Option B (Expectation, User Agency cao nhất, Nút can thiệp chỉnh sửa, control Đóng/Khôi phục/Trang chủ).
- Test chéo Option A/C do bạn build để chuẩn hoá trước khi test thật (GATE 4).
- Facilitate Tester 1 với cả A/B/C + ghi `prototype-feedback-note.md`.
- Tổng hợp cùng nhóm `group-feedback-synthesis.md` (1 Next Change + Still Unproven).

## 5. Prototype Feedback (phiên tôi facilitate — điền sau test, không bịa)
- **Tóm tắt phiên Tester 1 (Cường facilitate):**
  * **Tester:** Lưu Xuân Dũng (MSHV: 02746, ngoài nhóm FinTech).
  * **Context thực tế:** Từng bị mắc kẹt khi học mô hình Transformer, làm bài quiz sai 3 lần nhưng không biết mình hổng ở công thức hay ở logic truy vấn, nản lòng và tắt máy bỏ bài.
  * **Hành vi & Trích dẫn cốt lõi:**
    1. *"Luồng hơi ép buộc người dùng vào một khuôn, chưa cho người dùng control được."* (Phản hồi về Option A/C).
    2. *"Khi người dùng chưa hiểu bài thì vẫn chưa biết cần hỏi AI về vấn đề gì."* (Ngập ngừng 15s trước khung chat mở của Option B).
    3. *"Có giải thích tổng quát nhưng chưa cho phép người dùng hỏi lại khi chưa hiểu."* (Thiếu tính năng hỏi đào sâu vào câu chữ cụ thể).
  * **Lựa chọn & Trade-off:** Chọn **Option B** (vì muốn tự làm chủ cách học, chấp nhận tốn công suy nghĩ và gõ chữ hơn việc để AI dọn sẵn ở Option C).
  * *Chi tiết 4 lớp OBSERVED / INTERPRETED / DECIDED / STILL UNPROVEN:* xem file [`prototype-feedback-note.md`](file:///d:/VinUni/LabTrack1-03/Track1_Day18_2A202602560_TaVietCuong/prototype-feedback-note.md).

- **Ba-feedback synthesis (Hội tụ bằng chứng & Pattern giữa 3 Tester):**
  * **Sự hội tụ bằng chứng tam giác (Triangulation giữa Cường, Thăng, Dũng):** Cả ba tester độc lập ngoài nhóm đều xác nhận cùng 3 điểm nghẽn tương tác:
    1. *Ở Option B (Tê liệt khi bí kiến thức):* Không biết đặt câu hỏi gì (Tester 1) / *"đặt câu hỏi không tối ưu"* (Tester 2) / *"lúc đang bí kiến thức có thể không biết nên chọn cách hỏi nào trước"* (Tester 3, chấm Control 5/5, Help 5/5).
    2. *Ở Option A (Thiếu linh hoạt đào sâu):* Rất khen ví dụ lợp ngói nhưng *"chưa cho phép hỏi lại khi chưa hiểu"* (Tester 1) / *"chưa cho tự do gõ câu hỏi"* (Tester 2) / *"luồng gợi ý ban đầu khá định hướng; muốn hỏi một chi tiết riêng thì chưa tiện"* (Tester 3, chấm Control 4/5, Help 5/5).
    3. *Ở Option C (Mất quyền kiểm soát & sợ sót):* Luồng ép buộc (Tester 1) / *"trải nghiệm hơi bị động, lo ngại sót thông tin do AI định hướng sẵn"* (Tester 2, Control 2/5) / *"AI tự kết luận 80% lỗi ở overlap khiến tôi lo... phải vào báo ngoại lệ để sửa"* (Tester 3, Control 3/5).
  * **Khác biệt & Lựa chọn:** 2/3 tester chọn Option B (Tester 1 & 3) vì chuộng quyền làm chủ và muốn thay đổi cách học ngay trong lúc trao đổi; 1 tester phân vân giữa A và B (Tester 2). Không ai chọn Option C làm giải pháp học tập lâu dài.
  * *Chi tiết bảng đối chiếu 3 feedback:* xem file [`group-feedback-synthesis.md`](file:///d:/VinUni/LabTrack1-03/Track1_Day18_2A202602560_TaVietCuong/group-feedback-synthesis.md).

- **Một Next Change nhóm chốt (Hybrid Scaffolded Drill-down):**
  * **Giữ cơ chế chẩn đoán chủ động của Option A** để bóc tách sẵn 2–3 "nghi vấn cốt lõi" cụ thể dựa trên lỗi sai của quiz (giải quyết triệt để vấn đề *"không biết hỏi gì khi chưa hiểu"*).
  * **Tích hợp cơ chế đối thoại đào sâu theo ngữ cảnh của Option B:** Trong bài giải thích tổng quát của AI, cho phép người học **click trực tiếp vào từng câu hoặc từ khóa chưa hiểu (ví dụ: click vào 'ngữ cảnh', 'top-k') để mở luồng hỏi đáp đào sâu 2 chiều tại chỗ**, thay vì ép buộc người dùng vào các nút bấm cứng nhắc (giải quyết triệt để vấn đề *"bị ép vào khuôn & không cho hỏi lại"*).

- **Still Unproven sau 3 feedback:**
  * Chưa chứng minh được liệu việc cho phép hỏi đáp đào sâu tại chỗ có làm người học bị phân tâm, hỏi lan man vượt quá ngưỡng thời gian cam kết <10 phút của bài học hay không.
  * Chưa kiểm chứng được hành vi thực tế khi đối mặt với áp lực deadline/thi cử liệu người học có quay lại lạm dụng tính năng tự động làm hộ của Option C hay không.
  * Chưa đánh giá được phản ứng của nhóm người học mới bắt đầu (novice) — liệu họ có thấy "bị ép vào khuôn" như Tester 1 hay họ lại cần một luồng cố định để được chỉ dẫn từng bước.

## 6. AI Support Log
Xem `ai-support-log.md` — AI chỉ gợi ý cơ chế, rà câu dẫn, tạo fixture canned. Không dùng AI bịa quote/observation/feedback. Reflection và Feedback Note do tôi tự viết.
