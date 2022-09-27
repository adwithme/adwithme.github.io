---
layout: post
title: Calculate The Number of Days in Excel 
subtitle: Hidden Formula on Excel
cover-img: /img/posts/Excel/Excel.png
thumbnail-img: /img/posts/Excel/Excel.png
share-img: /img/posts/Excel/Excel.png
tags: [Excel]
Comments: True
---

Have you ever needed to determine the number of days, months or years between two dates? Calculating the number of days using Excel is pretty simple. Just use a formula to subtract the later date from the earlier date.

For example, if cell A1 contains 1-Jan-2004 and cell A2 contains 03-Mar-2004, you simply enter the formula =A2-A1 in cell A3 to get the number of days. If the result you get looks like a weird date rather than a number of days, that's because Excel assumed you were entering another date and automatically formatted cell A3 as a date.

To fix that, from the _Home tab_ click the Number Formats dropdown (in the Number group) and select _General_. Your answer should be *62*.

![Excel](/img/posts/Excel/Excel-IMG.jpg)

However, calculating the number of months or years between two dates isn't so obvious. There's a Function in Excel that makes this task easy but for some reason Microsoft has hidden it away. You won't find it in the Functions list (Formulas, Insert Function). This 'secret' function is called *DATEDIF* (i.e. date difference).

Let's use the same dates as above. The syntax for the function is...


> =DATEDIF(startdate,enddate,"interval")


Our formula to calculate the number of complete months between the two dates would be...


> =DATEDIF(A1,A2,"m")


Similarly, the formula to calculate the number of complete years is =DATEDIF(A1,A2,"y"), although in our example it would yield 0 complete years. Change cell A1 to a date a year or more earlier and you'll see the result.

![Excel](/img/posts/Excel/Excel-IMG2.png)

#### A few of things to keep in mind about the DATEDIF function:

1) The start date must be less than or equal to the end date, otherwise it will give an error.

2) Acceptable interval codes are "d", "m", "y", "ym", "yd", "md" (with quotes).

3) It may appear obvious what the "ym", "yd", and "md" interval codes do but they require a second look. The "ym" interval code yields the number of months between the two dates as if they were in the same year and ignores the year. The "yd", and "md" interval codes yields the number of days between the two dates as if they were in the same year and ignores the year.

To calculate the number of years, months and days between two dates (more than a year apart) you can use this formula (assuming your start date is in cell A1 and your end date is in cell A2).

Rather than attempting to retype this formula below, simply highlight and copy it from here, paste into your formula bar and then adjust the cell references as necessary.

> =DATEDIF(A1,A2,"y") & " years, " & DATEDIF(A1,A2,"ym") & " months, " & DATEDIF(A1,A2,"md") & " days"
