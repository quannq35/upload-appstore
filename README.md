# upload-appstore

# 1. Certificate(Chứng chỉ)
  - Xác nhận ai là người phát triển ứng dụng.
  - Cho phép ký số(code signing) ứng dụng để chạy trên thiết bị thật hoặc phát hành App Store
  - Đảm bảo ứng dụng ko bị giả mạo hoặc chỉnh sửa sau khi được ký.
  * Các loại chứng chỉ phổ biến
    - Development certificate: Dùng để cài đặt và chạy ứng dụng trên thiết bị thật trong giai đoạn phát triển
    - Distribution certificate: Dùng để ký ứng dụng khi phát hành lên App Store hoặc TestFight
    - Apple Distribution: Chứng chỉ chung cho Apple Store & Ad hoc (dành cho tài khoản tổ chức)
    - IOS Development: Chứng chỉ dành cho nhà phát triển cá nhân(hỗ trợ debug trên thiết bị thật)
    - Mac Development/ Mac App Distribution: Chứng chỉ dành cho MacOS App
    - Push Notification Certificate: Chứng chỉ gửi thông báo đây (APNs)

# 2. Identifier(Danh tính ứng dụng)
  - Giúp định danh ứng dụng và các dịch vụ liên quan
  - Được sử dụng để liên kết với Certificates, Provisioning Profiles, và Capabilities (Push Notifications, iCloud, In-App Purchases...)
  * Các loại Identifier quan trọng
    - App IDs(App Identifier): Dùng để định danh ứng dụng, có dạng com.company.appname
    - Bundle ID: Một định danh duy nhất của ứng dụng trong XCode(Phải khớp với App ID)
    - App Group: Cho phép chia sẻ dữ liệu giữa các ứng dụng hoặc extension
    - iCloud Containers: Dùng để lưu trữ dữ liệu trên iCloud
    - Apple Pay Merchant ID: Dùng để thiết lập Apple Pay cho ứng dụng
    - Push Notification(APNs): Định danh ứng dụng để sử dụng dịch vụ thông báo đẩy.
   
# 3. Device
  - Devices trong Apple Developer dùng để đăng ký thiết bị thật(Iphone, Ipad, Mac, Apple Watch) để thử nghiệm ứng dụng 
  - Mỗi tài khoản Apple Developer có thể đăng ký tối đa 100 thiết bị mỗi loại(iPhone, iPad,..)
  - Thiết bị được đăng ký bằng UDID
  - Khi thêm vào danh sách Devices, thiết bị có thể được sử dụng trong Provisioning Profile để cài đặt app thử nghiệm
  - Mỗi năm có thể reset danh sách thiết bị

# 4. Profiles(Cấu hình cấp phép)
  - Xác định ứng dụng có thể chạy trên thiết bị nào
  - Liên kết Certificate với Apple ID để đảm bảo app chỉ chạy với chứng chỉ hợp lệ
  - Kích hoạt các quyền đặc biệt như Push Notification, iCloud, AppGroup..
  * Các loại Provisioning Profile
    - Development Profile: Dùng để chạy app trên thiết bị thật trong quá trình phát triển
    - Ad hoc Profile: Dùng để phân phối app ngoài AppStore cho một nhóm thiết bị nhất định
    - App Store profile: Dùng để phát hành ứng dụng chính thức trên AppStore
    - In-House: Dành cho công ty có tài khoản Enterprise để phát hành nội bộ.
  * Lưu ý:
    - Development Profle yêu cầu IOS Deployment Certificate và danh sách thiết bị đã đăng ký.
    - App Store Profile chứng chỉ yêu cầu Apple Distribution Certificate(không cần danh sách thiết bị)

# 5. Keys(Khoá API & Bảo mật)
  - Keys trong Apple Developer là các khoá bảo mật được dùng để tích hợp API của Apple
  
