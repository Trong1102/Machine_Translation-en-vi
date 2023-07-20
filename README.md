# Machine Translation with Transfomer
## Datasets
[Dataset](https://drive.google.com/file/d/1Fuo_ALIFKlUvOPbK5rUA5OfAS2wKn_95/view)

## Tổng quan
### [Huấn luyện mô hình en-vi](https://github.com/Trong1102/Machine_Translation-en-vi/blob/main/Train_Transfomer_en_vi.ipynb)
### [Huấn luyện mô hình vi-en](https://github.com/Trong1102/Machine_Translation-en-vi/blob/main/Train_Transfomer_vi_en.ipynb)
### [Sử dụng mô hình](https://github.com/Trong1102/Machine_Translation-en-vi/blob/main/Transformer_translate.ipynb)

## Tóm tắt nội dung
### Mô tả về dự án
Dự án Dịch máy nhằm giải quyết bài toán dịch ngôn ngữ giữa tiếng Việt và tiếng Anh. Mục tiêu của dự án là tạo ra một mô hình dịch máy hiệu quả, có khả năng dịch chính xác và tự nhiên. Dự án có ý nghĩa thực tế bởi sự cần thiết của việc giao tiếp và chuyển đổi giữa các ngôn ngữ trong thế giới đa văn hóa ngày nay.

### Phương pháp và mô hình
Trong dự án, chúng tôi sử dụng mô hình Transformer làm cơ sở cho dịch máy. Mô hình Transformer là một kiến trúc mạng nơ-ron sử dụng cơ chế Attention để tập trung vào các phần quan trọng của câu đầu vào và tạo ra các dự đoán cho câu đầu ra. Mô hình bao gồm các lớp encode, decode và self-attention.

Lớp "encode" : Nhận đầu vào là câu tiếng Anh và biểu diễn từng từ trong câu sử dụng lớp self-attention.
Lớp "decode" : Nhận đầu vào là kết quả từ lớp encode và câu tiếng Việt đã được dịch một phần hoặc toàn bộ. Lớp này sử dụng cơ chế attention để tạo ra các dự đoán cho từng từ trong câu đầu ra.
"Self-attention" : Là một cơ chế quan trọng trong Transformer, self-attention giúp mô hình tập trung vào các từ trong câu và xác định mức độ quan trọng của từng từ đối với các từ khác trong câu.
Cùng với đó, chúng tôi áp dụng phương pháp beam-search để tìm kiếm các dự đoán tốt nhất trong quá trình dịch.

### Quy trình xử lí dữ liệu
Trước khi đưa vào mô hình, dữ liệu tiếng Việt và tiếng Anh được tiền xử lí. Các công việc tiền xử lí có thể bao gồm tách từ, chuẩn hóa chữ viết hoa, loại bỏ ký tự đặc biệt và mã hóa văn bản thành các vector số hóa. Dữ liệu được chia thành các tập huấn luyện, kiểm tra và đánh giá để đảm bảo đánh giá hiệu suất và chất lượng của mô hình dịch máy.

### Kết quả và đánh giá
Để đánh giá hiệu suất và chất lượng của mô hình dịch máy, chúng tôi sử dụng các phương pháp đánh giá như BLEU (BiLingual Evaluation Understudy) để so sánh kết quả dịch với các bản dịch tham chiếu chuẩn. Đánh giá được thực hiện trên tập dữ liệu kiểm tra và đánh giá để đảm bảo mô hình hoạt động tốt trên các dữ liệu mới.

### Tài liệu tham khảo
Trong dự án Dịch máy, chúng tôi tham khảo các tài liệu và bài báo sau để nắm vững các khái niệm, kỹ thuật và phương pháp liên quan đến dịch máy và mô hình Transformer:

Vaswani, A., Shazeer, N., Parmar, N., Uszkoreit, J., Jones, L., Gomez, A. N., ... & Polosukhin, I. (2017). "Attention is all you need." Advances in Neural Information Processing Systems, 5998-6008.
Sutskever, I., Vinyals, O., & Le, Q. V. (2014). "Sequence to sequence learning with neural networks." Advances in Neural Information Processing Systems, 3104-3112.
Bahdanau, D., Cho, K., & Bengio, Y. (2014). "Neural machine translation by jointly learning to align and translate." arXiv preprint arXiv:1409.0473.
