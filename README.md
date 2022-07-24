# Domain Message Flow Modelling

Designing loosely-coupled systems requires more than carefully designed boundaries. Carefully defined interactions between bounded contexts is equally important.

A [bounded context](https://martinfowler.com/bliki/BoundedContext.html) is a sub-system in a software architecture aligned to a part of the domain. It can be implemented as a microservice or a module within a monolith.

A Domain Message Flow Diagram is a simple visualisation showing the flow of messages (commands, events, queries) between actors, bounded contexts, and systems, for a single scenario.


# مدل سازی جریان پیام دامنه

طراحی سیستم‌های loosely-couple به چیزی بیش از مرزهایی که به دقت طراحی شده‌اند نیاز دارد. تعاملات با دقت تعریف شده بین Bounded Context ها  نیز به همان اندازه مهم است.

یک [bounded context](https://martinfowler.com/bliki/BoundedContext.html) یک زیر سیستم در معماری نرم افزار است که با بخشی از دامنه تراز شده است. می توان آن را به عنوان یک میکروسرویس یا یک ماژول در یک مونولیت پیاده سازی کرد.

نمودار جریان پیام دامنه یک رسم ساده است که جریان پیام ها (دستورات، رویدادها، پرس و جوها) را بین بازیگران، Bounded Contextها و سیستم ها برای یک سناریو نشان می دهد.

## Formats

There are 2 basic formats, but there is no formal specification so adjust the tool to suit your needs if the basic formats don't work for you.

### Separate Message & Contents

The separate message & contents format uses 2 shapes for each message: 1 for the name and order of the message and a separate box to display the contents of the message (the information it carries).

The benefit of this format is that you can focus on the flow of messages without getting bogged down by the message contents at the start.

Start by showing just the messages flowing between senders and receivers (with the order number on the message).

![Message Flow Just Messages](resources/just-messages-no-contents.jpg)

Then show the contents of each message in a separate box next to each message:

![Message Flow Messages & Contents](resources/messages-and-contents.jpg)

### Combined Message & Contents

The combined message & contents format uses a single shape to capture the message name, order, and contents.

![Example Message Flow](resources/domain-message-flow.jpg "An Example Domain Message Flow")

This format is good when you want to focus on the contents of each message from the beginning.



## فرمت ها

2 فرمت اصلی وجود دارد، اما هیچ مشخصات رسمی وجود ندارد، بنابراین اگر فرمت های اصلی برای شما کار نمی کنند، ابزار را مطابق با نیازهای خود تنظیم کنید.

### پیام و محتوا را جدا کنید

قالب جداگانه پیام و محتوا از 2 شکل برای هر پیام استفاده می کند: 1 برای نام و ترتیب پیام و یک کادر جداگانه برای نمایش محتوای پیام (اطلاعاتی که حمل می کند).

مزیت این فرمت این است که می توانید روی جریان پیام ها تمرکز کنید بدون اینکه در ابتدا درگیر محتوای پیام شوید.

فقط با نشان دادن پیام هایی که بین فرستنده و گیرنده جریان دارند (با شماره سفارش روی پیام) شروع کنید.

![Message Flow Just Messages](resources/just-messages-no-contents.jpg)

سپس محتویات هر پیام را در یک کادر جداگانه در کنار هر پیام نشان دهید:

![Message Flow Messages & Contents](resources/messages-and-contents.jpg)

### پیام و محتویات ترکیبی

قالب ترکیبی پیام و محتوا از یک شکل واحد برای ثبت نام، سفارش و محتوای پیام استفاده می کند.

![نمونه جریان پیام](resources/domain-message-flow.jpg "An Example Domain Message Flow")

این قالب زمانی خوب است که بخواهید از ابتدا روی محتوای هر پیام تمرکز کنید.



### Downloads

- [Domain Message Flow Modelling (miro board backup)](resources/Domain-Message-Flow-Modelling-en-v1.rtb)

## How to Use

When you have an initial cut of your architecture - you have identified candidate bounded contexts - you can begin design the message flows.

Start by creating a list of of scenarios to model. And then for each scenario create a diagram

When creating a diagram, the typical flow is:

1. Start with an actor/context/system
2. Create the message they want to send
3. Add the recipient of the message and a line connecting the sender and the receiver
4. Place the message close to the line
5. Repeat steps 1 - 4 until your scenario is complete

The message should contain 3 elements:

1. The name of the message
2. The significant data contained within the message
3. The order in which the message occurs in the flow being modelled



## نحوه استفاده

هنگامی که یک برش اولیه از معماری خود دارید - زمینه های محدود نامزد را شناسایی کرده اید - می توانید طراحی جریان پیام را شروع کنید.

با ایجاد لیستی از سناریوها برای مدل سازی شروع کنید. و سپس برای هر سناریو یک نمودار ایجاد کنید

هنگام ایجاد یک نمودار، جریان معمولی به صورت زیر است:

1. با یک بازیگر/Context/سیستم شروع کنید
2. پیامی را که می خواهند ارسال کنند ایجاد کنید
3. گیرنده پیام و خطی که فرستنده و گیرنده را به هم متصل می کند اضافه کنید
4. پیام را نزدیک خط قرار دهید
5. مراحل 1 تا 4 را تکرار کنید تا سناریوی شما کامل شود

پیام باید شامل 3 عنصر باشد:

1. نام پیام
2. داده های مهم موجود در پیام
3. ترتیبی که پیام در جریان مدل سازی رخ می دهد



## Visualisation Tips

The number one problem with Domain Message Flow Diagrams, and diagrams in general, is too much information. [Miller's Law](https://en.wikipedia.org/wiki/Miller%27s_law) is a good heuristic to use here. Aim to have between 5 and 9 messages on your diagram.

If you find that adding the data to each message is breaking your flow of progress, you can defer the data section of each message it until you have placed all of your messages.

## Additional Resources

- [DDD Pattern: Library Contexts](https://medium.com/nick-tune-tech-strategy-blog/ddd-pattern-library-contexts-d6ae81f462ef)
- [Mapper Contexts & Supercontexts: Decoupling Domain-Specific and Domain-Generic Bounded Contexts](https://medium.com/nick-tune-tech-strategy-blog/mapper-contexts-supercontexts-decoupling-domain-specific-and-domain-generic-bounded-contexts-5eb6a1e7c5fc)
- [Gateway Interchange Contexts](https://medium.com/nick-tune-tech-strategy-blog/gateway-interchange-contexts-899696e67848)

## Contributors

Thanks to all [existing and future contributors](https://github.com/ddd-crew/domain-message-flow-modelling/graphs/contributors) and to the following individuals who have all contributed to Domain Message Flow Modelling:

- [Kacper Gunia](https://github.com/cakper)
- [Zsofia Herendi](https://twitter.com/zherendi)
- [Nick Tune](https://github.com/ntcoding)

Domain Message Flow Diagrams are heavily inspired by:

- [Simon Brown's C4 Container Diagrams](https://c4model.com/)
- [Domain Storytelling](https://domainstorytelling.org/)

## Contributions and Feedback

The Domain Message Flow Modelling notation is freely available for you to use. In addition, your feedback and ideas are welcome to improve the technique or to create alternative versions.

Feel free to also send us a pull request with your examples.

[![CC BY 4.0][cc-by-shield]][cc-by]

This work is licensed under a [Creative Commons Attribution 4.0 International
License][cc-by].

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg
