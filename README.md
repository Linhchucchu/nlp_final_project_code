# nlp_final_project_code
Deep Learning-Based Classification of Scientific Abstracts by Research Methodology

Các bài báo trên arXiv chỉ có nhãn chung chung như cs.AI, cs.LG. Nó không gán nhãn chi tiết phương pháp nghiên cứu là "Thực nghiệm" hay "Khảo sát". Vì vậy, muốn làm, cần phải ngồi đọc lại và gán nhãn thủ công toàn bộ cho hàng nghìn thậm chí hàng trăm nghìn bài báo - đây là việc bất khả thi, hơn thế nữa, cách gán nhãn này có khả năng xảy ra sai sót cực kỳ lớn, làm ảnh hưởng đến chất lượng data và model sau này.

Vì vậy, trong báo cáo này, quyết định chọn tập dữ liệu PubMed vì đây là nguồn dữ liệu Benchmark uy tín, có hệ thống nhãn được xác thực bởi các chuyên gia y tế. Điều này giúp đảm bảo tính khách quan khi huấn luyện mô hình SciBERT, tránh việc sai số do gán nhãn thủ công không chuẩn xác như ở các lĩnh vực khác."

Dự án sử dụng Deep Learning để tự động phân loại phương pháp nghiên cứu của các **bài báo y khoa** trên PubMed thành 4 nhóm chính: **Case Report, Meta-Analysis, Observational Study, và Randomized Controlled Trial**.

Các bài báo này được scapping tự động từ PubMed thông qua Biopython/Entrez.

Model chính là Scibert, sử dụng mô hình Transformer được tiền huấn luyện trên 1.14 triệu bài báo y khoa.

Sau quá trình huấn luyện và kiểm thử, mô hình SciBERT vượt trội hoàn toàn so với các phương pháp truyền thống:

| Model | Accuracy | F1-Score |
| :--- | :---: | :---: |
| Naive Bayes | 91.08% | 0.91 |
| Bi-LSTM | 96.34% | 0.96 |
| SciBERT | 98.27% | 0.98 |
