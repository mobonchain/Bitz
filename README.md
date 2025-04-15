 <h1 align="center">Hi 👋, I'm Mob</h1>
<h3 align="center">Join the Cryptocurrency Market, make money from Airdrop - Retroactive with me</h3>

- <p align="left"> <img src="https://komarev.com/ghpvc/?username=mobonchain&label=Profile%20views&color=0e75b6&style=flat" alt="mobonchain" /> <a href="https://github.com/mobonchain"> <img src="https://img.shields.io/github/followers/mobonchain?label=Follow&style=social" alt="Follow" /> </a> </p>

- [![TopAME | Bullish - Cheerful](https://img.shields.io/badge/TopAME%20|%20Bullish-Cheerful-blue?logo=telegram&style=flat)](https://t.me/xTopAME)

# Hướng Dẫn Khai Thác $BITZ Mạng Eclipse
- Mục đích chủ yếu là tham gia **Mining $BITZ** tìm kiếm cơ hội **Airdrop Eclipse**, không hy vọng vào **Phần thưởng Mining**. Tổng nguồn cung **$BITZ** chỉ có **5M** 
---

## Yêu Cầu Trước Khi Bắt Đầu

Trước khi bắt đầu, bạn cần:

- ETH mạng Eclipse : **[Bridge tại đây](https://bridge.eclipse.xyz/)**
- VPS Linux hoặc Windows đã cài WSL

### Bước 1: Cập Nhật Và Cài Đặt Các Phụ Thuộc

Bước đầu tiên là cập nhật hệ thống của bạn và cài đặt các công cụ cần thiết.

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install curl nano build-essential -y
```
---

### Bước 2: Cài Đặt Các Phụ Thuộc Thêm

Tiếp theo, cài đặt các phụ thuộc bổ sung cần thiết để xây dựng phần mềm.

```bash
sudo apt install autoconf make gcc libutempter-dev libpam0g-dev libncurses5-dev -y
```

- Các gói này cung cấp các công cụ cần thiết để biên dịch và cài đặt phần mềm từ mã nguồn.

---

### Bước 3: Tải Và Cài Đặt Screen

Để chạy các tác vụ lâu dài mà không cần mở Terminal suốt, bạn sẽ sử dụng `screen`. Bỏ qua nếu VPS của bạn đã có.

```bash
curl -O https://ftp.gnu.org/gnu/screen/screen-4.9.1.tar.gz
tar -xzf screen-4.9.1.tar.gz
cd screen-4.9.1
./configure
make
sudo make install
```
---

### Bước 4: Cài Đặt Rust Và Solana CLI

Cài đặt `Rust`, công cụ lập trình cần thiết cho việc cài đặt Solana, và Solana CLI.

```bash
cd $HOME
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
- Nhấn 1 để tiếp tục và chờ quá trình cài đặt hoàn tất.
---

```bash
curl --proto '=https' --tlsv1.2 -sSfL https://solana-install.solana.workers.dev | bash
```

- Chờ quá trình cài đặt hoàn tất.

---

### Bước 5: Kiểm Tra Phiên Bản Rust, Solana

Cập nhật lại tệp cấu hình shell và kiểm tra phiên bản.

```bash
source $HOME/.bashrc
```
```bash
rustc --version
solana --version
```

- Nếu không thấy phiên bản, hãy thử khởi động lại VPS và kiểm tra lại.
- Nếu vẫn không có kết quả, sử dụng lệnh sau để thêm Solana vào `PATH`:

```bash
export PATH="$HOME/.local/share/solana/install/active_release/bin:$PATH"
```

---

### Bước 6: Tạo Khóa Mới Và Cấu Hình Solana

Tạo một cặp khóa mới và cấu hình Solana CLI để kết nối với mạng Eclipse.

```bash
solana-keygen new
```
- Nhấn Enter bỏ qua câu hỏi

```bash
solana config set --url https://bitz-000.eclipserpc.xyz/
```
---

### Bước 7: Cài Đặt Bitz

Cài đặt phần mềm `bitz` để bắt đầu khai thác.

```bash
cargo install bitz
```
- Chờ quá trình cài đặt hoàn tất.
---

### Bước 8: Lấy Địa Chỉ Ví Và Gửi ETH

Lấy`Private Key`, sẽ có dạng [158,39,56,104,.......98]

```bash
cat ~/.config/solana/id.json
```
- Sao chép `Private Key` và thêm nó vào ví Backpack trên mạng Eclipse.
- Sau đó, gửi từ 0.002 - 0.005 ETH mà bạn đã chuẩn bị từ trước vào ví này.
---

### Bước 9: Khởi Động Trình Khai Thác

Bắt đầu trình khai thác `bitz` trong một phiên `screen` để chạy nó trong nền.

```bash
screen -S bitzminer
```
- Lệnh này sẽ tạo một Screen để có thể hoạt động 24/7 mà không cần mở Temrinal
```bash
bitz collect
```
- Nếu không có lỗi gì thì quá trình khai thác sẽ diễn ra
- Sau đó thoát khỏi phiên `screen` bằng tổ hợp (Ctrl + A + D)
- Và bạn có thể quay lại bằng lệnh:
```bash
screen -r bitzminer
```
---

### Bước 10: Kiểm Tra Và Nhận Bitz

Kiểm tra tài khoản và nhận phần thưởng khai thác ( Sau khi đã thoát khỏi Screen )
- Kiểm tra :
```bash
bitz account
```
- Claim $BITZ :
```bash
bitz collect
```
---

## Nếu gặp phải bất kỳ vấn đề nào có thể hỏi thêm tại **[TopAME | Chat - Supports](https://t.me/yTopAME)**
