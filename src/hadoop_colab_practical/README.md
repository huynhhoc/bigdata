# THỰC HÀNH CHƯƠNG 2 — HADOOP TRÊN GOOGLE COLAB

## Notebook

- `Hadoop_Practical_Online_Colab.ipynb`: bài thực hành chính, gồm HDFS, block, replication, YARN, MapReduce, tự kiểm tra Hadoop và phần mở rộng so sánh PySpark.
- `HDFS_FileSystem_Shell_Lab_Colab.ipynb`: bài bổ trợ chuyên sâu về FileSystem Shell.

## Thứ tự sử dụng đề xuất

1. Dạy slide Chương 2 đến cơ chế đọc/ghi HDFS.
2. Chạy Bài 1–4 trong notebook chính.
3. Dạy YARN và MapReduce.
4. Chạy Bài 5–8 trong notebook chính.
5. Dùng Bài 9–10 để củng cố Hadoop 3.x và tự kiểm tra.
6. Bài 11 PySpark là phần mở rộng, giúp so sánh DataFrame với Hadoop Streaming.
7. Dùng notebook FileSystem Shell cho giờ tự học hoặc buổi thực hành tăng cường.

## Môi trường

- Google Colab
- Apache Hadoop 3.5.0
- Java 17
- Pseudo-distributed single-node

## Tài liệu chính thức

- [Apache Hadoop 3.5.0](https://hadoop.apache.org/docs/r3.5.0/)
- [HDFS Architecture](https://hadoop.apache.org/docs/r3.5.0/hadoop-project-dist/hadoop-hdfs/HdfsDesign.html)
- [FileSystem Shell](https://hadoop.apache.org/docs/r3.5.0/hadoop-project-dist/hadoop-common/FileSystemShell.html)
- [Single Node Setup](https://hadoop.apache.org/docs/r3.5.0/hadoop-project-dist/hadoop-common/SingleCluster.html)
- [PySpark DataFrame Quickstart](https://spark.apache.org/docs/latest/api/python/getting_started/quickstart_df.html)

## Usage

Upload notebook lên Google Drive → Open with Google Colaboratory → chạy tuần tự từ PHẦN 0.

> Colab chỉ có một DataNode. Đây là môi trường học workflow, không phải minh họa đầy đủ fault tolerance của cluster production.
