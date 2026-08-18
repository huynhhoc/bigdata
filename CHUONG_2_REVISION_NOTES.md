# GHI CHÚ HIỆU ĐÍNH — CHƯƠNG 2 HADOOP

Ngày hiệu đính: 13/08/2026

## Phạm vi

- `02.Hadoop.pptx`
- `Lectures/Lecture 2 Hadoop.pptx`
- `src/hadoop_colab_practical/Hadoop_Practical_Online_Colab.ipynb`
- `src/hadoop_colab_practical/HDFS_FileSystem_Shell_Lab_Colab.ipynb`
- Các hướng dẫn giảng viên trong `src/hadoop_colab_practical/`

## Những điểm đã sửa trong bài giảng

- Phân biệt đúng node và cluster trong định nghĩa distributed file system.
- Diễn đạt replication theo block replica trên DataNode/rack; không xem replication là cơ chế tạo bản sao sang “cluster” khác.
- Thay các số liệu quy mô cũ, thiếu nguồn bằng các đặc tính kiến trúc ổn định.
- Cập nhật vai trò NameNode, DataNode, block và replication factor.
- Thay thuật ngữ master/slave bằng manager/worker khi mô tả kiến trúc.
- Làm rõ bốn thành phần YARN và sửa đúng trình tự chạy application.
- Thay liên kết blog Hadoop 2.x bằng tài liệu cluster setup chính thức.
- Bổ sung mô hình MapReduce và vai trò của Shuffle/Sort.
- Bổ sung ví dụ WordCount theo luồng Map → Shuffle/Sort → Reduce.
- Nêu rõ workload phù hợp và các giới hạn thiết kế của HDFS.
- Bổ sung các điểm quan trọng của Hadoop 3.x/Hadoop 3.5.0.
- So sánh replication với erasure coding và giới hạn minh họa trên Colab single-node.
- Đồng bộ phần kết thúc bài giảng với notebook Hadoop và bài PySpark mở rộng.

## Những điểm đã sửa trong bài thực hành

- Giữ Hadoop 3.5.0 và Java 17, phù hợp tài liệu chính thức của dòng 3.5.
- Làm setup shell an toàn hơn khi xử lý path và có thể chạy lại.
- Sửa thao tác copy HDFS để cell chạy lại không lỗi vì file đích đã tồn tại.
- Sửa sơ đồ và câu hỏi YARN theo đúng lifecycle của ApplicationMaster/container.
- Bổ sung bước đối chiếu kết quả MapReduce thay vì chỉ kiểm tra job thành công.
- Làm rõ `setrep`, under-replication và giới hạn single-node.
- Bổ sung mapping giữa slide, bài thực hành và minh chứng cần nộp.

## Gợi ý phân phối

- Phần lý thuyết DFS/HDFS + Bài 1–4: 150–180 phút.
- Phần lý thuyết YARN/MapReduce + Bài 5–8: 150–180 phút.
- Notebook FileSystem Shell: bài bổ trợ hoặc buổi thực hành riêng 120–180 phút.

## Nguồn chuẩn dùng để đối chiếu

- Apache Hadoop 3.5.0 documentation: <https://hadoop.apache.org/docs/r3.5.0/>
- HDFS Architecture: <https://hadoop.apache.org/docs/r3.5.0/hadoop-project-dist/hadoop-hdfs/HdfsDesign.html>
- FileSystem Shell: <https://hadoop.apache.org/docs/r3.5.0/hadoop-project-dist/hadoop-common/FileSystemShell.html>
- Single Node Setup: <https://hadoop.apache.org/docs/r3.5.0/hadoop-project-dist/hadoop-common/SingleCluster.html>
- Cluster Setup: <https://hadoop.apache.org/docs/r3.5.0/hadoop-project-dist/hadoop-common/ClusterSetup.html>
