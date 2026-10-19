# Session 01 - BlockChain Fundamental

- Student: Nguyễn Minh Hiếu
- GitHub: https://github.com/MynameisHiu
- Submitted: 20/10/2026
- Commit: 

## 1. Summary
- Tổng quát về công nghệ Blockchain.
- Lý do ra đời của Blockchain: xuất phát từ hạn chế của các hệ thống tài chính tập trung
truyền thống. 
- Định nghĩa kỹ thuật cốt lõi của cấu trúc khối (Block) và chuỗi liên kết (Chain),
- Các đặc tính nền tảng như: tính phi tập trung, minh bạch, bảo mật và bất biến.
- Phân loại các mô hình Blockchain (Public, Private, Hybrid, Consortium) 
- 4 thế hệ phát triển từ Bitcoin, Ethereum cho đến các nền tảng tiên tiến hiện đại 
- Phân tích các ứng dụng thực tế trong tài chính phi tập trung (DeFi) cũng như nhiều ngành nghề khác.

## 2. Topic notes

1. Vì sao công nghệ Blockchain lại ra đời?
- Hạn chế của mô hình tập trung truyền thống: Khi thực hiện các giao dịch tài chính qua ngân hàng, người dùng bắt buộc phải đặt niềm tin tuyệt đối vào bên trung gian. Ngân hàng là bên nắm quyền xác nhận giao dịch, giữ tiền và có quyền khóa tài khoản của người dùng.
- Thanh toán quốc tế gặp rào cản: Việc chuyển tiền xuyên quốc gia thông qua ngân hàng truyền thống thường diễn ra chậm chạp và tốn kém phí giao dịch cao. Ví Blockchain ra đời giúp tối ưu hóa quá trình này, tiết kiệm đáng kể thời gian và chi phí.
- Sự khởi đầu của thị trường Crypto: Năm 2008, Satoshi Nakamoto đã xuất bản bản whitepaper về Bitcoin, và chính thức ra mắt mạng lưới Bitcoin vào năm 2009. Sự kiện này đánh dấu sự ra đời của công nghệ Blockchain và đồng tiền mã hóa đầu tiên ($BTC), đặt nền móng cho toàn bộ thị trường tiền mã hóa.
2. Blockchain là gì và cơ chế hoạt động cốt lõi?
- Định nghĩa: Blockchain là một cơ sở dữ liệu phân cấp dùng để lưu trữ thông tin dưới dạng các khối.
- Block (Khối): Chứa các dữ liệu thông tin giao dịch.
- Chain (Chuỗi): Các khối được liên kết chặt chẽ với nhau thông qua mã hash.
- Sổ cái điện tử phân tán: Khác với cơ sở dữ liệu tập trung, thông tin trên Blockchain được lưu trữ phân tán đồng thời trên nhiều máy tính (gọi là các node) trong toàn bộ mạng lưới.
3. Tại sao dữ liệu trên Blockchain lại khó bị thay đổi (Tính bất biến)?
- Liên kết mã hóa dạng chuỗi: Mỗi khối chứa mã hash của chính nó và mã hash của khối liền trước. Khi dữ liệu trong một khối bị can thiệp, mã hash của khối đó sẽ thay đổi ngay lập tức, làm phá vỡ sự liên kết với khối tiếp theo.
- Xác thực phi tập trung: Nhờ mô hình sổ cái phân tán được lưu trữ ở nhiều node, việc một bên cố tình sửa đổi dữ liệu trên một máy tính lẻ tỏi sẽ bị toàn bộ mạng lưới từ chối. Do đó, hệ thống đạt được tính minh bạch, bảo mật, phi tập trung và bất biến.
4. Phân loại các mô hình Blockchain
Blockchain được chia thành các nhóm chính dựa trên quyền truy cập và kiểm soát:
- Public Blockchain (Không cần cấp phép - Permissionless): Không có cơ quan trung ương kiểm soát, bất kỳ ai cũng có thể tham gia mạng lưới (ví dụ: Bitcoin, Ethereum).
- Private Blockchain (Cần cấp phép - Permissioned): Được kiểm soát hoàn toàn bởi một tổ chức/cơ quan duy nhất.
- Consortium Blockchain (Cần cấp phép - Permissioned): Được quản lý và kiểm soát bởi một nhóm các tổ chức.
- Hybrid Blockchain: Mô hình kết hợp được kiểm soát bởi một tổ chức nhưng tích hợp một số quy trình không cần cấp phép.
5. Lịch sử và 4 thế hệ Blockchain
-Thế hệ 1 (Blockchain 1.0 - Bitcoin): Tập trung vào chức năng tiền mã hóa với sổ cái phi tập trung nhưng chưa hỗ trợ ứng dụng phi tập trung (dApp).
Thế hệ 2: (Ethereum) phát triển hơn có hỗ trợ smart
contract nhưng còn hạn chế khi mở rộng 
Thế hệ 3: (Cardano,Solana,Polkadot,...) kết hợp cả 2 tính
năng của hai thế hệ trước đó và đáp ứng được sự phát
triển nhanh nhu cầu của người dùng ( highest security,
scalability, …)
Thế hệ 4: (Midnight,Secret Network,Hedera,...) Tập trung
vào doanh nghiệp, quyền riêng tư, ứng dụng thực tiễn
6. Tài chính phi tập trung (DeFi) và ứng dụng thực tiễn
- CeFi vs DeFi: Tài chính truyền thống/tập trung (CeFi) đòi hỏi trung gian quản lý (ngân hàng, tổ chức tài chính). Trong khi đó, Tài chính phi tập trung (DeFi) cho phép người dùng giao dịch trực tiếp thông qua Smart Contract và các giao thức Blockchain.
Các lĩnh vực ứng dụng tiêu biểu:
- Tài chính & Thanh toán: Chuyển tiền quốc tế, P2P lending, microfinance.
- Quản lý hồ sơ & Bất động sản: Lưu trữ quyền sở hữu, chứng nhận tài sản, định danh số.
- Chuỗi cung ứng & Y tế & Giáo dục: Truy xuất nguồn gốc, bảo mật hồ sơ sức khỏe và bằng cấp.
- Gaming & Bản quyền số: Đảm bảo quyền sở hữu vật phẩm số và bản quyền trí tuệ.

## 3. Work completed
- Liệt kê và phân tích cấu trúc toán học/mã hóa của khối dữ liệu (Block), chuỗi liên kết (Chain) và cơ chế mã hash
- Bảng phân loại 4 nhóm mô hình Blockchain (Public, Private, Hybrid, Consortium).
- Đánh giá ma trận tiến hóa từ thế hệ Blockchain 1.0 đến 4.0 dựa trên các tiêu chí: Tiền tệ, Smart Contract, dApp, Khả năng mở rộng và Quyền riêng tư doanh nghiệp

## 4. Evidence
https://docs.google.com/document/d/1Rs-sHO9vW49wzqVWb9xoRc_snfbhZ1IZ/edit?usp=sharing&ouid=101913683076147613127&rtpof=true&sd=true


## 5. Blockers
- Tổng hợp thông tin sau khi học. 
- Khả năng dùng git. 
## 6. Takeaway