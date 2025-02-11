---
title: "הזרמת וידאו"
icon: material/video-wireless
description: רשתות אלו מאפשרות לך להזרים תוכן אינטרנט מבלי לבנות פרופיל פרסומי המבוסס על תחומי העניין שלך.
---

האיום העיקרי בעת שימוש בפלטפורמת הזרמת וידאו הוא שהרגלי הסטרימינג ורשימות המנויים שלך יוכלו לשמש אותך כדי ליצור פרופיל. עליך לשלב את הכלים האלה עם [VPN](vpn.md) או [Tor](https://www.torproject.org/) כדי להקשות על פרופיל השימוש שלך.

## קליינטים

!!! recommendation

    ![LBRY לוגו](assets/img/video-streaming/lbry.svg){ align=right }
    
    **The LBRY network** היא רשת שיתוף וידאו מבוזרת. הוא משתמש ברשת דמוית [BitTorrent](https://wikipedia.org/wiki/BitTorrent) כדי לאחסן את תוכן הווידאו, וב-[blockchain](https://wikipedia.org/wiki/Blockchain) כדי לאחסן את האינדקסים עבור הסרטונים האלה. היתרון העיקרי של עיצוב זה הוא התנגדות לצנזורה.
    
    **לקוח שולחן העבודה של LBRY** עוזר לך להזרים סרטונים מרשת LBRY ומאחסן את רשימת המנויים שלך בארנק LBRY משלך.
    
    [:octicons-home-16: דף הבית](https://lbry.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://lbry.com/privacypolicy){ .card-link title="מדיניות פרטיות" }
    [:octicons-info-16:](https://lbry.com/faq){ .card-link title=תיעוד}
    [:octicons-code-16:](https://github.com/lbryio/lbry-desktop){ .card-link title="קוד מקור" }
    
    ??? downloads "הורדות"
    
        - [:simple-windows11: Windows](https://lbry.com/windows)
        - [:simple-apple: macOS](https://lbry.com/osx)
        - [:simple-linux: Linux](https://lbry.com/linux)

!!! note "הערה"

    מומלץ רק **לקוח שולחני LBRY**, שכן לאתר [Odysee](https://odysee.com) וללקוחות LBRY ב-F-Droid, ב-Play Store וב-App Store יש סנכרון וטלמטריה חובה.

!!! warning "אזהרה"

    בזמן צפייה ואירוח בסרטונים, כתובת ה-IP שלך גלויה לרשת LBRY. שקול להשתמש ב-[VPN](vpn.md) או [Tor](https://www.torproject.org) אם [מודל האיום](basics/threat-modeling.md) שלך דורש הסתרת כתובת ה-IP שלך.

אנו ממליצים **נגד** סנכרון הארנק שלך עם LBRY Inc., מכיוון שסנכרון ארנקים מוצפנים עדיין אינו נתמך. אם אתה מסנכרן את הארנק שלך עם LBRY Inc., אתה צריך לסמוך עליהם שלא יסתכלו ברשימת המנויים שלך, קרנות [LBC](https://lbry.com/faq/earn-credits), או להשתלט על הערוץ שלך.

ניתן להשבית *שמירת נתוני אירוח כדי לעזור לרשת LBRY* באפשרות :gear: **הגדרות** ← **הגדרות מתקדמות**, כדי להימנע מחשיפת כתובת ה-IP והסרטונים שצפיתם בעת השימוש ב-LBRY למשך תקופה ממושכת.

## קריטריונים

**שים לב שאיננו קשורים לאף אחד מהפרויקטים שאנו ממליצים עליהם.** בנוסף ל [הקריטריונים הסטנדרטיים שלנו](about/criteria.md), פיתחנו סט ברור של דרישות כדי לאפשר לנו לספק המלצות אובייקטיביות. אנו מציעים לך להכיר את הרשימה הזו לפני שתבחר להשתמש בפרויקט, ולערוך מחקר משלך כדי להבטיח שזו הבחירה הנכונה עבורך.

!!! example "חלק זה הוא חדש"

    אנו עובדים על קביעת קריטריונים מוגדרים לכל קטע באתר שלנו, והדבר עשוי להשתנות. אם יש לך שאלות כלשהן לגבי הקריטריונים שלנו, אנא [שאל בפורום שלנו](https://discuss.privacyguides.net/latest) ואל תניח שלא שקלנו משהו כשהצענו את ההמלצות שלנו אם הוא לא רשום כאן. ישנם גורמים רבים שנחשבים ונדונים כאשר אנו ממליצים על פרויקט, ותיעוד כל אחד מהם הוא עבודה בתהליך.

- חייב לא לדרוש חשבון מרוכז כדי לצפות בסרטונים.
    - אימות מבוזר, כגון באמצעות מפתח פרטי של ארנק נייד מקובל.
