---
title: "你是人类吗？"
published: 2025-08-12
tags: ["验证"]
description: 我的 Captcha 还蛮多的，欢迎你们来这里玩，玩累了就直接刷新，没问题的~
image: ../assets/images/cloudflare-turnstile-verify-error-1.png
category: 杂项
draft: false
showcover: false
customcover: ../assets/images/cloudflare-turnstile-verify-error.png
---

<head>
    <!-- Google reCaptcha v2-->
    <!-- <script src="https://www.google.com/recaptcha/api.js" async defer></script> -->
    <script src="https://recaptcha.net/recaptcha/api.js" async defer></script>
    <!-- Cloudflare Turnstile -->
    <script src="https://challenges.cloudflare.com/turnstile/v0/api.js?onload=onloadTurnstileCallback" defer async></script>

</head>


你好~
我的 Captcha 还蛮多的，欢迎你们来这里玩，玩累了就直接刷新，没问题的~

:::NOTE["抱歉"]
现在只有两家 Captcha，后续会慢慢补上其他 Captcha 的！
:::

# Google reCaptcha V2
## 休闲版（不保证）

<form action="?" method="POST">
    <div class="g-recaptcha" data-sitekey="6LerBqQrAAAAAJm_8-H-wq25iSKxprYEW8G_XYhi"></div>
</form>

## 挑战版（不保证）

<form action="?" method="POST">
    <div class="g-recaptcha" data-sitekey="6LcQFKQrAAAAAFg294vepQULbQX11BXa0NTt-21h"></div>
</form>

<br>

# Cloudflare Turnstile

<div id="example-container"></div>

<script is:inline>
  function onloadTurnstileCallback() {
    // 确保 turnstile 对象已加载
    if (typeof turnstile !== 'undefined') {
      turnstile.render('#example-container', {
        // 重要：将下面的 sitekey 替换为你自己的
        sitekey: '0x4AAAAAABq8mQb4rm0Y4ir5', // 这是一个用于测试的 key
        callback: function(token) {
          console.log(`挑战成功，获取到的 token 是: ${token}`);
          // 在这里你可以将 token 发送到后端进行验证
        },
      });
    }
  }
</script> 