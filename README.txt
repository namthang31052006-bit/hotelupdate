<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="LumiStay - Đặt phòng khách sạn nhanh chóng, dễ dàng và đáng tin cậy.">
  <title>LumiStay | Đặt phòng khách sạn</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Manrope:wght@600;700;800&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header class="site-header">
    <a class="brand" href="#" aria-label="LumiStay - Trang chủ">
      <span class="brand-mark">L</span>
      <span>LumiStay</span>
    </a>
    <nav class="desktop-nav" aria-label="Điều hướng chính">
      <a class="active" href="#rooms">Lưu trú</a>
      <a href="#benefits">Ưu đãi</a>
      <a href="#about">Về chúng tôi</a>
    </nav>
    <div class="header-actions">
      <button class="icon-button" id="savedButton" aria-label="Phòng đã lưu">
        <svg viewBox="0 0 24 24" aria-hidden="true"><path d="M20.8 4.6a5.5 5.5 0 0 0-7.8 0L12 5.7l-1.1-1.1a5.5 5.5 0 0 0-7.8 7.8l1.1 1.1L12 21l7.8-7.5 1.1-1.1a5.5 5.5 0 0 0-.1-7.8Z"/></svg>
        <span class="saved-count" id="savedCount">0</span>
      </button>
      <button class="login-button" id="loginButton">Đăng nhập</button>
    </div>
  </header>

  <main>
    <section class="hero">
      <div class="hero-orb orb-one"></div>
      <div class="hero-orb orb-two"></div>
      <div class="hero-copy">
        <p class="eyebrow">Kỳ nghỉ hoàn hảo bắt đầu từ đây</p>
        <h1>Tìm một nơi khiến bạn muốn <em>ở lại lâu hơn.</em></h1>
        <p>Khám phá những khách sạn được chọn lọc kỹ, với giá tốt và trải nghiệm đặt phòng thật nhẹ nhàng.</p>
      </div>

      <form class="search-panel" id="searchForm">
        <label class="search-field destination-field">
          <span class="field-icon">
            <svg viewBox="0 0 24 24"><path d="M20 10c0 5-8 11-8 11S4 15 4 10a8 8 0 1 1 16 0Z"/><circle cx="12" cy="10" r="2.5"/></svg>
          </span>
          <span>
            <small>Điểm đến</small>
            <input id="destination" type="text" placeholder="Bạn muốn đi đâu?" autocomplete="off">
          </span>
        </label>
        <label class="search-field">
          <span class="field-icon">
            <svg viewBox="0 0 24 24"><rect x="3" y="5" width="18" height="16" rx="2"/><path d="M16 3v4M8 3v4M3 10h18"/></svg>
          </span>
          <span>
            <small>Nhận phòng</small>
            <input id="checkin" type="date">
          </span>
        </label>
        <label class="search-field">
          <span class="field-icon">
            <svg viewBox="0 0 24 24"><rect x="3" y="5" width="18" height="16" rx="2"/><path d="M16 3v4M8 3v4M3 10h18"/></svg>
          </span>
          <span>
            <small>Trả phòng</small>
            <input id="checkout" type="date">
          </span>
        </label>
        <label class="search-field">
          <span class="field-icon">
            <svg viewBox="0 0 24 24"><path d="M16 21v-2a4 4 0 0 0-4-4H6a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M22 21v-2a4 4 0 0 0-3-3.9M16 3.1a4 4 0 0 1 0 7.8"/></svg>
          </span>
          <span>
            <small>Khách</small>
            <select id="guests">
              <option value="1">1 khách</option>
              <option value="2" selected>2 khách</option>
              <option value="3">3 khách</option>
              <option value="4">4 khách</option>
              <option value="5">5+ khách</option>
            </select>
          </span>
        </label>
        <button class="search-button" type="submit">
          <svg viewBox="0 0 24 24"><circle cx="11" cy="11" r="7"/><path d="m20 20-4-4"/></svg>
          <span>Tìm phòng</span>
        </button>
      </form>
    </section>

    <section class="content-section" id="rooms">
      <div class="section-heading">
        <div>
          <p class="eyebrow">Được yêu thích nhất</p>
          <h2>Những nơi đáng để dừng chân</h2>
        </div>
        <p id="resultText">6 chỗ nghỉ phù hợp</p>
      </div>

      <div class="filters" aria-label="Bộ lọc khách sạn">
        <button class="filter active" data-filter="all">Tất cả</button>
        <button class="filter" data-filter="beach">Gần biển</button>
        <button class="filter" data-filter="city">Trung tâm</button>
        <button class="filter" data-filter="romantic">Lãng mạn</button>
      </div>

      <div class="hotel-grid" id="hotelGrid">
        <figure class="hotel-card" data-category="beach" data-location="Đà Nẵng">
          <div class="card-image-wrap">
            <img src="assets/danang-suite.png" alt="Phòng Ocean Pearl Resort tại Đà Nẵng">
            <span class="card-badge">Bán chạy</span>
            <button class="save-button" aria-label="Lưu Ocean Pearl Resort">
              <svg viewBox="0 0 24 24"><path d="M20.8 4.6a5.5 5.5 0 0 0-7.8 0L12 5.7l-1.1-1.1a5.5 5.5 0 0 0-7.8 7.8l1.1 1.1L12 21l7.8-7.5 1.1-1.1a5.5 5.5 0 0 0-.1-7.8Z"/></svg>
            </button>
          </div>
          <figcaption class="card-body">
            <div class="location">Sơn Trà, Đà Nẵng <span class="rating">4.9</span></div>
            <h3>Ocean Pearl Resort</h3>
            <p class="amenities">Hướng biển · Hồ bơi · Bữa sáng</p>
            <div class="card-footer">
              <p><strong>2.450.000đ</strong><span>/ đêm</span></p>
              <button class="book-button" data-hotel="Ocean Pearl Resort" data-price="2450000">Đặt ngay</button>
            </div>
          </figcaption>
        </figure>

        <figure class="hotel-card" data-category="city" data-location="Hà Nội">
          <div class="card-image-wrap">
            <img src="assets/hanoi-room.png" alt="Phòng khách sạn The Sage House tại Hà Nội">
            <span class="card-badge muted">Giảm 18%</span>
            <button class="save-button" aria-label="Lưu The Sage House">
              <svg viewBox="0 0 24 24"><path d="M20.8 4.6a5.5 5.5 0 0 0-7.8 0L12 5.7l-1.1-1.1a5.5 5.5 0 0 0-7.8 7.8l1.1 1.1L12 21l7.8-7.5 1.1-1.1a5.5 5.5 0 0 0-.1-7.8Z"/></svg>
            </button>
          </div>
          <figcaption class="card-body">
            <div class="location">Hoàn Kiếm, Hà Nội <span class="rating">4.8</span></div>
            <h3>The Sage House</h3>
            <p class="amenities">Phố cổ · Nhà hàng · Đưa đón</p>
            <div class="card-footer">
              <p><strong>1.680.000đ</strong><span>/ đêm</span></p>
              <button class="book-button" data-hotel="The Sage House" data-price="1680000">Đặt ngay</button>
            </div>
          </figcaption>
        </figure>

        <figure class="hotel-card" data-category="romantic" data-location="Hội An">
          <div class="card-image-wrap">
            <img src="assets/hoian-suite.png" alt="Phòng Lantern Heritage tại Hội An">
            <span class="card-badge">Đặc biệt</span>
            <button class="save-button" aria-label="Lưu Lantern Heritage">
              <svg viewBox="0 0 24 24"><path d="M20.8 4.6a5.5 5.5 0 0 0-7.8 0L12 5.7l-1.1-1.1a5.5 5.5 0 0 0-7.8 7.8l1.1 1.1L12 21l7.8-7.5 1.1-1.1a5.5 5.5 0 0 0-.1-7.8Z"/></svg>
            </button>
          </div>
          <figcaption class="card-body">
            <div class="location">Minh An, Hội An <span class="rating">4.9</span></div>
            <h3>Lantern Heritage</h3>
            <p class="amenities">Phố cổ · Ban công · Spa</p>
            <div class="card-footer">
              <p><strong>1.950.000đ</strong><span>/ đêm</span></p>
              <button class="book-button" data-hotel="Lantern Heritage" data-price="1950000">Đặt ngay</button>
            </div>
          </figcaption>
        </figure>

        <figure class="hotel-card" data-category="beach" data-location="Nha Trang">
          <div class="card-image-wrap alternate-one">
            <img src="assets/danang-suite.png" alt="Phòng Azure Bay Hotel tại Nha Trang">
            <button class="save-button" aria-label="Lưu Azure Bay Hotel">
              <svg viewBox="0 0 24 24"><path d="M20.8 4.6a5.5 5.5 0 0 0-7.8 0L12 5.7l-1.1-1.1a5.5 5.5 0 0 0-7.8 7.8l1.1 1.1L12 21l7.8-7.5 1.1-1.1a5.5 5.5 0 0 0-.1-7.8Z"/></svg>
            </button>
          </div>
          <figcaption class="card-body">
            <div class="location">Lộc Thọ, Nha Trang <span class="rating">4.7</span></div>
            <h3>Azure Bay Hotel</h3>
            <p class="amenities">Bãi biển · Rooftop · Phòng gym</p>
            <div class="card-footer">
              <p><strong>2.120.000đ</strong><span>/ đêm</span></p>
              <button class="book-button" data-hotel="Azure Bay Hotel" data-price="2120000">Đặt ngay</button>
            </div>
          </figcaption>
        </figure>

        <figure class="hotel-card" data-category="city" data-location="Hồ Chí Minh">
          <div class="card-image-wrap alternate-two">
            <img src="assets/hanoi-room.png" alt="Phòng Sora Central tại Thành phố Hồ Chí Minh">
            <button class="save-button" aria-label="Lưu Sora Central">
              <svg viewBox="0 0 24 24"><path d="M20.8 4.6a5.5 5.5 0 0 0-7.8 0L12 5.7l-1.1-1.1a5.5 5.5 0 0 0-7.8 7.8l1.1 1.1L12 21l7.8-7.5 1.1-1.1a5.5 5.5 0 0 0-.1-7.8Z"/></svg>
            </button>
          </div>
          <figcaption class="card-body">
            <div class="location">Quận 1, TP. HCM <span class="rating">4.8</span></div>
            <h3>Sora Central</h3>
            <p class="amenities">Trung tâm · Hồ bơi · Co-working</p>
            <div class="card-footer">
              <p><strong>2.280.000đ</strong><span>/ đêm</span></p>
              <button class="book-button" data-hotel="Sora Central" data-price="2280000">Đặt ngay</button>
            </div>
          </figcaption>
        </figure>

        <figure class="hotel-card" data-category="romantic" data-location="Đà Lạt">
          <div class="card-image-wrap alternate-three">
            <img src="assets/hoian-suite.png" alt="Phòng Mây Villa tại Đà Lạt">
            <span class="card-badge muted">Mới</span>
            <button class="save-button" aria-label="Lưu Mây Villa">
              <svg viewBox="0 0 24 24"><path d="M20.8 4.6a5.5 5.5 0 0 0-7.8 0L12 5.7l-1.1-1.1a5.5 5.5 0 0 0-7.8 7.8l1.1 1.1L12 21l7.8-7.5 1.1-1.1a5.5 5.5 0 0 0-.1-7.8Z"/></svg>
            </button>
          </div>
          <figcaption class="card-body">
            <div class="location">Phường 3, Đà Lạt <span class="rating">4.9</span></div>
            <h3>Mây Villa</h3>
            <p class="amenities">Săn mây · Bồn tắm · Lò sưởi</p>
            <div class="card-footer">
              <p><strong>1.890.000đ</strong><span>/ đêm</span></p>
              <button class="book-button" data-hotel="Mây Villa" data-price="1890000">Đặt ngay</button>
            </div>
          </figcaption>
        </figure>
      </div>
      <div class="empty-state" id="emptyState">
        <h3>Chưa tìm thấy chỗ nghỉ phù hợp</h3>
        <p>Hãy thử một điểm đến hoặc bộ lọc khác nhé.</p>
      </div>
    </section>

    <section class="benefits" id="benefits">
      <div class="benefit">
        <span>01</span>
        <div><h3>Giá minh bạch</h3><p>Không phí ẩn, không bất ngờ khi thanh toán.</p></div>
      </div>
      <div class="benefit">
        <span>02</span>
        <div><h3>Hỗ trợ 24/7</h3><p>Luôn có người đồng hành trong suốt chuyến đi.</p></div>
      </div>
      <div class="benefit">
        <span>03</span>
        <div><h3>Đặt phòng linh hoạt</h3><p>Nhiều lựa chọn hoàn hủy miễn phí, dễ thay đổi.</p></div>
      </div>
    </section>
  </main>

  <footer id="about">
    <a class="brand footer-brand" href="#"><span class="brand-mark">L</span><span>LumiStay</span></a>
    <p>Nơi những hành trình đáng nhớ bắt đầu.</p>
    <p>© 2026 LumiStay. Bài tập website responsive.</p>
  </footer>

  <dialog id="bookingModal">
    <form method="dialog" class="modal-card" id="bookingForm">
      <button class="modal-close" id="modalClose" type="button" aria-label="Đóng">×</button>
      <p class="eyebrow">Xác nhận kỳ nghỉ</p>
      <h2 id="modalHotel">Tên khách sạn</h2>
      <p class="modal-subtitle">Chỉ còn một bước để giữ phòng cho bạn.</p>
      <div class="booking-summary">
        <div><span>Thời gian</span><strong id="modalDates">1 đêm</strong></div>
        <div><span>Số khách</span><strong id="modalGuests">2 khách</strong></div>
        <div><span>Tổng cộng</span><strong id="modalTotal">0đ</strong></div>
      </div>
      <label>Họ và tên<input id="guestName" type="text" placeholder="Nguyễn Văn A" required></label>
      <label>Số điện thoại<input type="tel" placeholder="090 123 4567" required></label>
      <button class="confirm-button" value="default" type="submit">Xác nhận đặt phòng</button>
    </form>
  </dialog>

  <div class="toast" id="toast" role="status" aria-live="polite">Đã cập nhật</div>
  <script src="script.js"></script>
</body>
</html>
