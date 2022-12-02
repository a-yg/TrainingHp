<script>
export default {
  methods: {
    accessImg() {
      let contact_position = $('#contact').offset().top - $(window).height();
      if(scroll > access_position){
      // #contactが表示されるまでの間は、背景画像をfadeInで表示する
      if(scroll < contact_position){
        $('.bg').fadeIn(500);
      } else {
        $('.bg').fadeOut(500);
      }
    // #accessが表示される前の場合
      } else {
        // 背景画像を表示しない
        $('.bg').fadeOut(500);
      }
    }
  }
}

</script>

<template>
  <div class="container">
    <main>

      <div id="mainvisual">
        <img src="../img/mainvisual1.jpg">
        <img src="../img/mainvisual2.jpg">
        <img src="../img/mainvisual3.jpg">
      </div>

      <h1 class="site-title inview fadein">
        Hello Flower!<br>
        FA EXHIBITION 2021
      </h1>
      <section id="information">
        <h2 class="section-title">INFORMATION</h2>
        <p>
          <span class="info-title-en">2021 jUL 1(THU)-3(SAT)</span><br>
          <span class="info-time-en">DAY 10am-6pm OTHER 10am-5:30pm</span>
        </p>
        <h3 class="info-place">at PARk SIDE HALL</h3>
        <p class="info-date-ja">2021年7月1日(木)-3日(土)<br>
        Day1 10時〜18時  その他10時〜17時30分</p>
      </section>

      <div id="side-btn">
        <a href="#">FOR VISITOR</a>
        <a href="#">FOR EXHIBITOR</a>
      </div>

      <section id="gallery" class="wrapper">
        <h2 class="section-title">GALLERY</h2>
        <ul class="list">
          <li class="inview fadein"><img src="../img/flower1.jpg"></li>
          <li class="inview fadein"><img src="../img/flower2.jpg"></li>
          <li class="inview fadein"><img src="../img/flower3.jpg"></li>
          <li class="inview fadein"><img src="../img/flower4.jpg"></li>
          <li class="inview fadein"><img src="../img/flower5.jpg"></li>
          <li class="inview fadein"><img src="../img/flower6.jpg"></li>
        </ul>
      </section>

      <section id="access">
        <h2 class="section-title">ACCESS</h2>
        <p class="address">
          〒152-0035 東京都目黒区自由が丘1-1-1 PARK SIDE HALL<br>
          PARK SIDE HALL, 1-1-1 Jiyugaoka, Meguro-ku, Tokyo
        </p>
        <p class="contact">
          Tel:03-111-111<br>
          Email:info@xxxx.jp
        </p>
        <a class="btn" href="#">GOOGLE MAP</a>
      </section>

      <section id="contact" class="wrapper">
        <h2 class="section-title">CONTACT</h2>
        <a class="btn" href="#">出典に関するお問い合わせ</a><br>
        <a class="btn" href="#">その他のお問い合わせ</a>
      </section>

      <div class="bg"></div>
    </main>
  </div>
</template>

<style scoped>
template {
  font-size: 100%;
}
a {
  color: #fff;
  text-decoration: none;
}
img {
  max-width: 100%;
  vertical-align: bottom;
}
li {
  list-style: none;
}
.list {
  list-style: none;
  margin: 0;
  padding: 0;
}
.wrapper {
  max-width: 800px;
  padding: 0 30px;
  margin: 0 auto;
}
.container {
  background-color: #050507;
  color: #fff;
  text-align: center;
}
#mainvisual {
  display: flex;
  overflow: hidden;
}
#mainvisual img {
  width: calc(100%/3);
  height: 100vh;
}
.site-title {
  /* text-align: center; */
  font-size: 6.25rem;
  font-weight: 300;
  letter-spacing: 0.03em;
  margin: 100px 0;
}
.section-title {
  border-bottom: 1px solid #fff;
  display: inline-block;
  font-size: 3.75rem;
  font-weight: 300;
  /* 文字間の間隔 */
  letter-spacing: 0.03em;
  margin-bottom: 45px;
}
#information .info-date-en {
  display: block;
  font-size: 1.5rem;
}
#information .info-time-en {
  display: block;
  font-size: 1.125rem;
}

#gallery {
  margin-bottom: 480px;
}
#gallery .list li {
  margin-bottom: 60px;
}
#gallery .list li img {
  width: 48%;
}
/* 奇数のliは左よせ */
#gallery .list li:nth-child(odd) {
  text-align-last: left;
}
/* 偶数のliは右よせ */
#gallery .list li:nth-child(even) {
  text-align-last: right;
}
#side-btn {
  border: solid 1px #fff;
  position: fixed;
  right: -144px;
  bottom: 200px;
  transform: rotate(-90deg) translateY(60px);
  transition: 0.6s;
  z-index: 30;
}
#side-btn a {
  width: 165px;
  font-size: 0.875rem;
  display: inline-block;
  letter-spacing: 0.1em;
  padding: 15px 0;
  transition: 0.3s;
}
#side-btn a:last-of-type {
  border-left: solid 1px #fff;
}
#side-btn a:hover {
  opacity: 0.7;
}
.bg {
  background: url("../img/bg.jpg") center center repeat !important;
  width: 100vw;
  height: 100vh;
  position: fixed;
  top: 0;
  left: 0;
  display: none;
  z-index: 10;
}

#access {
  margin-bottom: 480px;
  position: relative;
  z-index: 20;
}
#access .place {
  font-size: 1.75rem;
  font-weight: 400;
  margin-bottom: 20px;
}
#access .address {
  margin-bottom: 20px;
}
#access .contact {
  margin-bottom: 30px;
}
#access .btn {
  border: solid 1px #fff;
  color: #fff;
  display: inline-block;
  padding: 15px 82px;
  transition: 0.3s;
}
#access .btn:hover {
  background-color: #050507;
}

#contact {
  margin-bottom: 200px;
  position: relative;
  z-index: 20;
}
#contact .btn {
  width: 400px;
  border: solid 1px #7d7d7d;
  color: #fff;
  display: block;
  padding: 30px 0;
  margin: 0 auto 20px auto;
  position: relative;
  transition: 0.3s;
}
/*
ボタン矢印
*/
#contact .btn::before,
#contact .btn::after {
  content: "";
  position: absolute;
  right: -40px;
  height: 1px;
  background-color: #fff;
  transition: 0.3s;
}
/*
矢印の直線部分
*/
#contact .btn::before {
  width: 120px;
  top: 48px;
}
/*
矢印の先端部分
「rotate(25deg)」で角度をつける
*/
#contact .btn::after {
  width: 15px;
  top: 45px;
  transform: rotate(25deg);
}
#contact .btn:hover {
  opacity: 0.7;
}
#contact .btn:hover::before,
#contact .btn:hover::after {
  right: -50px;
}

@media screen and (max-width: 900px) {
  .site-title {
    font-size: 3rem;
    margin: 50px ;
  }
  .section-title {
    font-size: 2rem;
  }
  #information .info-date-en,
  #information .info-time-en,
  #information .info-date-ja {
    font-size: 1rem;
  }
  #information .info-place {
    font-size: 2rem;
  }

  #gallery {
    margin-bottom: 280px;
  }
  #gallery .list li {
    margin-bottom: 30px;
  }
  #gallery .list li img {
    width: 100%;
  }
}

</style>