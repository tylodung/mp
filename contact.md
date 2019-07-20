---
layout: page
title: Liên Hệ
description: Let's talk.
permalink: /contact/
---

<style type="text/css" media="screen">
  .container {
    margin: 0px auto;
    max-width: 600px;
  }
</style>

<div class="container">

  <h2>Liên hệ</h2>
  <h1><p>- Fanpage: https://www.facebook.com/AsiniceDung/</p>
  <p>- Điện thoại liên hệ: 090 268 3189</p>
  <p>- Cơ Sở Sản Xuất: 21/4A Xuân Thới Thượng, Hóc Môn, Thành phố Hồ Chí Minh.</p></h1>
  <p><img src="https://scontent.fsgn2-4.fna.fbcdn.net/v/t1.0-9/66746613_1338941712926597_6089818516792279040_n.jpg?_nc_cat=111&_nc_eui2=AeFywX2FMuyK0MPQBj7ueJrsjPZW2PR7turWQ6iljEOmk0f5z7sZK99TalHzUbmo8oOvGAPscMvu4S-GNTtV5oi5MWKCcjw17IN6LigmlWj-Gg&_nc_oc=AQnmf7fKhXPQrhXiYkhxCqOmXllfPUhxfHbLC9BJFk-yvly6cTKMFiscUmL3f210d1o&_nc_ht=scontent.fsgn2-4.fna&oh=0c348a3a6a7c7a03ba07e07ed1725d61&oe=5DA77F60"></p>

  <div id="form" class="contact-form">
     
    <li><a class="feed" href="https://docs.google.com/forms/d/e/1FAIpQLSfFzVUIZlyyK-TiKsZNTf-MKubPu_ip7zJQUpQzLq4JcsBVOw/viewform" title="Bấm ngay"><button type="submit">ĐẶT HÀNG</button></a></li>
      
    
  </div>

</div>

<script type="text/javascript">
function adjust_textarea(h) {
    h.style.height = "200px";
    h.style.height = (h.scrollHeight)+"px";
}
</script>

<script src="https://unpkg.com/vue@2.4.2"></script>
<script src="https://unpkg.com/vee-validate@2.0.0-rc.8"></script>
<script type="text/javascript">
Vue.use(VeeValidate);

new Vue({
  el: '#form',
  delimiters: ['${', '}'],
  methods: {
    validateBeforeSubmit: function () {
      this.$validator.validateAll();
      if (!this.errors.any()) {
        this.$refs.contact.submit();
      }
    }
  }
});
</script>
