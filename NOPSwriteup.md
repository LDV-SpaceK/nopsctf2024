 

Trong server discord có đoạn ascii 
49 66 20 61 6E 79 6F 6E 65 20 72 65 61 64 73 20 69 74 2C 20 49 20 61 6D 20 4A 6F 6A 6F 2E 20 49 20 68 61 76 65 20 62 65 65 6E 20 63 61 70 74 75 72 65 64 20 62 79 20 61 20 67 72 6F 75 70 20 63 61 6C 6C 65 64 20 4A 33 4A 75 4A 34 2E 20 50 6C 65 61 73 65 20 63 6F 6D 65 20 61 6E 64 20 73 61 76 65 20 6D 65 21 0A 4E 30 50 53 7B 4A 30 4A 30 5F 31 73 5F 6D 31 53 35 31 6E 47 21 7D
Mình sử dụng CyberChef để decode
 
N0PS{J0J0_1s_m1S51nG!}

OSINT:
 

 
Mình sử dụng google lens và tìm được nơi bức ảnh này được đăng tải
  

Tiêu đề là praca do comercio

NOPS{praca-do-comercio}

 

Mình có một đoạn cipher text
Đây là một đoạn mã morse
....- ...-- -.... ..-. -.... . -.... --... --... ..--- -.... .---- --... ....- --... .- ..--- .---- ..--- ----- ..... ....- -.... ---.. -.... ..... ..--- ----- -.... -.... -.... -.-. -.... .---- -.... --... ..--- ----- -.... ----. --... ...-- ...-- .- ..--- ----- ....- . ...-- ----- ..... ----- ..... ...-- --... -... ....- -.. ...-- ----- --... ..--- ..... ...-- ...-- ...-- ..... ..-. ....- ....- ...-- ...-- -.... ...-- ...-- ----- -.... ....- ...-- ...-- ..... ..--- ..... ..-. ..... ----- --... ..--- ...-- ----- --... -..

 

N0PS{M0rS3_D3c0d3R_Pr0}

 

Đầu tiên mình kiểm tra metadata của file main

 

Đây là file elf nên mình mở bằng ida để đọc

 

Trong hàm main, các thành phần của mảng s được khai báo từ 0 đến 22 là những mã ascii tương ứng nên mình đã decode bằng tay

N0PS{cH4r_1s_8bits_1Nt}
 

Mình sử dụng cipher identifier để xác định đây là loại cipher gì
 
Kết quả cho thấy đây có thể là Railfence Cipher
Mình sử dụng dcode.fr để decode với depth là 3

 

NOPS{SOMETIMESAFLAGISBETTERTHANACOOKIE}

 

Theo đề thì có thể bài này sẽ liên quan đến cookie nên mình đã thử xem cookie của web này
Giao diện web 
 
Instruction có vẻ đã hướng dẫn một số thao tác đổi cookie tuy nhiên mình vẫn phải thử
Thử input username: admin
 

Decode cookie
 

Có vẻ key isAdmin đang có value là 0 nên mình thử đổi thành 1 và encode, đổi cookie
Sau khi đổi cookie và refresh lại thì
 

N0PS{y0u_Kn0W_H0w_t0_c00K_n0W}


