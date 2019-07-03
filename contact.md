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

  <h2>Thông tin Đặt Hàng</h2>

  <div id="form" class="contact-form">
    <form accept-charset="UTF-8" method="POST" action="https://docs.google.com/spreadsheets/d/1o8ys1TbjshTOLbNH5-xtwoKCNAs6Zrx8RBl1aQEi_Vc/edit#gid=449555141" v-on:submit.prevent="validateBeforeSubmit" ref="contact">
      <fieldset>
        <input type="hidden" name="_subject" value="New contact!" />
        <input type="hidden" name="_next" value="{{ site.url }}/contact/message-sent/" />
        <input type="hidden" name="_language" value="en" />

        <p><legend><p>Điện thoại liên hệ: 090 268 3189 (Đoàn Bình)</p>
	Địa chỉ: 21/4A Xuân Thới Thượng, Hóc Môn, Thành phố Hồ Chí Minh.</legend></p>
    <span>Họ và Tên:</span> <input type="text"><br>
    <span>Số điện thoại:</span> <input type="text"><br>
    <span>Ngày giao hàng:</span> <input type="text"><br>
    <span>Nội Dung:</span> <textarea name="message" placeholder="tên sản phẩm muốn mua"></textarea>


        <button type="submit">Send</button>
      </fieldset>
    </form>
  </div>

</div>

function guiBieuMau(e)
{
  // Thay thế bằng địa chỉ email của bạn
  var email = "doan.trong.quoc.binh@gmail.com";
  // Tiêu đề của email được gửi về
  var subject = "Đơn đặt hàng";
  // Không rành thì đùng đụng vào code ở dưới nhé
  var s = SpreadsheetApp.getActiveSheet();
  var columns = s.getRange(1,1,1,s.getLastColumn()).getValues()[0];  
  var message = "";  
  // Lấy ra những thông tin nào có dữ liệu điền vào
  for ( var keys in columns ) {
    var key = columns[keys];
    if ( e.namedValues[key] && (e.namedValues[key] != "") ) {

      message += key + ' :: '+ e.namedValues[key] + "\n\n";
    }
  }
  // Dùng MailApp service của Google Apps Script để gửi về email của bạn.
  MailApp.sendEmail(email, subject, message);

}