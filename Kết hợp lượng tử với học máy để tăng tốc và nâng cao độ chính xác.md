1. Định nghĩa & động lực phát triển
Quantum Machine Learning (QML) là lĩnh vực liên ngành tận dụng ưu thế song song, không gian trạng thái cao chiều của lượng tử để xử lý các bài toán học máy, mở rộng năng lực vượt quá mô hình cổ điển. Mục tiêu:
- Tăng tốc huấn luyện, tối ưu hóa và dự đoán
- Phân tích dữ liệu phức tạp, không gian đặc trưng phi tuyến
- Mở ra mô hình AI thế hệ mới hợp nhất classical + quantum
Các hướng chủ lực của QML gồm: tăng tốc kernel methods (SVM, clustering), học sâu lượng tử (QNN, GNN, QCNN), tối ưu hóa (QAOA), mô phỏng lượng tử cho khoa học vật liệu/hóa học.
2. Kiến trúc hybrid quantum-classical
Phổ biến nhất hiện nay là hybrid quantum-classical (HQML), kết hợp các lớp/mô-đun lượng tử (quantum layer) vào pipeline học máy cổ điển. Quy trình gồm:
- Encoding dữ liệu cổ điển thành trạng thái qubit (angle encoding, amplitude encoding, basis encoding...).
- Cho dữ liệu đi qua mạch lượng tử tham số hóa (Variational Quantum Circuit, VQC).
- Đo lường đầu ra, lấy giá trị cổ điển (expectation value).
- Tối ưu hóa parameters mạch lượng tử bằng thuật toán cổ điển (Adam, SGD, COBYLA…).
- Ghép với các lớp cổ điển: dense, softmax, classifier.
Ưu điểm HQML:
- Tận dụng tối đa ưu thế song song hóa của lượng tử (mô hình hóa đặc trưng phi tuyến, rối lượng tử, ánh xạ kernel phức tạp).
- Giảm tải yêu cầu phần cứng lượng tử, tăng tính khả thi trên nền tảng NISQ.
3. Variational Quantum Circuits (VQC) và nguyên lý
Variational Quantum Circuit là mạch lượng tử với các tham số có thể huấn luyện, tạo không gian biểu diễn cực kỳ lớn. Trong pipeline QML, VQC thay thế các layer non-linear của mô hình classical:
- Các tham số được tối ưu bằng gradient hoặc rule như parameter-shift.
- Độ sâu mạch (number of layers) và loại cổng (entanglement, rotation) quyết định khả năng biểu diễn.
VQC là nền tảng của:
- Quantum Neural Network (QNN)
- Variational Quantum Eigensolver (VQE)
- Quantum GAN, quantum classifier v.v.
- Được triển khai linh hoạt trên Qiskit, PennyLane, TensorFlow Quantum.
4. Phương pháp Quantum Kernel và ứng dụng phân loại
Phương pháp kernel lượng tử tận dụng ánh xạ đặc trưng phi tuyến phức tạp của không gian Hilbert lượng tử, giúp phân loại dữ liệu vượt trội classical kernel:
- Dùng quantum circuit ánh xạ dữ liệu lên không gian đặc trưng (feature map), ví dụ: zz_feature_map hoặc custom circuit.
- Tính inner product trong không gian Hilbert nhờ phép đo trên trạng thái lượng tử.
- Sinh kernel matrix (ma trận tương đồng) cho bộ dữ liệu.
- Áp dụng các phương pháp cổ điển như SVM, clustering với kernel này.
Ứng dụng: Phân loại ảnh, phát hiện gian lận tài chính, nhận diện gene bệnh, tối ưu hóa, v.v. Các kết quả gần đây ghi nhận quantum kernel giúp nâng cao độ chính xác phân loại các bài toán phi tuyến, mở rộng vùng mà máy học cổ điển gặp khó khăn.


