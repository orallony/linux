# תרגול בלינוקס - LAB-01

## 📁 ניווט וקבצים
פתח את הטרמינל.

הצג את התיקייה הנוכחית בה אתה נמצא:
`pwd`

הצג את כל הקבצים בתיקייה הנוכחית:
`ls`

הצג גם קבצים מוסתרים:
`ls -a`

עבור לתיקיית הבית:
`cd ~`

עבור לתיקיית Documents:
`cd Documents`

חזור תיקייה אחת אחורה:
`cd ..`

צור תיקייה בשם test:
`mkdir test`

עבור לתוך התיקייה test:
`cd test`

צור קובץ ריק בשם file1.txt:
`touch file1.txt`

צא מהתיקייה הנוכחית:
`cd ..`

מחק תיקייה ריקה בשם test2:
`rmdir test2`

צור כמה תיקיות יחד:
`mkdir -p a/b/c`

הצג עץ תיקיות:
`ls -R`

העתק תיקייה עם כל התוכן:
`cp -r a/ b/`

עבור לתיקייה העליונה ביותר:
`cd /`

בדוק כמה מקום תופסות תיקיות:
`du -sh *`

בדוק כמה מקום פנוי בדיסק:
`df -h`

עבור לתיקייה לפי נתיב מוחלט:
`cd /var/log`

צור תיקייה בשם ניסוי וכתוב לתוכה קובץ:
`mkdir ניסוי && echo 'בדיקה' > ניסוי/בדיקה.txt`


## 📝 עריכה פשוטה
כתוב לקובץ:
`echo "Hello Linux" > file1.txt`

הוסף שורה נוספת:
`echo "Another line" >> file1.txt`

הצג את תוכן הקובץ:
`cat file1.txt`

הצג את תחילת הקובץ:
`head file1.txt`

הצג את סוף הקובץ:
`tail file1.txt`

ערוך קובץ עם עורך nano:
`nano file1.txt`

הצג תוכן מדורג:
`less file1.txt`

צור קובץ חדש עם שורות טקסט:
`echo -e "שורה1\nשורה2" > multi.txt`

חפש מילה בקובץ:
`grep "Hello" file1.txt`

מיין שורות בקובץ:
`sort file1.txt`

מחק קובץ:
`rm file1.txt`

שמור פלט של פקודה לקובץ:
`ls > list.txt`

צרף שני קבצים:
`cat a.txt b.txt > c.txt`

מנה מספר תווים בקובץ:
`wc -m file1.txt`

מנה מילים בקובץ:
`wc -w file1.txt`


## 🔄 ניהול קבצים ותיקיות
צור תיקייה בשם backup והעתק אליה קובץ:
`mkdir backup`
`cp file1.txt backup/`

שנה שם של קובץ:
`mv file1.txt notes.txt`

מחק קובץ:
`rm notes.txt`

מחק תיקייה עם תוכן:
`rm -r backup`

העתק כמה קבצים יחד:
`cp *.txt folder/`

העבר קובץ מתיקייה לתיקייה אחרת:
`mv file.txt folder/`

שמור עותק של קובץ בשם אחר:
`cp notes.txt notes_backup.txt`

השווה בין שני קבצים:
`diff file1.txt file2.txt`

בדוק אם קובץ קיים:
`[ -f file1.txt ] && echo "קיים"`

בדוק אם תיקייה קיימת:
`[ -d folder ] && echo "תיקייה קיימת"`

צור תיקייה עם רווח בשם:
`mkdir "my folder"`

העתק קובץ מהורדה לתיקיית הבית:
`cp ~/Downloads/file.txt ~`

הפוך קובץ לקריא בלבד:
`chmod 444 file.txt`

הפוך קובץ לבעל הרשאות כתיבה:
`chmod +w file.txt`

צור קובץ מוסתר:
`touch .hidden.txt`


## 🔍 חיפוש ומידע
חפש קובץ בשם notes.txt:
`find . -name "notes.txt"`

ראה מידע על קובץ:
`ls -l notes.txt`

בדוק את סוג הקובץ:
`file notes.txt`

ספר שורות בקובץ:
`wc -l notes.txt`

מצא קבצים ששונו היום:
`find . -type f -mtime 0`

מצא קבצים גדולים מ־10MB:
`find . -size +10M`

מצא קבצים עם סיומת log:
`find /var/log -name "*.log"`

מצא קובץ לפי תוכן:
`grep -r "error" .`

חפש מילה בתוך קובץ:
`grep "Linux" file1.txt`

