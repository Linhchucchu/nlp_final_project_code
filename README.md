# nlp_final_project_code
Deep Learning-Based Classification of Scientific Abstracts by Research Methodology

Dự án sử dụng Deep Learning để tự động phân loại phương pháp nghiên cứu của các bài báo y khoa trên PubMed thành 4 nhóm chính: Case Report, Meta-Analysis, Observational Study, và Randomized Controlled Trial.

Mô hình SciBERT vượt trội hoàn toàn so với các phương pháp truyền thống:

| Model | Accuracy | F1-Score |
| :--- | :---: | :---: |
| Naive Bayes | 91.08% | 0.91 |
| Bi-LSTM | 96.34% | 0.96 |
| SciBERT | 98.27% | 0.98 |

Cấu trúc thư mục trong bài này như sau

├── Data/                 # Dữ liệu thu thập từ PubMed
├── Notebooks/            # 8 File code từ Scraping đến Inference
│   ├── File1_Scrapping.ipynb
│   ├── ...
│   └── File8_Realtime_Demo.ipynb
├── Models/               # Chứa trọng số (.weights.h5) và Full Model
└── Results/              # Các biểu đồ đánh giá (ROC, PR Curve, Heatmap)
