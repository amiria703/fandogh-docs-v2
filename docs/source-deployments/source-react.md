---
id: source-react
title: پروژه‌هایReact
sidebar_label: پروژه‌های React
description: 'در این بخش به توضیح چگونگی دیپلوی کردن سرویس React Project بدون نیاز به دانش docker می‌پردازیم.'
keywords:
  - "سکوی ابری"
  - داکر
  - service
  - container
  - React
  - react
  - "react.js"
  - framework
  - "اجرای مستقیم کد"
  - "source deployment"
  - "سرویس داکری"
  - docker
  - "سکوی ابری فندق"
  - "زیرساخت ابری"
image: /img/docs/thumbnails/source-deployments/reactjs-thumbnail.png
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

 ![React.JS](/img/docs/reactjs-banner.svg "React.JS")

دیپلوی کردن سرویس‌ها بر روی فندق برای کاربرانی که با docker کار نکرده‌اند ممکن است مقداری مبهم باشد؛ همینطور معمولا آماده سازی پروژه‌ها برای اجرا در محیط واقعی نیاز به تنظیماتی دارد که باعث پیچیده شدن کار برنامه‌نویس می‌شود.<br/>
ما در این بخش به توضیح چگونگی دیپلوی کردن سرویس `React Project` بدون نیاز به دانش docker می‌پردازیم.

:::tip fandogh-cli setup
اگر هنوز fandogh-cli بر روی کامپیوتر شما نصب نیست از طریق این [مستند] [getting_started] می‌توانید cli را بر روی کامپیوتر خود نصب کنید.
:::

در پوشه اصلی پروژه، بعد از اینکه در فندق login کردید دستور `fandogh source init` را اجرا کنید. در اولین مرحله شما می‌بایست اسم سرویس رو انتخاب نمایید.

```
Service Name: myReactProject
```

 بعد از وارد کردن نام Service  برای شما گزینه هایی که بدون نیاز به دانش docker قابل اجرا هستند نمایش داده می شود. از بین گزینه های نمایش داده شده گزینه **React Project** را انتخاب کنید.

:::note توجه
توجه داشته باشید برای انتخاب، شماره گزینه مورد نظر را وارد کنید.
::::

```yaml {6}
-[1] Static Website
-[2] Django Project
-[3] Laravel Project
-[4] ASP.NET Core Project
-[5] Vue.js Project
-[6] React Project
Please choose one of the project types above:
```

در قسمت بعدی شما باید context را وارد کنید. اگر در حال حاضر در پوشه اصلی نیستید می توانید آدرس آن را وارد کنید یا در غیر این صورت خالی بگذارید و دکمه enter را فشار دهید.

```
The context directory [.]:
```


پس از مشخص کردن اطلاعات فوق، فایلی با نام fandogh.yml در پوشه جاری شما ساخته می‌شود.
اکنون با نوشتن دستور `fandogh source run` می‌توانید پروژه خودتان را بر روی فندق دیپلوی کنید.

:::tip راهنمایی
پس از هر بار تغییر در پروژه تنها کافیست که دستور fandogh source run را مجددا اجرا کنید.
فایل `fandogh.yml` می‌تواند شامل تمام بخش‌هایی که در [مانیفست] [service_manifest] فندق است باشد٬ شما به صورت دستی قادر هستید تا بخش‌های مورد نیاز این فایل را تغییر دهید.
:::

## فیلم‌های آموزشی

<Tabs
  groupId="reactjs-source-deployment-tutorials"
  defaultValue="deploy"
  values={[
    {label: 'استقرار', value: 'deploy'},
    {label: 'دامنه دلخواه', value: 'domains'},
  ]
}>
<TabItem value="deploy">
<figure class="video-container">
  <video src="https://media.fandogh.cloud/tutorials/source-deployments/reactjs/reactjs-source-deploy.mp4" controls></video>
</figure>
</TabItem>

<TabItem value="domains">
<figure class="video-container">
  <video src="https://media.fandogh.cloud/tutorials/source-deployments/reactjs/reactjs-add-domain.mp4" controls></video>
</figure>
</TabItem>

</Tabs>


[getting_started]: /docs/preface/getting-started
[service_manifest]: /docs/services/service-manifest
