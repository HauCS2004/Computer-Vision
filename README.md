# 🚗 Hệ Thống Nhận Diện Biển Số Xe (License Plate Recognition)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![OpenCV](https://img.shields.io/badge/Library-OpenCV-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

Dự án thuộc học phần **Thị giác máy tính (Computer Vision)**. Hệ thống thực hiện việc phát hiện và nhận diện các ký tự trên biển số xe từ hình ảnh đầu vào.

---

## 🛠️ Quy trình hoạt động (Methodology)

Mô hình hoạt động dựa trên quy trình xử lý ảnh tuần tự gồm các bước chính: Tiền xử lý, Tách biên, Xác định vùng biển số và Nhận diện ký tự.

![Sơ đồ thuật toán](https://github.com/user-attachments/assets/ee851bee-a349-42c2-a173-bfe0c53663b2)

### Chi tiết các bước xử lý:
1.  **Input Image:** Nhận ảnh đầu vào từ camera hoặc file.
2.  **Grayscale & Histogram Equalization:** Chuyển ảnh sang mức xám và cân bằng sáng để tăng độ tương phản.
3.  **Canny Edge Detection:** Sử dụng thuật toán Canny để phát hiện các cạnh trong ảnh.
4.  **Find Contours:** Tìm các đường bao (contours) khép kín để xác định ứng viên biển số.
5.  **License Plate Extraction:** Cắt vùng ảnh chứa biển số xe.
6.  **Character Segmentation:** Phân tách từng ký tự trong biển số.
7.  **Recognition:** Nhận diện ký tự (Sử dụng KNN/CNN hoặc Tesseract OCR).

---

## 📸 Kết quả thực nghiệm (Results)

Hệ thống đã thử nghiệm trên nhiều điều kiện ánh sáng và góc chụp khác nhau. Dưới đây là một số kết quả nhận diện thành công:

| Ảnh gốc (Input) | Biển số trích xuất & Kết quả |
| :---: | :---: |
| **Trường hợp 1** | <img src="https://github.com/user-attachments/assets/2c1b010c-9321-4d00-bfba-376c1d600c97" width="100%"> |
| **Trường hợp 2** | <img src="https://github.com/user-attachments/assets/69091789-b534-4200-b690-081c7de52e26" width="100%"> |

> **Nhận xét:** Mô hình hoạt động tốt với các biển số rõ nét, ánh sáng ban ngày. Tốc độ xử lý trung bình ~0.5s/ảnh.

---

## 🚀 Cài đặt và Hướng dẫn sử dụng

### Yêu cầu hệ thống
* Python 3.x
* OpenCV, NumPy, Matplotlib

### Cài đặt thư viện
```bash
pip install opencv-python numpy matplotlib imutils
