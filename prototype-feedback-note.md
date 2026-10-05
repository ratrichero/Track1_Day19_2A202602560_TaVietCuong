# Prototype Feedback Note — Người facilitate: Tạ Việt Cường (2A202602560)
> Tester 1 (ngoài nhóm). Test cả A/B/C, ~4 phút/option. Ghi hành vi trước, diễn giải sau. Không hỏi "Bạn có thích không?". Không bịa quote.

## Tester / context
- **Tên/gợi nhớ:** Lưu Xuân Dũng (MSHV: 02746, ngoài nhóm FinTech).
- **Relevant context (trả lời câu ≤2 phút "7 ngày qua có lúc nào học mà dừng vì không hiểu?"):** 
  *"Có, 3 hôm trước mình học phần Attention Mechanism trong Transformer, làm bài quiz trên mạng sai 3 lần liên tiếp. Càng đọc tài liệu càng rối vì không biết mình đang bị hổng ở công thức ma trận hay ở logic truy vấn, sau đó nản quá phải tắt máy đi ngủ."*
- **Ngày/giờ test:** 05/10/2026, 11:45 — 12:05 • **Thời lượng:** 20 phút.

---

## Observation (điền trong lúc test)

| Observation | Note (nguyên văn hành vi + lời tester) |
|---|---|
| **First action** | - **Option A:** Nhìn lướt kết quả sai 0/2 ở bài quiz, sau đó bấm ngay nút `[⚡ Xem gợi ý từ Trợ lý]`.<br>- **Option B:** Dừng lại nhìn khung chat ~15 giây, đọc 3 nút gợi ý nhưng không bấm ngay mà ngập ngừng trước ô nhập text.<br>- **Option C:** Đọc dòng thông báo hệ thống tự động soạn bài ôn, di chuột qua nút `[Duyệt]` nhưng chưa bấm, mắt liếc sang nút `[Báo ngoại lệ]`. |
| **Chỗ dừng, do dự hoặc hiểu sai** | - **Dừng ở Option B:** Tester im lặng khá lâu trước ô chat và thốt lên: *"Khi người dùng chưa hiểu bài thì vẫn chưa biết cần hỏi AI về vấn đề gì"* (không biết gõ từ khóa nào để bắt đầu).<br>- **Do dự ở Option A & C:** Sau khi đọc xong đoạn văn giải thích về Chunk Overlap, tester tìm cách hỏi thêm nhưng không thấy chỗ nhập, nhận xét: *"Có giải thích tổng quát nhưng chưa cho phép người dùng hỏi lại khi chưa hiểu"*. |
| **Evidence được đọc hay bỏ qua** | - Tester đọc kỹ đoạn ví dụ trực quan lợp ngói và lý do cắt cụt câu ở Option A.<br>- Ở Option C, tester đọc lướt qua lý do sai, chủ yếu chú ý xem hệ thống đã tự động thay đổi đáp án gì của mình. |
| **Cách tester sửa hoặc lấy lại control** | - Ở Option A: Thử bấm vào các lựa chọn 1, 2, 3 nhưng cảm thấy bị gò bó: *"Luồng hơi ép buộc người dùng vào một khuôn, chưa cho người dùng control được"*. Sau đó bấm nút `🏠 Trang chủ` để đổi phương án.<br>- Ở Option B: Thử bấm nút `[✏️ Lấy ví dụ đời thực]` và gõ thử vào ô ghi chú cá nhân.<br>- Ở Option C: Bấm thử nút `[⚠️ Báo hệ thống hiểu sai / Can thiệp ngoại lệ]` để xem hệ thống phản ứng thế nào khi bị chặn. |
| **Option được chọn** | **Option B** (sau khi được thử các nút đổi góc độ giải thích). |
| **Lý do và trade-off** | *"Mình chọn B vì mình muốn tự quyết định cách học, dù phải đánh đổi là mất công hơn và lúc đầu hơi bối rối không biết hỏi gì. Phương án A và C luồng hơi ép buộc vào một khuôn có sẵn và không cho mình hỏi vặn lại khi có chỗ chưa thủng."* |
| **Evidence chống lại kỳ vọng của nhóm** | - Nhóm kỳ vọng Option A với luồng 2 bước tích hợp sẽ được thích nhất vì nhanh gọn; nhưng tester lại phản ánh mạnh rằng luồng này quá ép buộc (rigid flow).<br>- Nhóm kỳ vọng Option B với khung chat mở sẽ giúp người dùng thoải mái hỏi; nhưng tester lại bị "tê liệt" ban đầu vì không biết phải hỏi gì khi bản thân đang chưa hiểu bài. |

