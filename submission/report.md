1. Tôi dùng AWS, us-east-1 (N. Virginia), EC2 t3.medium cho compute node; source commit 55539f6.
2. Dataset có 284.807 dòng và 30 đặc trưng; train/test lần lượt 227.845/56.962 dòng, seed không ghi nhận trong bằng chứng hiện có.
3. Load dữ liệu mất 2,412 giây; training mất 2,570 giây; best iteration là 1.
4. AUC 0,951654; Accuracy 0,998947; F1 0,727273; Precision 0,655738; Recall 0,816327 trên tập test.
5. Latency 1 dòng 1,240 ms; throughput batch 1.000 dòng 631.052 dòng/giây; đo bằng benchmark.py trên compute node.
6. Tài nguyên được quan sát sau benchmark: top ghi CPU idle 99,7%, RAM 3,7 GiB tổng/3,2 GiB khả dụng; ip -s link ghi nhận ens5 RX 276.902.388 và TX 1.126.473 bytes.
7. Billing ngày 04/10/2026 chưa có dữ liệu; Bills hiển thị estimated grand total USD 0,00 và Cost Management yêu cầu chờ khoảng 24 giờ cập nhật.
8. Ảnh 06 cho thấy không còn instance trong Asia Pacific (Singapore). Tôi đã tải kết quả trước đó và xóa hoàn toàn tài nguyên vào lúc 1 giờ 21 phút sáng ngày 04/10/2026.