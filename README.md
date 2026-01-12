<!DOCTYPE html>
<html lang="bn">
<head>
  <meta charset="UTF-8" />
  <title>Khamon Kumar | Personal Website</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <style>
    body {font-family:'Segoe UI',sans-serif;margin:0;background:#0f172a;color:#e5e7eb}
    header {background:linear-gradient(135deg,#1e3a8a,#0f766e);padding:60px 20px;text-align:center}
    header h1 {font-size:42px;margin-bottom:10px}
    nav {background:#020617;padding:12px;text-align:center;position:sticky;top:0}
    nav a {color:#e5e7eb;margin:0 15px;text-decoration:none}
    section {max-width:1000px;margin:40px auto;padding:0 20px}
    .card {background:#020617;border-radius:16px;padding:30px;box-shadow:0 20px 40px rgba(0,0,0,.4);margin-bottom:30px}
    h2 {color:#38bdf8}
    input,textarea {width:100%;padding:12px;border-radius:8px;border:none;margin-bottom:10px}
    button {background:#38bdf8;border:none;padding:12px 20px;border-radius:10px;font-size:16px;cursor:pointer}
    .hidden {display:none}
    img {max-width:100%;border-radius:12px;margin:10px 0}
    footer {text-align:center;padding:30px;background:#020617;color:#94a3b8}
  </style>
</head>
<body>
<header>
  <h1>Khamon Kumar</h1>
  <p>Nimgachi, Bazar, Raiganj, Sirajgonj,</p>
  <p2>Mobile No : +88018716165</p2>
</header>
<nav>
  <a href="#about">About</a>
  <a href="#gallery">Gallery</a>
  <a href="#blog">Diary / Blog</a>
  <a href="#contact">Contact</a>
  <a href="#login">Admin</a>
</nav>
<section id="about">
  <div class="card">
    <h2>My Self</h2>
    <h4> Khamon</h4>
    <p>ঠিকানা: নিমগাছী বাজার, রায়গঞ্জ, সিরাজগঞ্জ</p>
    <p>পিতা: শ্রী সুখিত চন্দ্র বসাক | মাতা: পূষ্প বালা</p>
    <p>যারা পরিচিত তাদেরকে নতুন করে কিছু বলার নেই।
    কিন্তু পুরোনো বন্ধুদের নতুন করে বলতে চাই। আমি ক্ষুদ্র দুনিয়াতে সামান্য একজন মানব</p>
    
    <p> ভালোবাসার মানুষ নেই, শূণ্যতায় কেটেছে পুরো জীবন। নিজের পছন্দের জীনিস গুলো কখনোই কিনতে পারি নাই। মনের মতো করে </p>
  </div>
</section>
<section id="gallery">
  <div class="card">
    <h2>Photo Gallery</h2>
    <img src="https://via.placeholder.com/600x400" />
    <img src="https://via.placeholder.com/600x400" />
  </div>
</section>
<section id="blog">
  <div class="card">
    <h2>ডায়েরি / ব্লগ</h2>
    <div id="posts"></div>
  </div>
</section>
<section id="login">
  <div class="card">
    <h2>Admin Login</h2>
    <input type="password" id="pass" placeholder="Enter Password" />
    <button onclick="login()">Login</button>
  </div>
</section>
<section id="admin" class="hidden">
  <div class="card">
    <h2>New Blog Post</h2>
    <textarea id="postText" placeholder="আজকের ডায়েরি লিখুন..."></textarea>
    <button onclick="addPost()">Publish</button>
  </div>
</section>
<section id="contact">
  <div class="card">
    <h2>যোগাযোগ</h2>
    <p>📞 01871616565</p>
    <p>📧 khamon.kumar.70@gmail.com</p>
    <p>🌐 Facebook: khamon.kumar.70</p>
  </div>
</section>
<footer>© 2026 Khamon Kumar</footer>
<script>
  const PASSWORD = "Shetu@70AA"; // change password
  function login(){
    if(document.getElementById('pass').value===PASSWORD){
      document.getElementById('admin').classList.remove('hidden');
      alert('Login Successful');
    } else alert('Wrong Password');
  }
  function addPost(){
    const text=document.getElementById('postText').value;
    const div=document.createElement('div');
    div.innerHTML=`<p>${text}</p><hr>`;
    document.getElementById('posts').prepend(div);
    document.getElementById('postText').value='';
  }
</script>
</body>
</html>
