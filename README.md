
## Bài 1: Khối ALU thực hiện được các chức năng cơ bản
![image](https://github.com/fatbaccon/Lab1/assets/122776108/fe034d2a-4c0a-4ee0-9704-c8d1241ba424)


## Bài 2: Mạch Dice game thiết kế bằng phương pháp GRAFCET,
Mạch về cơ bản thực hiện được yêu cầu của bài toán, tuy nhiên vẫn còn vấn đề khi nhận diện số lần đổ xúc xắc nên phải bổ sung thêm một counter bên trong controller gây phức tạp hóa mạch
### Mạch tổng thể
![image](https://github.com/fatbaccon/Lab1/assets/122776108/018e8f8a-5463-4101-958a-6f51aef06a0a)
 

### Mạch controller
![image](https://github.com/fatbaccon/Lab1/assets/122776108/bdb9e96d-695f-4d10-92a1-76336862d7a6)
![image](https://github.com/fatbaccon/Lab1/assets/122776108/fb290adc-de27-4e1f-ad6f-9d0cfdf2ac1b)

|        |        |
|:-------|:------:|
|  S0+ = 0   |  S0 = S0. S1’.S2’.S3’   |
|  S0- = S1 + S2 + S3 |   |
|S1+ = D711.S0 + C.S3 | S1 = D711.S0 + C.S3 + S1|
|S1- = 0||
|S2+ = D2312.S0 + D7.S3 | S2 = D2312.S0 + D7.S3 + S2 |
|S2- = 0||
|S3+ = (D711’ + D2312’).S0 |S3 = ( (D711’ + D2312’).S0 + S3).S1’.S2’|
|S3- = S1 + S2||


### Mạch điều khiển để Register chỉ lưu point giá trị đầu tiên
![image](https://github.com/fatbaccon/Lab1/assets/122776108/38ffbcca-dd43-4650-878d-ce9245258289)


