# KTPM_Tuan09: Event-Driven architecture

### Example model

![evnet.png](img/evnet.png)

![img01.png](img/img01.png)

Bên client dùng port 8083, services dùng port 8081
![Screenshot 2024-05-03 211452.jpg](img/Screenshot%202024-05-03%20211452.jpg)

Bên Client định nghĩa một endpoint POST "http://localhost:8083/api/orders/" để nhận dữ liệu đơn hàng dưới dạng JSON sau đó trả về một thông báo cho biết đơn hàng đã được gửi thành công.

![Screenshot 2024-05-03 215727.jpg](img/Screenshot%202024-05-03%20215727.jpg)

Test method post trên postman
![Screenshot 2024-05-03 215313.jpg](img/Screenshot%202024-05-03%20215313.jpg)

Bên Services sẽ lắng nghe các tin nhắn từ message broker sử dụng JMS (Java Message Service).
![Screenshot 2024-05-03 215648.jpg](img/Screenshot%202024-05-03%20215648.jpg)

Bên service sẽ nhận thông tin order dưới dạng chuỗi json
![Screenshot 2024-05-03 215405.jpg](img/Screenshot%202024-05-03%20215405.jpg)

Một tin nhắn được gửi tới chủ đề "processing_order_1".
![Screenshot 2024-05-03 215444.jpg](img/Screenshot%202024-05-03%20215444.jpg)
