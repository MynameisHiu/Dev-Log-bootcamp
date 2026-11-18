# Session 05 - <Smart Contracts &amp; Digital Assets (Hợp đồng thông minh &amp; Tài sản số)>

- Student: <Nguyễn Minh Hiếu>
- GitHub: [@MynameisHiu](https://github.com/MynameisHiu)
- Submitted: 2026/11/11
- Commit: <https://github.com/MynameisHiu/Dev-Log-bootcamp/blob/main/submissions/MynameisHiu/session-05.md>
## 1\. Summary

- Khái niệm và cơ chế vận hành của **Smart Contract** thông qua ví dụ ứng dụng mua vé sự kiện.
- Phân biệt rõ ràng giữa **Native Coin, Token, Stablecoin và NFT**
- Hướng dẫn phương pháp tính **phí giao dịch Gas** và giới thiệu vai trò của các môi trường thực thi máy ảo như **EVM, SVM và WASM**.

## 2. Topic notes
### 2.1\. Smart Contract là gì và quy tắc hoạt động

* **Định nghĩa**: Smart Contract (Hợp đồng thông minh) là một chương trình tự động thực thi trên mạng lưới blockchain. Mã lệnh và dữ liệu được lưu trữ trực tiếp trên chuỗi và sẽ tự động chạy theo quy tắc định sẵn khi nhận được lời gọi hợp lệ.
* **Ví dụ ứng dụng bán vé sự kiện**:
  * **Đầu vào**: Lan gửi yêu cầu mua vé và chuyển tiền.
  * **Kiểm tra**: Hệ thống kiểm tra số lượng vé còn lại và xác nhận điều kiện thanh toán.
  * **Cập nhật**: Nếu thỏa mãn, Smart Contract ghi nhận Lan là chủ sở hữu mới của vé; nếu không đủ điều kiện, thao tác sẽ bị từ chối.
  * **Chuyển nhượng vé**: Khi Lan chuyển vé số `#042` cho Minh, chủ sở hữu được đổi từ Lan sang Minh nhưng tổng cung toàn hệ thống vẫn giữ nguyên (ví dụ 100 vé).
* **Giới hạn của Smart Contract**: Smart Contract chỉ là cỗ máy thực thi logic nhận vào input và trả ra output. Nó không thể tự thu thập hay xác thực dữ liệu thực tế ngoài đời (như nhiệt độ container, thời tiết, kết quả sự kiện) nếu không có sự hỗ trợ của **Oracle** (hệ thống cung cấp dữ liệu bên ngoài). Ngoài ra, Smart Contract không đảm nhận phần giao diện người dùng hay quy tắc vận hành ngoài hệ thống.

### 2.2\. Phân biệt Native Coin và Token

* **Native Coin (Coin gốc)**: Là tài sản nguyên bản của mạng lưới Blockchain (ví dụ: ETH trên Ethereum, SOL trên Solana, BTC trên Bitcoin). Đồng coin này bắt buộc phải được sử dụng để thanh toán phí giao dịch (Gas fee) cho mạng lưới đó.
* **Token (Tài sản phụ phụ thuộc)**: Là tài sản được quản lý bởi một chương trình/hợp đồng thông minh chạy trên blockchain (ví dụ: USDC, token điểm thưởng thành viên, NFT).
* **Tình huống giao dịch**: Nếu ví của Lan có `100 USDC` trên Ethereum nhưng không có đồng `ETH` nào, Lan không thể thực hiện giao dịch chuyển USDC. Muốn chuyển USDC, Lan bắt buộc phải nạp thêm ETH để trả phí Gas xử lý cho mạng lưới.

### 2.3\. Stablecoin & Các cơ chế giữ neo giá trị (Pegging)

* **Khái niệm**: Stablecoin là các loại token được thiết kế với mục tiêu giữ giá trị ổn định, thường bám theo một đồng tiền pháp định (ví dụ: $1 \text{ token} \approx 1 \text{ USD}$) để giải quyết vấn đề biến động giá của thị trường crypto
* **3 Cơ chế giữ neo chính**:
  1. **Dự trữ tiền mặt/tài sản (Fiat-backed)**: Bên phát hành nắm giữ tài sản thực tế trong ngân hàng để bảo chứng (ví dụ: USDC, USDT).
  2. **Thế chấp bằng Crypto (Crypto-backed)**: Khóa tài sản mã hóa làm tài sản đảm bảo và quản lý tỷ lệ thế chấp.
  3. **Điều tiết bằng thuật toán (Algorithmic)**: Tự động điều chỉnh nguồn cung và cầu để duy trì mức neo giá.

### 2.4\. NFT (Non-Fungible Token) &amp; Quyền sở hữu

* **Định nghĩa**: NFT là token có mã định danh riêng biệt để phân biệt hoàn toàn với các token khác trong cùng một bộ sưu tập hay contract (ví dụ: Vé `#042` khác với Vé `#043`).
* **Sở hữu NFT bao gồm những gì?**: Bản ghi on-chain xác nhận địa chỉ ví đang giữ token và lịch sử chuyển dịch.
* **Rào cản về bản quyền**: Việc mua và sở hữu một NFT hình ảnh/tác phẩm **không tự động đồng nghĩa với việc sở hữu bản quyền pháp lý** hay toàn quyền thương mại của tác phẩm đó. Quyền hạn phụ thuộc hoàn toàn vào điều khoản ban đầu của bên phát hành.

### 2.5\. Gas và Phí giao dịch (Transaction Fee)

* **Bản chất của Gas**: Gas đại diện cho khối lượng công việc tính toán mà hệ thống phải xử lý khi thực thi giao dịch.
* **Công thức tính phí** : $$\text{Phí giao dịch} = \text{Lượng Gas sử dụng} \times \text{Đơn giá Gas (Gas Price)}$$Ví dụ trên Ethereum L1: Phí của một giao dịch chuyển khoản cơ bản dùng hết $21.000 \text{ Gas}$ với đơn giá $20 \text{ gwei}$823: $$21.000 \times 20 \text{ gwei} = 420.000 \text{ gwei} = 0,00042 \text{ ETH} \quad (1 \text{ gwei} = 10^{-9} \text{ ETH}) \text{$$823$$}$$
**Giao dịch thất bại (Revert) có mất phí không?**:
* Nếu từ chối ký lệnh trong ví (chưa phát tán lên mạng): **Không mất phí**.
* Nếu giao dịch đã vào block nhưng bị lỗi/revert trong quá trình thực thi: **Vẫn mất phí Gas** vì hệ thống đã tiêu tốn tài nguyên máy tính để chạy mã lệnh.

### 2.6\. Môi trường thực thi Smart Contract: EVM, SVM và WASM

* **EVM (Ethereum Virtual Machine)**: Môi trường thực thi mã Smart Contract tiêu chuẩn trên Ethereum và các mạng Ethereum-compatible (sử dụng chuẩn token ERC-20 cho token thay thế).
* **SVM (Solana Virtual Machine)**: Máy ảo thực thi chương trình của Solana với chuẩn quản lý tài sản qua các Mint Account.
* **WASM (WebAssembly)**: Định dạng mã nhị phân cho phép lập trình Smart Contract bằng nhiều ngôn ngữ phổ biến (C, C++, Rust...) thay vì chỉ phụ thuộc vào Solidity.

## 3. Work completed

Không có

## 4. Evidence

Không có

## 5. Blockers

Không có

## 6. Takeaway

Không có
