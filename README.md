# Ksec_tuan11-12
Máy chủ 1: DNS Server
Install bind 9: sudo apt-get install bind9



Máy chủ 2: Web Server
Trước tiên, nên tiến hành cập nhập gói phần mềm của Ubuntu lên phiên bản mới nhất với lệnh:
apt-get update
Cài đặt apache với lệnh sau:
apt-get install apache2

Thêm VirtualHost chúng ta cũng cần tạo cho nó một thư mục chứa dữ liệu cho domain cần thêm vào

mkdir /var/www/html/ksec
tạo thêm 1 file HTML với nội dung bất kì để sau có thể kiểm tra xem apache có hoạt động ko ( index.html )

Sau đó chúng ta cần copy file /etc/apache2/sites-available/000-default.conf 
ra một file mới file chứa cấu hình của domain cần thêm vào (ksec.com)

cp /etc/apache2/sites-available/000-default.conf /etc/apache2/sites-available/www.ksec.com.conf

Bây giờ hãy mở file /etc/apache2/sites-available/www.ksec.com.conf lên và sửa nội dung trong đó:


Máy chủ 3: Database Server
