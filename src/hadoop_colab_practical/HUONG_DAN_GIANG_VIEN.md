# HƯỚNG DẪN GIẢNG VIÊN — HADOOP PRACTICAL TRÊN GOOGLE COLAB

## 1. Mục tiêu
Bộ thực hành bám theo lecture Big Data và Hadoop:
- DFS và replication
- HDFS, NameNode, DataNode
- Block
- HDFS administration
- YARN: ResourceManager, NodeManager, ApplicationMaster, Container
- MapReduce

## 1.1 Liên kết bài giảng và thực hành

| Nội dung bài giảng | Hoạt động trong notebook | Minh chứng |
|---|---|---|
| DFS, HDFS, NameNode, DataNode | Bài 1 | `put`, `ls`, `cat`, `get` |
| Block | Bài 2 | `fsck -files -blocks -locations` |
| Replication, fault tolerance | Bài 3 | `stat`, `setrep`, trạng thái under-replicated |
| HDFS administration | Bài 4 | `dfsadmin -report`, `fsck /` |
| YARN | Bài 5 | `yarn node`, `yarn application` |
| MapReduce | Bài 6–8 | WordCount và Hadoop Streaming |

## 2. Môi trường
- Google Colab
- Apache Hadoop 3.5.0
- Java 17
- pseudo-distributed single-node

## 3. Thời lượng đề xuất

### Buổi 1 — HDFS (150–180 phút)
- 20 phút: setup + architecture
- 40 phút: HDFS shell
- 35 phút: block
- 25 phút: replication/fault tolerance
- 20 phút: administration
- 30 phút: bài tập

### Buổi 2 — YARN + MapReduce (150–180 phút)
- 25 phút: YARN
- 45 phút: WordCount
- 60 phút: Hadoop Streaming + sales
- 30 phút: bài tổng hợp

## 4. Điểm cần nhấn mạnh
Colab không phải cluster nhiều máy. Pseudo-distributed mode tạo các Hadoop daemon riêng nhưng chỉ có một DataNode và một NodeManager.

Do đó:
- dùng Colab để học lệnh, workflow và kiến trúc;
- dùng slide/sơ đồ hoặc cluster multi-node của giảng viên để minh họa fault tolerance thực.

Không gọi SecondaryNameNode là NameNode dự phòng. Vai trò cơ bản của nó là tạo checkpoint bằng cách gộp namespace image và edit log; HA cần kiến trúc NameNode riêng.

Trong YARN, trình tự cần giảng đúng: client submit → ResourceManager cấp container đầu tiên để chạy ApplicationMaster → ApplicationMaster đăng ký và xin container → NodeManager khởi chạy task containers.

## 5. Cách phát bài
1. Upload notebook vào Google Drive hoặc LMS.
2. Sinh viên mở bằng Google Colab.
3. Chọn File → Save a copy in Drive.
4. Chạy từ PHẦN 0.
5. Nếu Runtime reset, chạy lại notebook từ đầu.

## 6. Chuẩn đầu ra
Sinh viên giải thích được:
- Local FS vs HDFS
- NameNode vs DataNode
- Block
- Replication
- ResourceManager vs NodeManager
- Map → Shuffle → Reduce

## 7. Đánh giá
Rubric 10 điểm nằm ở cuối notebook.

Yêu cầu sinh viên đối chiếu output MapReduce với kết quả tính tay hoặc Python thuần; không chỉ chụp ảnh job chạy thành công.
