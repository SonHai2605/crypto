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

### config git ( chỉ chạy duy nhất một lần)

### git config --global user.name "họ và tên"

### git config --global user.name "...@gmail.com"

### git commit -m "message"

> > dùng để gắn message vào trong những file đang ở staging đc phép đưa lên repo remote
> > mỗi commit có một mã sha (id)

### git log

> > kiểm tra lịch sử commit

<<<<<<< HEAD

### muốn chuyển qua nhánh khác trong git thì phải commit hết các file đang sửa or chưa sửa và chưa commit lên git repo remote

=======

### git push -u origin <tên nhánh>

=> đưa code lên repo remote
=> từ lần push code thứ 2 : git push

### đưa file từ staging về lại working

git reset
git restore -S . (đưa all các file đang ở staging về working)

git restore -S <url file> (chỉ đưa duy nhất file về working)

### git checkout <url file>

=> đưa 1 file đang được chỉnh sửa về cái trạng thái trước đó của nó

### git checkout -b <tên nhánh>

=> tương đương với 2 lệnh git branch + git switch

### git checkout < tên nhánh>

=> tương đương với lệnh git switch
=> dùng để chuyển qua <tên nhánh>

### branch

// dev => kiếm thử QA và DEV (dev)

// staging => QA kiếm thử 1 lần (staging)

// production => end user dùng (main/release)

git branch <tên nhánh>
=> tạo ra 1 nhánh mới
=> nhánh mới sẽ chứa toàn bộ code của nhánh đang đứng

git branch -a or git branch
=> liệt kê all các branch đang có trong repo

git switch <tên nhánh>
=> chuyển qua nhánh <tên nhánh>
<<<<<<< HEAD

### git pull

=> pull code ở repo remote về local

git pull --no-ff

### git clone <url repo>

=> Dùng để clone source code của 1 repo bất kỳ

### git merge <branch>

merge <branch> vào branch hiện tại

1. TH1: merge thành công nếu ko có bất kỳ xung đột (conflict)
2. TH2 : bị xung đột => giải quyết conflict => git add => commit
   => nếu merge code mà bị conflict => có thể hủy git merge thông qua lệnh: git merge --abort

### cách xóa lịch sử commit

b1 git log
b2 chọn coppy id dưới cái lịch sử cần xóa
b3 q rồi git reset + dán id vừa coppy vào enter
