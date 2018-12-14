# Phần I: Phân tích hệ thống

Hệ thống phân quyền người dùng(4):

- Cán bộ quản lý của trường:

  - Thông tin các khoa viện
  - Thông tin về các giàng viên toàn trường
  - Thông tin về các sinh viên toàn trường
  - Quản lý việc đăng ký lớp

- Cán bộ quản lý của từng khoa viện:

  - Thông tin các học phần
  - Mở lớp cho mỗi ký đăng ký
  - Thông tin về các giàng viên thuộc khoa viện
  - Thông tin về các sinh viên thuộc khoa viện

- Giảng viên:
    - Các thông tin cá nhân
    - Danh sách các lớp được phân công
- Sinh viên:
    - Các thông tin cá nhân
    - Đăng ký lớp


# Phần II: Thiết kế hệ thống

# 1. Thiết kế cơ sở dữ liệu :

- [Khoa viện] **Department** ( Dept\_Name, Address, _User\_Id_ )
- [Giảng viên] **Teacher** ( Teacher\_Id, Name, Information, _Dept\_Name, User\_Id_)
- [Sinh viên] **Student** (Student\_Id, Name, Information, _Dept\___Name, User\_Id_)
- [Học phần] **Course** (Course\_Id, Name, Information, Credits, _Dept\___Name_)
- [Lớp học] **Classroom** (Classroom\_Id, Semester, Course\_Id, _Teacher\_Id_)
- [Thời gian, Địa điểm lớp học] **Time\_Slot** ( _Classroom_\_Id, _Semester_, Day_,_ Start\_time_,_ End\_time, Room)
- [Sinh viên đăng ký lớp] **Enrollment** ( _Classroom\_Id __,_ _Semester__ , Student\_Id_, Mid\_Grade, Final\_Grade)
- [Học phần điều kiện] **Prerequisite** (_Course\_Id_, Prereq\_Id)
- [Thời gian mở đăng ký lớp] **Time\_Enrollment** (Semester, Start\_time, End\_time)
- [Người dùng] **User** (Id, Username, Password, _Role\_Id_)
- [Phân quyền] **Role** (Id, Name)


![database](https://user-images.githubusercontent.com/45429771/49976535-041bfe00-ff75-11e8-8084-eb7fb1693d59.png)


# 2. Xây dựng ứng dụng:

 Backend: C#, Asp.net core

        Frontend: Html, Css(Bootstrap), Javascript(Jquery)

        Database: Sql Server
