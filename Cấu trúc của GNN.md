Cấu trúc của GNN: Node, Edge, Message Passing, Embedding
Thành phần cơ bản:
•	Node (Đỉnh): Đại diện thực thể (cảm biến, thiết bị IoT, server, dịch vụ, điểm kết nối, người dùng,...). Đặc trưng node: thuộc tính vật lý, địa chỉ, năng lực, trạng thái hoạt động...
•	Edge (Cạnh): Mô tả mối liên hệ (luồng dữ liệu, sự kiện chung, giao tiếp vật lý hoặc logic, truyền thông,...), có thể có trọng số, hướng, thuộc tính động (băng thông, loại tấn công, độ trễ).
•	Edge Features: Có thể là vector số thực/categorical biểu diễn đặc thù kết nối.
•	Graph Structure: Khung đồ thị mô tả topology vật lý hoặc logic.
Cốt lõi của GNN là chu trình message passing: Mỗi node trong đồ thị sẽ lặp lại quá trình nhận, tổng hợp (aggregate) và cập nhật (update) thông tin từ các node hàng xóm qua các edge theo từng lớp (layer). Mỗi lớp, trạng thái (embedding) của node sẽ dần dần bao trùm cả các hàng xóm xa hơn (k-hop neighborhood). Điều này cho phép mỗi node tích lũy thông tin từ mạng lưới lớn hơn mà không mất tính cục bộ ban đầu.
Phép toán embedding cuối cùng sẽ ánh xạ thông tin của các node, edge sang không gian véctơ liên tục, dưới dạng low-dimensional vector representation, phục vụ các tác vụ như phân loại node, link prediction, phân loại/cluster toàn đồ thị, hoặc phát hiện điểm bất thường.