---

## Tách 4 lớp (viết sau test, không suy diễn quá)

- **OBSERVED: Tester đã làm/nói gì? (chỉ sự thật)**
  1. Nguyên văn nhận xét 1: *"Luồng hơi ép buộc người dùng vào một khuôn, chưa cho người dùng control được."*
  2. Nguyên văn nhận xét 2: *"Khi người dùng chưa hiểu bài thì vẫn chưa biết cần hỏi AI về vấn đề gì."*
  3. Nguyên văn nhận xét 3: *"Có giải thích tổng quát nhưng chưa cho phép người dùng hỏi lại khi chưa hiểu."*
  4. Tester dừng lại nhìn khung chat mở của Option B 15 giây mà không gõ phím; chỉ thao tác sau khi nhìn thấy các nút gợi ý định hướng sẵn.
  5. Khi đọc xong đoạn giải thích tổng quát của Option A, tester di chuột tìm kiếm ô nhập để hỏi thêm về cụm từ "mất ngữ cảnh" nhưng không có, buộc phải chọn 1 trong 3 nút cứng có sẵn.

- **INTERPRETED: Nhóm nghĩ điều đó có thể có nghĩa gì? (gắn với Pain A/B, agency, evidence)**
  1. **Nghịch lý của quyền kiểm soát (Control Paradox):** Khi hệ thống dẫn dắt quá chặt chẽ (Option A, Option C), người học cảm thấy bị tước đoạt quyền tự chủ (ép vào khuôn). Tuy nhiên, nếu trao toàn bộ quyền chủ động qua một khung chat trắng (Option B), người học lại rơi vào trạng thái *"không biết mình không biết gì"* (cognitive freeze), không thể tự đặt câu hỏi chất lượng.
  2. **Nhu cầu đối thoại đào sâu ngữ cảnh (Contextual Drill-down):** Lời giải thích tổng quát một chiều (1-shot monologue) không bao giờ giải quyết triệt để sự cố học tập. Người học luôn phát sinh các thắc mắc phụ ngay trên chính câu chữ giải thích của AI (ví dụ: thế nào là "ranh giới cắt", tại sao "mô hình tìm kiếm ngữ nghĩa lại thất bại"). Việc thiếu cơ chế hỏi vặn lại tại chỗ khiến người học cảm thấy bế tắc.

- **DECIDED — NEXT CHANGE (đề xuất của tôi):**
  > **Chốt 1 hướng cải tiến đột phá: Thiết kế cơ chế "Hybrid Scaffolded Drill-down" (Gợi ý định hướng kết hợp Hỏi đào sâu ngữ cảnh):**
  - **Khắc phục nhận xét 2 (không biết hỏi gì):** Giữ lại cơ chế chẩn đoán chủ động từ Option A — AI tự động bóc tách sẵn 2–3 "nghi vấn cốt lõi" cụ thể dựa trên lỗi sai của quiz (thay vì để khung chat trắng bắt người học tự nghĩ).
  - **Khắc phục nhận xét 1 & 3 (bị ép khuôn & không được hỏi lại):** Xóa bỏ các nút lựa chọn cứng nhắc. Trong đoạn văn giải thích của AI, cho phép người học **click trực tiếp vào bất kỳ câu/từ khóa nào chưa hiểu để mở rộng luồng hỏi đáp đào sâu 2 chiều tại chỗ** (In-context Deep Dive), cho đến khi thực sự hiểu bản chất để làm lại quiz.

- **STILL UNPROVEN: Điều gì chưa thể kết luận từ 1 người này?**
  - Chưa thể kết luận liệu tính năng "bấm vào từ khóa để hỏi sâu" có khiến người học bị phân tâm, sa đà vào việc hỏi lan man và làm vỡ mục tiêu hoàn thành bài học trong <10 phút hay không.
  - Chưa chứng minh được liệu phản ứng "bị ép buộc vào khuôn" có lặp lại với nhóm người học mới bắt đầu (novice learners - những người thường thích được cầm tay chỉ việc) hay chỉ xuất hiện ở những sinh viên kỹ thuật có tính tự chủ cao như Tester 1.

---
> Cam kết: note này do chính Tạ Việt Cường trực tiếp facilitate và ghi nhận trung thực từ tester ngoài nhóm. Không dùng AI bịa quote/observation.
