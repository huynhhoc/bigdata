# THỰC HÀNH CHƯƠNG 2 — HADOOP TRÊN GOOGLE COLAB

## Notebook

- `bai_thuc_hanh_hadoop_colab.ipynb`: bài thực hành Hadoop chính thức của Chương 2.

## Nội dung chính

- Cài đặt Apache Hadoop 3.5.0 và Java 17 trên Google Colab.
- Khởi tạo Hadoop ở chế độ pseudo-distributed single-node.
- Thực hành HDFS FileSystem Shell và quan sát block/replication.
- Chạy MapReduce và kiểm tra kết quả trên HDFS.
- Giải thích giới hạn của môi trường Colab so với một Hadoop cluster production.

## Cách sử dụng

1. Mở `bai_thuc_hanh_hadoop_colab.ipynb` bằng Google Colab.
2. Chọn **Runtime → Run all** hoặc chạy tuần tự từ trên xuống.
3. Không chạy lại bước format NameNode khi các Hadoop daemon đang hoạt động.

> Google Colab chỉ chạy một DataNode. Notebook minh họa quy trình sử dụng Hadoop, không thể hiện đầy đủ khả năng chịu lỗi của một cluster nhiều máy.
