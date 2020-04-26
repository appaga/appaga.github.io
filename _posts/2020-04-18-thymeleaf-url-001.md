---
title: "Springboot Thymeleaf Link URLs"
author: APPAGA
date: 2020-04-18 22:00:00 +0900
categories: [Web,spring]
tags: [springboot, thymeleaf]
---

# 타임리프 URL 링크 걸기

`th:href` 속성으로 링크를 작성한다.

```html
<!-- Will produce 'http://localhost:8080/gtvg/order/details?orderId=3' (plus rewriting) -->
<a href="details.html"
th:href="@{http://localhost:8080/gtvg/order/details(orderId=${o.id})}">view</a>
<!-- Will produce '/gtvg/order/details?orderId=3' (plus rewriting) -->
<a href="details.html" th:href="@{/order/details(orderId=${o.id})}">view</a>
<!-- Will produce '/gtvg/order/3/details' (plus rewriting) -->
<a href="details.html" th:href="@{/order/{orderId}/details(orderId=${o.id})}">view</a>
```

[타임리프 사이트: Standard URL Syntax](https://www.thymeleaf.org/doc/articles/standardurlsyntax.html)