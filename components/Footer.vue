<script>

export default {

}
</script>

<template>
  <div class="container">
    <footer>
      <div>
          <p>FA EXHIBITION</p>
          <p>〒152-0035 東京都目黒区自由が丘1-1-1 PARK SIDE HALL</p>
          <p class="contact">
            Tel: 03-1111-1111<br>
            E-mail: info@xxxxxxx.jp
          </p>
          <ul class="sns">
            <li><a href="#" target="_blank">Twitter</a></li>
            <li><a href="#" target="_blank">Facebook</a></li>
            <li><a href="#" target="_blank">Instagram</a></li>
          </ul>
        </div>
        <ul class="copyright">
          <li><a href="#">PRIVACY POLICY</a></li>
          <li>&copy; FA EXHIBITION</li>
        </ul>
    </footer>
  </div>
</template>

<style scoped>
li {
  list-style: none;
}
a {
  color: #fff;
  text-decoration: none;
}
.container {
  background-color: #050507;
  color: #fff;
}
footer {
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
  font-size: 0.75rem;
  padding: 80px 30px;
  text-align-last: left;
}
p {
  line-height: 15px;
}
.sns {
  display: flex;
  align-items: center;
  margin-top: 30px;
  padding: 0;
}
.sns li {
  margin-right: 15px;
}
.copyright {
  display: flex;
  align-items: center;
}
.copyright li:last-child {
  margin-left: 30px;
}
</style>