חפש מילה ללא תלות באותיות גדולות/קטנות:
`grep -i "linux" file1.txt`

מצא קבצים בלי הרשאות קריאה:
`find . ! -readable`

בדוק למי שייך קובץ:
`ls -l file.txt`

מצא קבצים ריקים:
`find . -type f -empty`

מצא קבצים שנערכו בשעה האחרונה:
`find . -type f -mmin -60`

מצא קבצים לפי שם שמכיל חלק:
`find . -name "*report*"`


## ⚙️ הרשאות וביצוע
צור קובץ script.sh:
`echo "echo Hello" > script.sh`

תן הרשאות הרצה:
`chmod +x script.sh`

הרץ את הסקריפט:
`./script.sh`

בדוק את ההרשאות של קובץ:
`ls -l script.sh`

שנה בעלות על קובץ:
`sudo chown username file.txt`

מנע הרצת קובץ:
`chmod -x script.sh`

אפשר הרצת סקריפט דרך bash:
`bash script.sh`

צפה בתהליכים רצים:
`ps aux`

הפסק תהליך לפי מספר זיהוי:
`kill PID`

הרץ תהליך ברקע:
`./script.sh &`

הצג פקודות שהרצת:
`history`

נקה את ההיסטוריה:
`history -c`

הרץ פקודה בשם אחר:
`alias ll="ls -l"`

הסר alias:
`unalias ll`

צור סקריפט שמבצע חישוב:
`echo "echo $((2+3))" > math.sh`


## 📦 ניהול תוכנה
בדוק גרסת מערכת:
`uname -a`

בדוק אם curl מותקן:
`which curl`

התקן curl:
`sudo apt install curl`

הסר curl:
`sudo apt remove curl`

חפש חבילה במאגר:
`apt search nano`

עדכן את רשימת החבילות:
`sudo apt update`

שדרג את המערכת:
`sudo apt upgrade`

הצג גרסה של חבילה:
`apt show nano`

בדוק אם git מותקן:
`git --version`

התקן git:
`sudo apt install git`

בדוק מקום פנוי:
`df -h`

בדוק זיכרון פנוי:
`free -h`

בדוק אם תוכנה פועלת:
`systemctl status ssh`

התחל שירות:
`sudo systemctl start ssh`

הפעל שירות עם אתחול:
`sudo systemctl enable ssh`


## 🧠 כלים שימושיים
תיעוד לפקודה:
`man ls`

נקה את המסך:
`clear`

צא מהטרמינל:
`exit`

שנה סיסמה:
`passwd`

ראה מי מחובר למערכת:
`who`

בדוק את הזמן הנוכחי:
`date`

בדוק את שם המשתמש שלך:
`whoami`

ראה את שם המחשב:
`hostname`

צור alias לפקודה נפוצה:
`alias cls="clear"`

בדוק את כתובת ה-IP שלך:
`ip a`

שלח פינג לאתר:
`ping google.com`

חשב md5 של קובץ:
`md5sum file.txt`

צפה בכוננים מחוברים:
`lsblk`

מצא מיקום של תוכנה:
`whereis nano`

בדוק זמינות חיבור לאינטרנט:
`curl -I http://example.com`


# תרגול חופשי

צור את הספרייה Data ובתוכה את הקבצים הבאים (שים לב לקבצים נסתרים):  
   .data1, data2, data_3, .data, my_name  

צור את הספרייה Zoo ובתוכה את הקבצים:  
   Visitors, animals, keeper  

צור את הספרייה Progs ובתוכה את הקבצים:  
   .prog1.c, prog2.c, small_prog, medium_prog, .pro1.exe, my_prog  

צור את הספרייה Family בתוך ספרית Zoo.

השתמש בעורך הטקסט nano. צור קובץ בשם name_My וכתוב בו את שמך בשורה הראשונה וכתובתך בשורה השנייה.

צור קובץ בשם family_My וכתוב בו שמות שלושה בני משפחה – אחד בכל שורה.

וודא כי הקבצים תחת ספריית Family.

העתק את קובץ name_My לקובץ בשם name.

שנה שמו של קובץ family_My ל-Family.

צור קובץ בשם family_Whole המורכב משרשור Family ו-name.  
    `cat name Family >> Whole_family`

הצג את family_Whole.

עבור ל-directory home שלך.

שנה את שם ספריית Zoo ל-zoo_My.

העתק את ספריית Family על תוכנה ל-directory home שלך.

מחק את ספריית zoo_My על תוכנה.

חשב את נפח ספריית הבית שלך באמצעות.
