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

  <h2>Thông tin chi tiết

Tên gọi: Mỹ Phẩm Á Châu hoặc Mỹ Phẩm AsiNice.

Điện thoại liên hệ: 090 268 3189 (Đoàn Bình)

Địa chỉ: 21/4A Xuân Thới Thượng, Hóc Môn, Thành phố Hồ Chí Minh.</h2>

  <div id="form" class="contact-form">
    <form accept-charset="UTF-8" method="POST" action="https://formspree.io/{{ site.email }}" v-on:submit.prevent="validateBeforeSubmit" ref="contact">
      <fieldset>
        <input type="hidden" name="_subject" value="New contact!" />
        <input type="hidden" name="_next" value="{{ site.url }}/contact/message-sent/" />
        <input type="hidden" name="_language" value="en" />

        <legend>Personalia:</legend>
    Name: <input type="text"><br>
    Email: <input type="text"><br>
    Date of birth: <input type="text"><br>
    Date of birth: <textarea name="message" placeholder="Test Message"></textarea>


        <button type="submit">Send</button>
      </fieldset>
    </form>
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
