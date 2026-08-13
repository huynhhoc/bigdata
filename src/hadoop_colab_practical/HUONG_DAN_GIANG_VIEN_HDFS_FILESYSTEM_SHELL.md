# HƯỚNG DẪN GIẢNG VIÊN — HDFS FILESYSTEM SHELL LAB

## Mục tiêu
Bài thực hành tập trung riêng vào Hadoop FileSystem Shell.

## Nội dung chính
1. help
2. mkdir / ls
3. put / copyFromLocal
4. cat / head / tail
5. appendToFile / touch / touchz
6. cp / mv
7. du / df / count
8. stat / checksum
9. find / test
10. get / copyToLocal / getmerge
11. chmod
12. setrep
13. rm / rmdir
14. bài tổng hợp file lifecycle

## Thời lượng đề xuất
### Buổi 1 — 150 phút
- Setup: 20'
- Directory + upload: 35'
- Read + append: 30'
- cp/mv: 20'
- du/df/count: 25'
- bài tập: 20'

### Buổi 2 — 120–150 phút
- stat/checksum/find/test: 35'
- get/getmerge: 25'
- permission/replication: 25'
- delete: 15'
- bài tổng hợp: 40'

## Lưu ý
Google Colab dùng HDFS pseudo-distributed single-node.
Do đó:
- phù hợp để luyện FileSystem Shell;
- replication thực tế chỉ có một DataNode;
- không dùng notebook này để demo fault tolerance multi-node.

`setrep` chỉ đặt số replica mong muốn; nó không tạo thêm DataNode. Có thể cho sinh viên đặt replication = 3 để quan sát under-replicated, nhưng phải đưa về 1 và không dùng `-w 3` vì lệnh sẽ chờ không có điểm kết thúc trên single-node.

Khi giải thích `du`, phân biệt kích thước logic của file với dung lượng tiêu thụ có tính replication.
