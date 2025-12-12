# Tạo hệ thống mạng lưới nhà khoa học

Module xây dựng hệ thống mạng lưới nhà khoa học quốc tế.

## Mô tả

Thực hiện trích xuất thông tin và đồ thị hóa.

Tech stack: Neo4j, neomodel, pandas.

## Docs

Tư liệu cho báo cáo: `/professors/docs/`

## Source

Source code: `/professors/src`

## Chạy dự án:

Khởi tạo môi trường:

```bash

python3 -m venv .venv

source .venv/bin/activate

pip install -r requirements.txt

#set up file .env 
# for neo4j db

pip install -e .



```

Crawl dữ liệu: `python3 src/GraphBuilder/crawl/crawl.py`

Tạo mạng: `python3 src/main.py`




# 1. Cài đặt
pip install -r requirements.txt

# 2. Khởi động Neo4j Desktop (tạo DB tên "nobel")

# 3. Xây index (chạy 1 lần)
python graphrag/build_graph.py

# 4. Sinh bộ đánh giá
python evaluation/generate_questions.py

# 5. Demo chatbot
python server.py 




# demo_graph.bat






## 02_ner – Named Entity Recognition (0.75 điểm)

### Label system (đúng yêu cầu đề bài)
- PERSON     → Nhà khoa học
- ORG        → Trường ĐH, viện nghiên cứu
- FIELD      → Lĩnh vực (AI, Physics, Mathematics...)
- AWARD      → Nobel Prize, Turing Award, Fields Medal...
- COUNTRY    → Vietnam, United States, France...

### Model sử dụng


### Cách chạy
python src/02_ner/infer_ner.py

→ Kết quả: data/processed/entities_extracted.jsonl (mỗi dòng là 1 nhà khoa học + list entity)
