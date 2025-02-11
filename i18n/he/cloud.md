---
title: "אחסון בענן"
icon: material/file-cloud
description: ספקי אחסון בענן רבים דורשים את האמון שלך שהם לא יסתכלו על הקבצים שלך. אלו חלופות פרטיות!
---

ספקי אחסון ענן רבים דורשים את האמון המלא שלך בכך שהם לא יסתכלו על הקבצים שלך. החלופות המפורטות להלן מבטלות את הצורך באמון על ידי מתן שליטה על הנתונים שלך או על ידי יישום E2EE.

אם חלופות אלה אינן מתאימות לצרכים שלך, אנו מציעים לך לבדוק את [תוכנת ההצפנה](encryption.md).

??? השאלה "מחפשים את NextCloud?"

    NextCloud הוא [עדיין כלי מומלץ](productivity.md) לאחסון עצמי של חבילת ניהול קבצים, אך איננו ממליצים כרגע על ספקי אחסון צד שלישי של Nextcloud, מכיוון שאיננו ממליצים על הפונקציונליות המובנית של Nextcloud ב - E2EE עבור משתמשים ביתיים.

## Proton Drive

!!! recommendation

    ![Proton Drive לוגו](assets/img/cloud/protondrive.svg){ align=right }
    
    **Proton Drive** הוא שירות אחסון קבצים כללי E2EE של ספק הדוא"ל המוצפן הפופולרי [Proton Mail](https://proton.me/mail).
    
    [:octicons-home-16: דף הבית](https://proton.me/drive){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="מדיניות פרטיות" }
    [:octicons-info-16:](https://proton.me/support/drive){ .card-link title=תיעוד}
    [:octicons-code-16:](https://github.com/ProtonMail/WebClients){ .card-link title="קוד מקור" }
    
    ??? downloads "הורדות"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=me.proton.android.drive)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1509667851)


## קריטריונים

**שים לב שאיננו קשורים לאף אחד מהפרויקטים שאנו ממליצים עליהם.** בנוסף ל [הקריטריונים הסטנדרטיים שלנו](about/criteria.md), פיתחנו סט ברור של דרישות כדי לאפשר לנו לספק המלצות אובייקטיביות. אנו מציעים לך להכיר את הרשימה הזו לפני שתבחר להשתמש בפרויקט, ולערוך מחקר משלך כדי להבטיח שזו הבחירה הנכונה עבורך.

!!! example "חלק זה הוא חדש"

    אנו עובדים על קביעת קריטריונים מוגדרים לכל קטע באתר שלנו, והדבר עשוי להשתנות. אם יש לך שאלות כלשהן לגבי הקריטריונים שלנו, אנא [שאל בפורום שלנו](https://discuss.privacyguides.net/latest) ואל תניח שלא שקלנו משהו כשהצענו את ההמלצות שלנו אם הוא לא רשום כאן. ישנם גורמים רבים שנחשבים ונדונים כאשר אנו ממליצים על פרויקט, ותיעוד כל אחד מהם הוא עבודה בתהליך.

### דרישות מינימליות

- חייב לאכוף הצפנה מקצה לקצה.
- יש להציע תוכנית חינם או תקופת ניסיון לבדיקה.
- צריך לתמוך בתמיכה באימות רב-גורמי TOTP או FIDO2, או כניסות מפתח סיסמה.
- חייב להציע ממשק אינטרנט התומך בפונקציונליות ניהול קבצים בסיסית.
- חייב לאפשר ייצוא קל של כל הקבצים/המסמכים.
- חייב להשתמש בהצפנה סטנדרטית ומבוקרת.

### המקרה הטוב ביותר

הקריטריונים הטובים ביותר שלנו מייצגים את מה שהיינו רוצים לראות מהפרויקט המושלם בקטגוריה זו. ייתכן שההמלצות שלנו לא יכללו חלק מהפונקציונליות הזו או את כולה, אך אלו שכן כן עשויות לדרג גבוה יותר מאחרות בדף זה.

- הלקוחות צריכים להיות בקוד פתוח.
- לקוחות צריכים להיות מבוקרים במלואם על ידי צד שלישי עצמאי.
- צריך להציע ללקוחות מקומיים עבור לינוקס, אנדרואיד, Windows, macOS ו - iOS.
    - לקוחות אלה צריכים להשתלב עם כלי מערכת הפעלה מקוריים עבור ספקי אחסון בענן, כגון שילוב אפליקציות קבצים ב- iOS, או פונקציונליות DocumentsProvider באנדרואיד.
- צריך לתמוך בשיתוף קבצים קל עם משתמשים אחרים.
- אמור להציע לפחות תצוגה מקדימה בסיסית של קובץ ופונקציונליות עריכה בממשק האינטרנט.
