# GIT & GITHUB CRASH COURSE

## WHAT IS GIT?

![Git?](/assets/what-is-git.png)

Git là một công cụ hệ thống kiểm soát phiên bản miễn phí

## GitHub và GitHub Actions?

GitHub là một công ty hỗ trợ lưu trữ mã trên đám mây, cung cấp dịch vụ tự động hóa mọi loại quy trình làm việc có liên quan đến kho lưu trữ. Dịch vụ này được gọi là GitHub Actions.

## Cách cấu hình người dùng trong git

> git config --global user.name "your-username"  
> git config --global user.email "your-email"

`user.name` và `user.email` xác định ai đã thực hiện commit. `--global` thông tin này được áp dụng cho tất cả kho lưu trữ Git trên máy, bỏ `--global` khi chỉ muốn áp tên cho một kho lưu trữ cụ thể.

## Git cơ bản

![Git-add-&-git-commit](/assets/git-basic.png)

> git init

Khởi tạo một Git Repository và đính kèm vào thư mục dự án, tất cả các thư mục con của dự án này đều được Git quản lý.

Sau khi hoàn thành một tính năng/sửa lỗi/... cần tạo một code-snapshot và commit mới thông qua 2 bước.
Thêm các file đã thay đổi vào kiểm soát.

> git add

Tạo một commit dựa trên các thay đổi.

> git commit

Xem danh sách các commit. (trong đó HEAD là con trỏ do Git quản lý điều khiển commit nào hiện đang hiển thị trong dự án)

> git log

Di chuyển giữa các lần commit hoặc giữa các branch

> git checkout <id/branch_name>

Đảo ngược (revert) những thay đổi trong commit trước đó và tạo ra một commit mới mà không xóa lịch sử commit -> lựa chọn ưu tiên vì giữ lịch sử commit sạch và các thay đổi không bị xóa

> git revert <id>

Xóa thật sự một commit (tất cả các thay đổi, stagginh area và working directory)

> git reset --hard <id> // id của commit muốn quay trở lại

Loại bỏ các file các tệp không cần thiết phải quản lý chỉ cần thêm chúng vào file `.gitignore`

> npx gitignore <ngôn ngữ hoặc công nghệ>

![Git-add-&-git-commit](/assets/branches-&-merge-branches.png)

> git branch <branch_name> // Tạo branch

> git checkout -b <branch_name> // Tạo và chuyển sang branch mới

> git branch -d <branch_name> // Xóa branch

Kết hợp cả 2 nhánh lại với nhau nhưng vẫn giữ nguyên lịch sử commit, tạo ra một merge commit thể hiện việc hợp nhất

![before-merge](/assets/before-merge.png)

![after-merge](/assets/after-merge.png)

> git merge <branch_name>

> git push --set-upstream origin <main/master> // Cấu hình kết nối nghiêm ngặt giữa remote và local

> git pull // Kéo hoặc tải mã mới từ remote về local

### Compare & pull request

Quy trình so sánh những thay đổi với nhánh đích (main/master) sau đó tạo một yêu cầu hợp nhất (merge) các thay đổi vào nhánh đích.

1. Thực hiện các thay đổi trên nhánh của bạn.
2. So sánh nhánh của bạn với nhánh đích bằng tính năng "Compare".
3. Nhấp vào nút "Create Pull Request" (Tạo Pull Request).
4. Nhập tiêu đề và mô tả cho Pull Request của bạn, giải thích mục đích của thay đổi.
5. Gửi Pull Request.
6. Chủ dự án và cộng đồng sẽ xem xét PR, có thể yêu cầu thay đổi hoặc đồng ý hợp nhất.
7. Nếu được chấp nhận, thay đổi của bạn sẽ được merge vào nhánh đích.

### fork

Quy trình sao chép toàn bộ dự án sang một tài khoản hoặc không gian làm việc mới hữu ích khi đóng góp cho dự án mà không làm ảnh hưởng đến repository chính.

1. Phát triển độc lập
2. Gửi Pull request (PR)
3. Đóng góp vào mã nguồn mở
