<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>83 Sóc Trăng - Toàn Lộc Khang Phú Quân</title>
    <style>
      table {
    width: 100%;
    border-collapse: collapse; /* Đây là lệnh quan trọng để hiện đường kẻ bảng */
    margin: 20px 0;
    background-color: #ffffff;
}

table th, table td {
    border: 2px solid #d32f2f; /* Đường kẻ bảng màu đỏ đô */
    padding: 12px;
    text-align: left;
}

table th {
    background-color: #d32f2f; /* Màu nền tiêu đề bảng */
    color: white;
}

table tr:nth-child(even) {
    background-color: #fff3e0; /* Màu nền dòng chẵn cho dễ nhìn */
}
        :root { 
            --primary: #d32f2f; /* Màu Đỏ Đô chuyên nghiệp */
            --text: #4e342e;    /* Màu Nâu đậm dễ đọc */
            --bg: #ffffff;      
            --body-bg: #fff8e1; /* Nền kem nhạt dịu mắt */
            --accent: #ff9800;  /* Màu nhấn Vàng Cam */
        }

        body { font-family: 'Roboto', Arial, sans-serif; line-height: 1.8; margin: 0; color: var(--text); background-color: var(--body-bg); }
        
        /* Menu */
        nav { background: white; border-bottom: 2px solid var(--accent); position: sticky; top: 0; z-index: 1000; padding: 0 5%; display: flex; align-items: center; justify-content: space-between; height: 64px; }
        .logo { font-size: 22px; font-weight: bold; color: var(--primary); }
        .nav-links { display: flex; list-style: none; gap: 20px; overflow-x: auto; align-items: center; margin: 0; padding: 0; }
        .nav-links a { text-decoration: none; color: #5f6368; font-size: 14px; font-weight: 500; padding: 22px 5px; border-bottom: 3px solid transparent; cursor: pointer; white-space: nowrap; }
        .nav-links a:hover { color: var(--primary); }
        .nav-links a.active { color: var(--primary); border-bottom-color: var(--primary); }

        /* Banner */
        .banner { background: #3e2723; color: #ffd54f; padding: 100px 20px; text-align: center; border-bottom: 5px solid var(--accent); }
        .banner h1 { margin: 0; font-size: 3.5rem; letter-spacing: 2px; text-shadow: 2px 2px 4px rgba(0,0,0,0.3); }

        /* Main Content */
        .container { max-width: 1100px; margin: 40px auto; background: var(--bg); padding: 60px; box-shadow: 0 4px 15px rgba(0,0,0,0.1); border-radius: 8px; }
        .page { display: none; }
        .page.active { display: block; animation: fadeIn 0.5s ease; }
        
        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }

        /* Nội dung chi tiết */
        h2 { color: var(--primary); font-size: 32px; margin-bottom: 20px; border-left: 5px solid var(--accent); padding-left: 15px; }
        h3 { color: #bf360c; font-size: 24px; margin-top: 40px; }
        p { margin-bottom: 20px; text-align: justify; }
        .highlight-box { background: #fff3e0; border-radius: 8px; padding: 25px; margin: 20px 0; border: 1px solid var(--accent); }
        ul { margin-bottom: 20px; }
        li { margin-bottom: 12px; }

        /* Footer */
        footer { background: #263238; color: white; padding: 50px 20px; text-align: center; margin-top: 60px; }
        .contact-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 20px; max-width: 800px; margin: 0 auto 30px; }

        /* Đăng nhập */
        .login-btn { background: var(--primary); color: white !important; padding: 8px 15px !important; border-radius: 4px; margin-left: 10px; font-weight: bold; }
        .auth-modal { display: none; position: fixed; z-index: 2000; left: 0; top: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.6); }
        .auth-content { background: white; margin: 10% auto; padding: 30px; border-radius: 8px; width: 320px; position: relative; text-align: center; color: #333; }
        .auth-content input { width: 100%; padding: 10px; margin: 10px 0; border: 1px solid #ddd; border-radius: 4px; box-sizing: border-box; }
        .auth-submit { width: 100%; background: var(--primary); color: white; border: none; padding: 10px; border-radius: 4px; cursor: pointer; font-weight: bold; }
        .close-x { position: absolute; right: 15px; top: 10px; cursor: pointer; font-size: 20px; }
        .switch-auth { font-size: 13px; color: var(--primary); cursor: pointer; margin-top: 15px; text-decoration: underline; }
    </style>
</head>
<body>

<nav>
    <div class="logo">83-Sóc Trăng</div>
    <ul class="nav-links">
        <li><a onclick="tab(event, 'home')" class="active">Trang chủ</a></li>
        <li><a onclick="tab(event, 'history')">Lịch sử hình thành</a></li>
        <li><a onclick="tab(event, 'temple')">Chùa chiềng</a></li>
        <li><a onclick="tab(event, 'food')">Món ăn</a></li>
        <li><a onclick="tab(event, 'fest')">Lễ hội</a></li>
        <li><a onclick="tab(event, 'culture')">Văn hóa phi vật thể</a></li>
        <li><a onclick="tab(event, 'econ')">Nền Kinh tế</a></li>
        <li><a onclick="tab(event, 'tour')">Du lịch</a></li>
        <li><a onclick="tab(event, 'author')">Tác giả</a></li>
        <li><a onclick="openAuth()" class="login-btn">Đăng nhập</a></li>
    </ul>
</nav>

<div class="banner">
    <h1 id="b-text">83 SÓC TRĂNG</h1>
</div>

<div class="container">
    <div id="home" class="page active">
        <h2>Giới thiệu chung về Sóc Trăng</h2>
        <p>Sóc Trăng là tỉnh ven biển thuộc tiểu vùng ven biển Đông của Đồng bằng sông Cửu Long, nằm ở hạ lưu sông Hậu và sở hữu đường bờ biển dài 72km, là cửa ngõ giao thương quan trọng của khu vực. Nơi đây nổi tiếng là vùng đất đa văn hóa với sự chung sống và giao thoa của ba dân tộc chính là Kinh, Khmer, và Hoa, tạo nên một bức tranh văn hóa độc đáo. Sự đa dạng này thể hiện rõ nhất qua kiến trúc với hơn 90 ngôi chùa Khmer cổ kính và các lễ hội truyền thống đặc sắc như Lễ hội Oóc Om Bóc gắn liền với Đua Ghe Ngo truyền thống. Về mặt kinh tế, Sóc Trăng có thế mạnh về nông nghiệp (trồng lúa, mía), thủy sản (tôm sụ, tôm thẻ), và công nghiệp chế biến, là một trong những vựa lúa và thủy sản lớn của cả nước. Bên cạnh đó, ẩm thực Sóc Trăng cũng vô cùng phong phú, từ món ăn biểu tượng Bún Nước Lèo hòa quyện hương vị ba dân tộc cho đến đặc sản làm quà trứ danh là Bánh Pía và Lạp Xưởng Vũng Thơm, thu hút du khách tìm đến để khám phá và thưởng thức.</p>
        <div class="highlight-box">
            <strong>Mục tiêu trang web:</strong> Cung cấp cái nhìn toàn diện về lịch sử, kinh tế và con người Sóc Trăng, từ đó góp phần quảng bá du lịch và gìn giữ các giá trị văn hóa truyền thống.
        </div>
    </div>

    <div id="history" class="page">
        <h2>Lịch sử hình thành & Tên gọi</h2>
        <p>Tên gọi <strong>Sóc Trăng</strong> bắt nguồn từ tiếng Khmer là <strong>"Srok Kh'leang"</strong>. Trong đó, "Srok" có nghĩa là xứ, vùng; "Kh'leang" là kho chứa, vựa chứa. Srok Kh'leang là vùng đất có kho chứa bạc của nhà vua. Người Việt đọc trại âm thành Sóc Kha Lang, sau cùng trở thành Sóc Trăng.</p>
        <p>Sóc Trăng có nguồn gốc từ tiếng Khmer là "Srok Kh'leang" (Xứ có kho chứa bạc của nhà vua), là vùng đất lịch sử thuộc Ba Thắc của Chân Lạp trước khi được cắt dâng cho Chúa Nguyễn vào năm 1757, sau đó thuộc dinh Long Hồ và đến năm 1835 (đời Minh Mạng) thì được đặt là phủ Ba Xuyên thuộc tỉnh An Giang. Trong thời Pháp thuộc, khu vực này lần lượt đổi thành hạt thanh tra Ba Xuyên rồi hạt thanh tra Sóc Trăng, và chính thức được thành lập là Tỉnh Sóc Trăng vào khoảng năm 1900. Giai đoạn 1956-1975, chính quyền Việt Nam Cộng hòa sáp nhập Sóc Trăng và Bạc Liêu thành tỉnh Ba Xuyên, với tỉnh lỵ đặt tại Sóc Trăng (Khánh Hưng). Sau năm 1975, Sóc Trăng thuộc về tỉnh Hậu Giang cũ và đến ngày 26 tháng 11 năm 1991, tỉnh Sóc Trăng được tái lập theo Nghị quyết của Quốc hội, chính thức tách ra và giữ nguyên tên gọi cho đến ngày nay, là nơi giao thoa văn hóa đặc sắc của ba dân tộc Kinh, Khmer, và Hoa.</p>
        <h3>Các giai đoạn quan trọng:</h3>
        <ul>
            <li><strong>Thời phong kiến:</strong> Thuộc phủ Ba Xuyên, là vùng đất quan trọng trong việc khai khẩn miền Nam.</li>
            <li><strong>Thời Pháp thuộc:</strong> Được thành lập thành tỉnh Sóc Trăng năm 1899.</li>
            <li><strong>Sau năm 1975:</strong> Hợp nhất với Cần Thơ thành tỉnh Hậu Giang, sau đó chia tách lại thành tỉnh Sóc Trăng vào năm 1992.</li>
        </ul>
    </div>

    <div id="temple" class="page">
        <h2>Hệ thống Chùa chiềng Đặc sắc</h2>
        <h3>1. Chùa Dơi (Chùa Mahatup)</h3>
        <p>Đây là công trình nghệ thuật vĩ đại của người Khmer. Điểm đặc biệt nhất là khuôn viên chùa có hàng ngàn con dơi sinh sống. Dù trong vùng có nhiều ngôi chùa khác nhưng dơi chỉ tập trung về đây.</p>

<img src=" https://thamhiemmekong.com/wp-content/uploads/2020/03/chua-doi.jpg">

        <h3>2. Chùa Chén Kiểu (Chùa Sà Lôn)</h3>
        <p>Ngôi chùa sử dụng những mảnh chén, bát, đĩa sứ vỡ để ốp lên tường trang trí. Kỹ thuật này không chỉ tạo nên vẻ ngoài rực rỡ dưới ánh nắng mà còn thể hiện sự sáng tạo và tiết kiệm của người dân địa phương.</p>

<img src=" https://thamhiemmekong.com/wp-content/uploads/2020/04/chuachenkieu-1.jpg">

        <h3>3. Chùa Som Rong</h3>
        <p>Tên đầy đủ là Wat Pătum Wongsa Som Rong. Ngôi chùa nổi tiếng với bảo tháp màu xám uy nghiêm và bức tượng Phật Thích Ca nhập niết bàn dài nhất Việt Nam (63m). Đây là điểm đến tâm linh kết hợp với check-in hiện đại hàng đầu tỉnh.</p>

<img src=" https://thamhiemmekong.com/wp-content/uploads/2020/03/chuasomrong2-1024x768.jpg">

        <h3>4. Chùa Kh'leang</h3>
        <p>Một trong những ngôi chùa cổ nhất Sóc Trăng với tuổi đời hơn 500 năm. Chùa gắn liền với truyền thuyết về sự hình thành địa danh Srok Kh'leang.</p>

<img src="https://thamhiemmekong.com/wp-content/uploads/2020/07/chuakhleng2.jpg">

    </div>

    <div id="food" class="page">
        <h2>Ẩm thực Sóc Trăng - Sự giao thoa hương vị</h2>
        <div class="highlight-box">
            <h3>Bún Nước Lèo</h3>
            <p>Được mệnh danh là "món ăn đoàn kết" vì có sự kết hợp của mắm bò hóc (Khmer), heo quay (Hoa) và bún tươi, rau sống (Kinh). Nước dùng trong, thơm mùi sả và ngải bún.</p>

<img src=" https://soctrangtourism.vn/wp-content/uploads/2026/01/bun-nuoc-leo-soc-trang-dam-da-huong-vi-am-thuc-tay-nam-bo-01-1664031706.jpeg">

        </div>
        <h3>Bánh Pía Vũng Thơm</h3>
        <p>Đặc sản nức tiếng cả nước và xuất khẩu quốc tế. Bánh có lớp vỏ mỏng nhiều lớp xếp chồng lên nhau, nhân sầu riêng, đậu xanh, khoai môn quyện cùng trứng muối béo ngậy.</p>

<img src=" https://mia.vn/media/uploads/blog-du-lich/lang-nghe-banh-pia-vung-thom-bieu-tuong-cho-van-hoa-am-thuc-viet-nam-1-1665441647.jpg">

        <h3>Bánh Cống Đại Tâm</h3>
        <p>Bánh có hình dáng giống cái cống, làm từ bột gạo, đậu xanh, thịt băm. Mặt bánh đặt một con tôm đất chiên giòn, ăn kèm với nước mắm chua ngọt và rất nhiều loại rau rừng.</p>

<img src=" https://imagevietnam.vnanet.vn/upload/2011/9/9/9-2011At0173.jpg">

        <h3>Bún Gỏi Già</h3>
        <p>Món ăn có vị chua thanh của me, bùi của đậu phộng và ngọt của tôm, thịt luộc. Đây là biến tấu độc đáo của món gỏi cuốn nhưng được ăn như bún nước.</p>
    </div>

    <div id="fest" class="page">
        <h2>Lễ hội đặc sắc</h2>
        <h3>1. Lễ hội Oóc Om Bok (Lễ cúng Trăng)</h3>
        <p>Diễn ra vào đêm rằm tháng 10 âm lịch. Người dân cúng trăng bằng cốm dẹp để tạ ơn thần Mặt Trăng đã ban cho mùa màng bội thu. Hoạt động đặc sắc nhất là Đua Ghe Ngo trên sông Maspero.</p>
        <h3>2. Lễ Sen Đôn-ta (Lễ cúng ông bà)</h3>
        <p>Lễ hội thể hiện lòng hiếu thảo, tri ân tổ tiên của người Khmer, có ý nghĩa tương đương với lễ Vu Lan của người Kinh.</p>
        <h3>3. Lễ hội Thác Côn</h3>
        <p>Hay còn gọi là Lễ hội Cúng Dừa tại vùng An Hiệp, Châu Thành. Người dân dâng những trái dừa tươi trang trí đẹp mắt để cầu an lành.</p>
    </div>

    <div id="culture" class="page">
        <h2>Văn hóa Phi vật thể</h2>
        <ul>
            <li><strong>Nghệ thuật Dù Kê:</strong> Loại hình kịch hát dân gian của người Khmer, được công nhận là Di sản phi vật thể quốc gia.</li>
            <li><strong>Nghệ thuật Rô-bam:</strong> Kịch múa cổ điển với các mặt nạ nhân vật độc đáo.</li>
            <li><strong>Nhạc Ngũ âm:</strong> Dàn nhạc sử dụng 5 loại chất liệu âm thanh khác nhau, thường biểu diễn trong các dịp lễ chùa.</li>
        </ul>
    </div>

    <div id="econ" class="page">
    <div class="table-container">
    <h3>Số liệu & Thế mạnh phát triển</h3>
    <table class="table-econ">
        <thead>
            <tr>
                <th>Lĩnh vực</th>
                <th>Sản phẩm chủ lực</th>
                <th>Vị thế / Thành tựu</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td><strong>Nông nghiệp</strong></td>
                <td>Gạo ST24, ST25</td>
                <td>Gạo ngon nhất thế giới</td>
            </tr>
            <tr>
                <td><strong>Thủy sản</strong></td>
                <td>Tôm sú, Tôm thẻ chân trắng</td>
                <td>Kim ngạch xuất khẩu tỷ USD</td>
            </tr>
            <tr>
                <td><strong>Năng lượng</strong></td>
                <td>Điện gió, điện mặt trời</td>
                <td>Tiềm năng lớn nhất ĐBSCL</td>
            </tr>
            <tr>
                <td><strong>Du lịch</strong></td>
                <td>Văn hóa tâm linh, Lễ hội</td>
                <td>Điểm đến đặc sắc vùng sông nước</td>
            </tr>
            <tr>
                <td><strong>Hạ tầng</strong></td>
                <td>Cảng nước sâu Trần Đề</td>
                <td>Cửa ngõ ra biển Đông tương lai</td>
            </tr>
        </tbody>
    </table>
    </div>
        <h2>Nền Kinh tế Sóc Trăng</h2>
        <p>Sóc Trăng là tỉnh có thế mạnh đặc biệt về nông nghiệp. Tỉnh dẫn đầu cả nước về sản lượng gạo ST24, ST25 (Top đầu gạo ngon nhất thế giới) và kim ngạch xuất khẩu tôm.</p>
        <p>Hiện nay, tỉnh đang tập trung phát triển <strong>Năng lượng sạch</strong> (Điện gió ngoài khơi) và <strong>Kinh tế biển</strong> với dự án Cảng nước sâu Trần Đề trong tương lai.</p>
    </div>

    <div id="tour" class="page">
        <h2>Du lịch & Trải nghiệm</h2>
        <ul>
            <li><strong>Chợ nổi Ngã Năm:</strong> Nơi lưu giữ nét văn hóa giao thương sông nước đặc trưng của miền Tây.</li>
            <li><strong>KDL Sinh thái Hồ Bể:</strong> Bãi biển hoang sơ ven dải rừng phòng hộ Vĩnh Châu.</li>
            <li><strong>Cù Lao Dung:</strong> Vùng đất thiên nhiên với rừng bần rễ lạc và những vườn trái cây trĩu quả.</li>
        </ul>
    </div>

    <div id="author" class="page">
        <h2>Thông Tin Tác Giả</h2>
        <div class="highlight-box">
            <p><strong>Nhóm thực hiện:</strong> Lý Vĩnh Toàn, Nguyễn Hữu Lộc, Huỳnh Bảo Khang, Nguyễn Hoàng Quân, Lý Đắc Phú</p>
            <p><strong>Đơn vị:</strong> Lớp 12A2 - Trường THPT Hoàng Diệu</p>
            <p><strong>Ngày thực hiện:</strong> 06/11/2025</p>
            <hr>
            <p><em>Lời nhắn: Trang web vẫn đang trong quá trình hoàn thiện và có tham khảo từ nhiều nguồn tư liệu lịch sử, báo chí. Chúc bạn đọc có những trải nghiệm thú vị về quê hương Sóc Trăng!</em></p>
        </div>
    </div>
</div>

<div id="authModal" class="auth-modal">
    <div class="auth-content">
        <span class="close-x" onclick="closeAuth()">&times;</span>
        <div id="loginForm">
            <h2 style="border:none; padding:0; font-size: 24px;">Đăng Nhập</h2>
            <input type="text" placeholder="Tên đăng nhập">
            <input type="password" placeholder="Mật khẩu">
            <button class="auth-submit" onclick="alert('Đăng nhập thành công!')">Vào hệ thống</button>
            <p class="switch-auth" onclick="toggleAuth('reg')">Chưa có tài khoản? Đăng ký</p>
        </div>
        <div id="registerForm" style="display:none;">
            <h2 style="border:none; padding:0; font-size: 24px;">Đăng Ký</h2>
            <input type="text" placeholder="Họ và tên">
            <input type="email" placeholder="Email">
            <input type="password" placeholder="Mật khẩu">
            <button class="auth-submit" onclick="alert('Đăng ký thành công!')">Tạo tài khoản</button>
            <p class="switch-auth" onclick="toggleAuth('login')">Đã có tài khoản? Đăng nhập</p>
        </div>
    </div>
</div>

<footer>
    <div class="contact-grid">
        <div><strong>Địa chỉ</strong><br>TP. Sóc Trăng, Tỉnh Sóc Trăng</div>
        <div><strong>Điện thoại</strong><br>0377682218</div>
        <div><strong>Email</strong><br>lyvinhtoan12102000@gmail.com</div>
    </div>
    <p>© 2025 83 Sóc Trăng - Toàn Lộc Khang Phú Quân. All Rights Reserved.</p>
</footer>

<script>
    function tab(e, id) {
        const pages = document.querySelectorAll('.page');
        pages.forEach(p => p.classList.remove('active'));
        document.getElementById(id).classList.add('active');
        const links = document.querySelectorAll('.nav-links a');
        links.forEach(l => l.classList.remove('active'));
        e.currentTarget.classList.add('active');
        const titles = {
            'home': '83 SÓC TRĂNG', 'history': 'LỊCH SỬ', 'temple': 'CHÙA CHIỀNG',
            'food': 'ẨM THỰC', 'fest': 'LỄ HỘI', 'culture': 'VĂN HÓA',
            'econ': 'KINH TẾ', 'tour': 'DU LỊCH', 'author': 'TÁC GIẢ'
        };
        document.getElementById('b-text').innerText = titles[id];
        window.scrollTo(0, 0);
    }
    function openAuth() { document.getElementById('authModal').style.display = 'block'; }
    function closeAuth() { document.getElementById('authModal').style.display = 'none'; }
    function toggleAuth(type) {
        document.getElementById('loginForm').style.display = (type === 'reg') ? 'none' : 'block';
        document.getElementById('registerForm').style.display = (type === 'reg') ? 'block' : 'none';
    }
    window.onclick = function(event) { if (event.target == document.getElementById('authModal')) closeAuth(); }
</script>

</body> 
</html>
