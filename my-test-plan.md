# Kế hoạch test của Cường — Tester 1 (cả A/B/C, 20 phút)
> Phần việc Chặng 5 của Cường. Tester ngoài nhóm, ưu tiên người từng bị mắc kẹt khi học 7 ngày qua. Người điều khiển prototype là tester.

## Kịch bản nói nguyên văn
- **Opening:** "Chúng mình đang thử ba cách thiết kế, không kiểm tra bạn. Không có đúng/sai. Bạn hãy tự thao tác và nói rõ suy nghĩ của bạn sau quá trình thử nghiệm 3 phương án tương tác; mình sẽ cố gắng không hướng dẫn."
- **Relevant context (0-2'):** "Trong 7 ngày qua có lúc nào bạn học mà phải dừng lại vì không hiểu không? Đó là môn / bài gì?"
- **Outcome task (dùng chung cho A/B/C):** "Bạn đang học dở bài RAG này và vừa sai quiz 2 lần. Hãy dùng từng phương án A, B, C để tìm chỗ đang thiếu và quay lại làm tiếp bài."
- **Thứ tự thử nghiệm:** Trang chủ (M0) → A (4') → Trang chủ → B (4') → Trang chủ → C (4'). Tester tự bấm, không giải thích thay.
- **Compare (14-18'):** 
  * "Trong tình huống này, bạn chọn A, B hay C? Vì sao?"
  * "Bạn muốn tự làm phần nào và giao cho AI phần nào?"
  * "Ở Option B (đối thoại 2 chiều có nút can thiệp) và Option C (AI tự chạy ngầm có nút báo ngoại lệ), bạn thấy cách kiểm soát nào thoải mái hơn?"
  * "Điều gì ở phương án đã chọn khiến bạn chưa hài lòng?"
- **3 câu cứu hộ duy nhất:** "Bạn cứ nói to suy nghĩ nhé." / "Bạn sẽ làm gì tiếp theo?" / "Theo bạn, nó nên hoạt động như thế nào?"
- **Cấm:** giải thích giao diện hộ, lấp im lặng, hỏi "Bạn có thích không?".

## Observation focus của Cường (tối đa 5, ghi vào feedback-note)
1. **First action:** Ở A có bấm kích hoạt không? Ở B có bấm thử các nút chỉnh sửa góc độ không? Ở C có đọc log ngầm trước khi bấm duyệt không?
2. **Hesitation / Hiểu sai:** Dừng lại ở màn nào lâu nhất? Có hiểu lý do vì sao AI đưa ra gợi ý đó không?
3. **Phản ứng với Quyền kiểm soát của User:**
   - Option A: Có dùng nút đổi sang câu hỏi Top-k hoặc từ chối gợi ý không?
   - Option B: Có thử nghiệm các nút chỉnh sửa góc độ (Ví dụ đời thực / Bảng so sánh) và gõ sửa ô ghi chú không?
   - Option C: Có phát hiện và nhấn thử nút [⚠️ BÁO NGOẠI LỆ / CAN THIỆP] hay chỉ bấm Duyệt tự động?
4. **Correction / Recovery:** Cách tester thoát ra hoặc quay lại bài học (nút Trang chủ, nút từ chối).
5. **Option được chọn + Trade-off nguyên văn:** Trích dẫn chính xác lời giải thích và đánh đổi của tester.

## Checklist sau test (18-20')
- [x] Điền `prototype-feedback-note.md` ngay: hành vi trước, diễn giải sau, tách OBSERVED / INTERPRETED / DECIDED / STILL UNPROVEN.
- [x] Không bịa quote, không tuyên bố validated.
- [x] Gửi 1 dòng Next Change đề xuất của mình vào Doc chung để gộp Group Synthesis.
