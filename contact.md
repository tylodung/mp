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
  <h1><p>- Fanpage: https://www.facebook.com/AsiniceDung/</p></h1>
  <p><span>- Điện thoại liên hệ:</span> 090 268 3189</p>
  <p><span>- Địa chỉ:</span> 21/4A Xuân Thới Thượng, Hóc Môn, Thành phố Hồ Chí Minh.</p>

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
