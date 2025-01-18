---
layout: post
title: "J2Store plugin 3.3.6 – SQL Injection (CVE-2019-9184)"
date: 2019-02-26
description: "J2Store plugin 3.3.6 for Joomla! SQL Injection vulnerability (CVE-2019-9184)"
tags: j2store joomla sql-injection security
categories: 
featured: true
---

### Info

**Product**: J2Store Plugin for Joomla!\
**Version**: 3.x up to 3.3.6\
**Product page**: https://www.j2store.org/\
**Downloads**: 350,000+\
**CVE**: 2019-9184

### Description

Most popular shopping/e-commerce plugin for Joomla, J2Store, was vulnerable to SQL Injection until version 3.3.7. The vulnerability affects the page product.php and the vulnerable parameter is product_option[] array.\
An attacker could exploit this vulnerability by running arbitrary SQL queries on the internal database – this can lead to excalation of priviliges, ability to edit prices of products and more.

Ramesh Elamathi, the lead developer of J2Store, promptly replied willing to fix the vulnerability as soon as possible. In fact, the following day the vulnerability was fixed and 3.3.7 version was [released](http://j2store.org/blog/general/security-update-for-j2store.html).\
I was impressed by how fast he handled my report, in less than 24-hours the vulnerability was confirmed, fixed and an email was also sent to affected users.

If you are using J2Store plugin and haven’t updated to [3.3.7](http://j2store.org/blog/general/security-update-for-j2store.html) yet, make sure to update as soon as possible!

### Timeline
**19/02/2019** – Sent report to vendor\
**19/02/2019** – J2Store replied, confirmed and triaged the report\
**20/02/2019** – Vulnerability fixed and version 3.3.7 released\
**20/02/2019** – Acknowledged and rewarded\