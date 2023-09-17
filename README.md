# Hướng dẫn cài đăng docker desktop

Bạn đang tìm bài viết hướng dẫn chi tiết quy trình cài đặt Docker tool? Vậy bạn đã đến đúng chỗ.

Ở đây, chúng ta sẽ thảo luận chi tiết về khái niệm Cài đặt Docker trên Windows. Nhưng trước khi tìm hiểu về quá trình cài đặt, trước tiên chúng ta hãy hiểu Docker là gì.

Docker là một nền tảng phần mềm ảo hóa cấp hệ điều hành giúp người dùng xây dựng và quản lý các ứng dụng trong môi trường Docker với tất cả các phần phụ thuộc vào thư viện của nó.

![image](https://github.com/thangdtph27626/installDockerDesktop/assets/109157942/d0c5791d-6086-4eca-bfaf-4292c0cac2ed)

## 1: Một số lợi ích hàng đầu khi làm việc với Docker trên Windows 

- Cho phép giao diện người dùng tích hợp để xem và giám sát các vùng chứa Docker
- Nhanh chóng khởi động Docker trong vòng mười giây
- Không gian làm việc Linux dễ sử dụng
- Phân bổ không gian tài nguyên và bộ nhớ cần thiết
- Bao gồm đồng bộ hóa CA
- Hỗ trợ cài đặt proxy HTTP

## 2: Danh sách các thành phần bạn nên có để tạo và chạy các vùng chứa Docker:

- Docker Engine: Nó chạy trên máy chủ để xây dựng và chạy các container 
- Docker Daemon: Nó quản lý các container Docker
- Docker Client: Nó chạy lệnh. Lệnh được dịch bằng API REST và được gửi tới Docker Daemon 
- Docker Compose : Nó chạy hai container trong một dịch vụ

## 3: Yêu cầu
- Windows 10 với 64bit 
- Windows 11 với hệ điều hành 64 bit 
- Phiên bản Pro 2004 trở lên 
- Phiên bản 1909 trở lên dành cho phiên bản Enterprise hoặc Education

## 4: Thông số kỹ thuật

- Khi chọn windows 10 hoặc 11 64 bit thì phải có độ dịch cao hơn
- RAM 4GB hoặc phiên bản cao hơn nhưng không ít hơn
- Cài đặt BIOS phải bật hỗ trợ ảo hóa phần cứng. 
- Tính năng Hyper V, tính năng WSL 2 và tính năng Container phải được bật trong windows.  
- Windows được Microsoft hỗ trợ cần được cập nhật, nếu máy tính có phiên bản windows cũ hơn.

## 5: Cài đặt Docker từng bước trên Windows

- Truy cập trang web [https://desktop.docker.com/win/stable/Docker Desktop Installer.exe](https://desktop.docker.com/win/stable/Docker Desktop Installer.exe) và tải xuống tệp docker.

> Lưu ý: Bộ xử lý 64 bit và RAM hệ thống 4GB là điều kiện tiên quyết về phần cứng cần có để chạy thành công Docker trên Windows 10.

2. Sau đó, nhấp đúp vào Docker Desktop Installer.exe để chạy trình cài đặt.

> Lưu ý: Giả sử trình cài đặt (Docker Desktop Installer.exe) chưa được tải xuống; bạn có thể lấy nó từ Docker Hub và chạy nó bất cứ khi nào cần.

3. Sau khi bạn bắt đầu quá trình cài đặt, hãy luôn bật Tính năng Windows Hyper-V trên trang Cấu hình.

4. Sau đó, làm theo quy trình cài đặt để cho phép trình cài đặt và đợi cho đến khi quá trình hoàn tất.

5. Sau khi hoàn tất quá trình cài đặt, nhấn Close và khởi động lại. 

## 6: Khởi động công cụ máy tính để bàn Docker



Sau khi cài đặt xong, ở góc phải bên dưới sẽ hiện lên icon của Docker Desktop và trạng thái của nó. Có 3 trạng thái: Stopping, Restarting và Running.

![image](https://github.com/thangdtph27626/installDockerDesktop/assets/109157942/1a4dc973-db84-42e8-8243-fc1f56d45158)

Click chuột phải vào Docker icon sẽ hiện ra các option. Ở đây tôi chọn Dashboard

![image](https://github.com/thangdtph27626/installDockerDesktop/assets/109157942/c0ffc019-b058-4e76-ad7f-0ba97df123b6)

![image](https://github.com/thangdtph27626/installDockerDesktop/assets/109157942/08fe3fd4-81d6-4450-8024-0e0807fb995b)


## 7: cài đặt cấu hình

1: Click chuột phải docker icon và chọn Settings
2: Vào giao diện chính như hình trên và chọn icon bánh răng

![image](https://github.com/thangdtph27626/installDockerDesktop/assets/109157942/dca204f7-4f13-4a2a-bbe5-a40d9972054a)

Ở đây xảy ra 2 trường hợp:

- Bạn chọn dùng Windows Container làm backend engine
- Bạn chọn dùng WSL 2 làm backend engine

Cả 2 cách có ưu/nhược bù trừ. Như bạn dùng Windows Container thì setup đơn giản vì Windows 10 hỗ trợ hết rồi, nhưng khổ nỗi chạy không mượt bằng WSL 2. Còn nếu bạn dùng cách 2 thì chạy ngon hơn cách 1 nhưng setup thì rườm rà.

Tôi sẽ hướng dẫn các bạn cách 1 trước: sử dụng Windows Container

Bạn vào Apps&Features, một mục trong Settings của Windows
![image](https://github.com/thangdtph27626/installDockerDesktop/assets/109157942/e41ba22e-2680-4c31-97cd-b13848f1a8e5)


Vào phần Programes and Features góc phải bên trên
![image](https://github.com/thangdtph27626/installDockerDesktop/assets/109157942/88ecae4e-4489-404d-80cf-129155173ca3)


Vào phần Turn Windows features on or off
![image](https://github.com/thangdtph27626/installDockerDesktop/assets/109157942/ef848820-0de8-4367-bd96-e04391937c36)


Bạn chọn 2 ô Containers và Hyper-V ở hình dưới
![image](https://github.com/thangdtph27626/installDockerDesktop/assets/109157942/bcea3885-8b35-487c-8f5f-3ec412ac0e1d)


Restart máy

Nếu bạn dùng cách này thì trong phần Settings của Docker Desktop sẽ có phần thiết lập tài nguyên máy của mỗi Docker Container và thiết lập đường dẫn để mount thư mục trong Container với bên ngoài.
![image](https://github.com/thangdtph27626/installDockerDesktop/assets/109157942/bbcf1724-d49a-491b-a3e0-ce60750e895a)

Sau khi điều chỉnh ok thì bạn ấn vào Apply & Restart để lưu thay đổi.
![image](https://github.com/thangdtph27626/installDockerDesktop/assets/109157942/7550a941-3b6d-4ebc-9fe7-25b29abb95b4)

Ok thế là xong cách 1, chúng ta chuyển sang cách 2 nhé.

Cài đặt WSL 2
Bật tính năng Windows Subsystem for Linux bằng CMD của Windows, type dòng này:

```
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

Kiểm tra cấu hình máy xem có đủ điều kiện không

For x64 systems: Version 1903 or higher, with Build 18362 or higher.
For ARM64 systems: Version 2004 or higher, with Build 19041 or higher.
Bật tính năng Virtual Machine (máy ảo) lên

```
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

Tải về gói update Linux kernel qua link https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi

Để WSL 2 làm mặc định khi cài đặt Linux distribution

```
wsl --set-default-version 2
```

Về cơ bản làm xong bước trên là ok rồi nhưng nếu bạn muốn dùng Ubuntu hay Kali hay Debian thì vào Microsoft Store để tải các Linux distribution về nhé (https://aka.ms/wslstore)

Sau đó Linux sẽ đòi hỏi bạn tạo Username, Password các kiểu nhưng chỉ một lần thôi

Nếu bạn dùng WSL 2 làm backend thì không cần lo việc thay đổi Settings của Docker Desktop như tài nguyên máy cần sử dụng hay mount đường dẫn trong/ngoài container bởi mọi thứ đã được config sẵn rồi.


