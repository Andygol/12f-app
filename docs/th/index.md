---
title: บ้าน
description: วิธีการรับประกันความยืดหยุ่นสูงสุดในแง่ของความยืดหยุ่น ความคล่องตัว และความสามารถในการปรับขนาดเมื่อสร้างแอปพลิเคชัน SaaS
hide:
 - toc
 - navigation
---

## บทนำ

ในยุคสมัยใหม่ ซอฟต์แวร์ถูกส่งมอบทั่วไปเป็นบริการ: เรียกว่า *web apps*, หรือ *software-as-service*. twelve-factor app เป็นหลัการสำหรับสร้างแอพพลิเคชัน software-as-a-service ที่:

* ใช้รูปแบบ **declarative** สำหรับติดตั้งระบบอัตโนมัต เพื่อลดเวลาและค่าใช้จ่ายสำหรับนักพัฒนาใหม่ที่เข้าร่วมกับโครงการ;
* มี **clean contract** กับระบบปฏิบัติการที่แอพพลิเคชันทำงานด้วย นำเสนอ **maximun portibility** ระหว่างสิ่งแวดล้อมที่ระบบทำงาน;
* เหมาะสมสำหรับ **deployment** บน **cloud platforms** สมัยใหม่, ลดความต้องการของเซิร์ฟเวอร์และผู้ดูแลระบบ;
* **Maximized divergence** ระหว่างการพัฒนาและการใช้งานจริง ด้วยการใช้ **continuous deployment** เพื่อเพิ่มความเร็วสูงสุด;
* และสามารถ **scale up** โดยปราศจากการเปลี่ยนแปลงของ เครื่องมือ สถาปัตยกรรม หรือแนวทางปฏิบัตของการพัฒนา

หลักการ twelve-factor สามารถประยุกต์ใช้ได้กับแอพพลิเคชันที่เขียนด้วยภาษาใดๆ และซึ่งใช้ร่วมกับบริการสนับสนุนใดๆ (ฐานข้อมูล, คิว, หน่วยความจำเคช เป็นต้น).

## ประวัติ

ผู้มีส่วนร่วมของเอกสารนี้ได้มีส่วนเกี่ยวข้องโดยตรงกับการพัฒนาและการใช้งานแอพพลิเคชันจำนวนมาก และเกี่ยวข้องทางอ้อมสำหรับการพัฒนา การดำเนินงาน และการขยายขนาดของแอพพลิเคชันจำนวมมหาศาลผ่านงานของเราที่แพลตฟอร์ม <a href="http://www.heroku.com/" target="_blank">Heroku</a>

เอกสารนี้สังเคราะห์จากประสบการณ์และการสังเกตทั้งหมดของพวกเราบนแอพพลิเคชัน software-as-a-service ที่หลากหลายจำนวนมาก เป็นสามเหลียมของแนวทางปฏิบัตในอุดมคติสำหรับการพัฒนาแอพพลิเคชัน ให้ความสนใจเป็นพิเศษกับพลวัตของการเจริญเติบโตของแอพพลิเคชันในช่วงเวลาหนึ่ง พลวัตของการมีส่วนร่วมระหว่างนักพัฒนาที่ทำงานกับ codebase ของแอพพลิเคชัน และ<a href="http://blog.heroku.com/archives/2011/6/28/the_new_heroku_4_erosion_resistance_explicit_contracts/" target="_blank">หลีกเลี่ยงการใช้จ่ายของซอฟต์แวร์</a>.

แรงจูงใจของเราเพื่อสร้างความตระหนักของปัญหาระบบบางอย่างที่เราเห็นในการพัฒนาแอพพลิเคชันสมัยใหม่ เพื่อให้คำศัพย์ที่ใช้ร่วมกันสำหรับการพูดคุยเกี่ยวกับปัญหาเหล่านี้ และนำเสนอแนวทางแก้ไขแนวกว้างสำหรับปัญหาเหล่านี้พร้อมกับคำศัพท์ที่ใช้ประกอบกัน รูปแบบนี้ได้รับแรงบันดาลใจจากหนังสือของ Martin Fowler *<a href="https://books.google.com/books/about/Patterns_of_enterprise_application_archi.html?id=FyWZt5DdvFkC" target="_blank">Patterns of Enterprise Application Architecture</a>* และ *<a href="https://books.google.com/books/about/Refactoring.html?id=1MsETFPD3I0C" target="_blank">Refactoring</a>*.


## ใครควรจะอ่านเอกสารนี้?

นักพัฒนาที่สร้างแอพพลิเคชันซึ่งทำงานเป็นเซอร์วิซ (service) วิศวกรดำเนินงานผู้ซึ่งปรับใช้ (deploy) หรือจัดการแอพพลิเคชันดังกล่าว

## The Twelve Factors

### [I. Codebase](./codebase.md)

มีเพียง codebase เดียวที่ติดตามด้วย version control, มีหลาย deploy

### [II. Dependencies](./dependencies.md)

มีการประกาศและแยกการอ้างอิง (dependency) ทั้งหมดอย่างชัดเจน

### [III. Config](./config.md)

จัดเก็บการตั้งค่า (config) ไว้ในสิ่งแวดล้อมของระบบ

### [IV. Backing services](./backing-services.md)

จัดการกับบริการสนับสนุน (backing service) ให้เป็นทรัพยากรที่แนบมา

### [V. Build, release, run](./build-release-run.md)

แยกขั้นตอนของการ build และ run อย่างเคร่งครัด

### [VI. Processes](./processes.md)

รันแอพพลิเคชันเป็นหนึ่งหรือมากกว่าให้เป็น stateless processes

### [VII. Port binding](./port-binding.md)

นำออกบริการด้วยการเชื่อมโยง port

### [VIII. Concurrency](./concurrency.md)

ขยายออกของแอพพลิเคชันด้วยรูปแบบ process

### [IX. Disposability](./disposability.md)

เพิ่มความแข็งแกร่งด้วยการเริ่มต้นระบบอย่างรวดเร็วและปิดระบบอย่างนุ่มนวล

### [X. Dev/prod parity](./dev-prod-parity.md)

รักษา development, staging และ production ให้มีความใกล้เคียงกันที่สุด

### [XI. Logs](./logs.md)

จัดการ logs ให้เป็นแบบ event stream

### [XII. Admin processes](./admin-processes.md)

รันงานของผู้ดูแลระบบ/การจัดการให้เป็นกระบวนการแบบครั้งเดียว
