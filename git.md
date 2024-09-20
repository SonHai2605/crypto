## tạo respository (repo)

git init

> > > nhánh chính : master

#### git init -b main

> tạo repo local với nhánh chính có tên main

### git remote add origin + <url repo>

> liên kết repo local và repo remote

### không đưa thư mục node_modules lên repo remote

> node_modules chiếm dl rất lớn
> node_modules có thể cài lại thông qua câu lệnh L: npm i

### file .gitignore quy định những thư mục hay file không được phép đẩy lên repo remote

> > file .gitignore nằm ở ngoài thư mục root

### git status

> > kiểm tra sự thay đổi của các file trong dự án

### git add

=> thêm file vào trong staging

## git add . >> dùng để thêm tất cả các file ở trong thư mục hiện tại vào trong staging

## git add -A >> dùng để thêm tất cả các file ở trong dự án vào trong staging

## git add <đường dẫn fiel> >> chỉ thêm file cụ thể vào trong staging

### working directoy (file màu đỏ)

### staging (file màu xanh)

> lúc này file sẵn sàng để đưa lên repo remote

### git commit -m "message"

> > dùng để gắn message vào trong những file đang ở staging đc phép đưa lên repo remote
> > mỗi commit có một mã sha (id)

### git log

> > kiểm tra lịch sử commit

### muốn chuyển qua nhánh khác trong git thì phải commit hết các file đang sửa or chưa sửa và chưa commit lên git repo remote
