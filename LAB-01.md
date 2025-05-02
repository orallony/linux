# תרגול בלינוקס - LAB-01

## 📁 ניווט וקבצים

פתח את הטרמינל.
הצג את התיקייה הנוכחית בה אתה נמצא:
```bash
pwd
```

הצג את כל הקבצים בתיקייה הנוכחית:
```bash
ls
```

הצג גם קבצים מוסתרים:
```bash
ls -a
```

עבור לתיקיית הבית:
```bash
cd ~
```

עבור לתיקיית Documents:
```bash
cd Documents
```

חזור תיקייה אחת אחורה:
```bash
cd ..
```

צור תיקייה בשם test:
```bash
mkdir test
```

עבור לתוך התיקייה test:
```bash
cd test
```

צור קובץ ריק בשם file1.txt:
```bash
touch file1.txt
```

צא מהתיקייה הנוכחית:
```bash
cd ..
```

מחק תיקייה ריקה בשם test2:
```bash
rmdir test2
```

צור כמה תיקיות יחד:
```bash
mkdir -p a/b/c
```

הצג עץ תיקיות:
```bash
ls -R
```

העתק תיקייה עם כל התוכן:
```bash
cp -r a/ b/
```

עבור לתיקייה העליונה ביותר:
```bash
cd /
```

בדוק כמה מקום תופסות תיקיות:
```bash
du -sh *
```

בדוק כמה מקום פנוי בדיסק:
```bash
df -h
```

עבור לתיקייה לפי נתיב מוחלט:
```bash
cd /var/log
```

צור תיקייה בשם ניסוי וכתוב לתוכה קובץ:
```bash
mkdir test && echo 'i love tivonim' >> tivonily.txt
```

## 📝 עריכה פשוטה

כתוב לקובץ:
```bash
echo "Hello Linux" > file1.txt
```

הוסף שורה נוספת:
```bash
echo "Another line" >> file1.txt
```

הצג את תוכן הקובץ:
```bash
cat file1.txt
```

הצג את תחילת הקובץ:
```bash
head file1.txt
```

הצג את סוף הקובץ:
```bash
tail file1.txt
```

ערוך קובץ עם עורך nano:
```bash
nano file1.txt
```

הצג תוכן מדורג:
```bash
less file1.txt
```

צור קובץ חדש עם שורות טקסט:
```bash
echo -e "tivonily" > multi.txt
```

חפש מילה בקובץ:
```bash
grep "Hello" file1.txt
```

מיין שורות בקובץ:
```bash
sort file1.txt
```

מחק קובץ:
```bash
rm file1.txt
```

שמור פלט של פקודה לקובץ:
```bash
ls > list.txt
```

צרף שני קבצים:
```bash
cat a.txt b.txt > c.txt
```

מנה מספר תווים בקובץ:
```bash
wc -m file1.txt
```

מנה מילים בקובץ:
```bash
wc -w file1.txt
```

## 🔄 ניהול קבצים ותיקיות

צור תיקייה בשם backup והעתק אליה קובץ:
```bash
mkdir backup
cp file1.txt backup/
```

שנה שם של קובץ:
```bash
mv file1.txt notes.txt
```

מחק קובץ:
```bash
rm notes.txt
```

מחק תיקייה עם תוכן:
```bash
rm -r backup
```

העתק כמה קבצים יחד:
```bash
cp *.txt folder/
```

העבר קובץ מתיקייה לתיקייה אחרת:
```bash
mv file.txt folder/
```

שמור עותק של קובץ בשם אחר:
```bash
cp notes.txt notes_backup.txt
```

השווה בין שני קבצים:
```bash
diff file1.txt file2.txt
```

בדוק אם קובץ קיים:
```bash
[ -f file1.txt ] && echo "קיים"
```

בדוק אם תיקייה קיימת:
```bash
[ -d folder ] && echo "תיקייה קיימת"
```

צור תיקייה עם רווח בשם:
```bash
mkdir "my folder"
```

העתק קובץ מהורדה לתיקיית הבית:
```bash
cp ~/Downloads/file.txt ~
```

הפוך קובץ לקריא בלבד:
```bash
chmod 444 file.txt
```

הפוך קובץ לבעל הרשאות כתיבה:
```bash
chmod +w file.txt
```

צור קובץ מוסתר:
```bash
touch .hidden.txt
```
## 🔍 חיפוש ומידע

חפש קובץ בשם notes.txt:
```bash
find . -name "notes.txt"
```

ראה מידע על קובץ:
```bash
ls -l notes.txt
```

בדוק את סוג הקובץ:
```bash
file notes.txt
```

ספר שורות בקובץ:
```bash
wc -l notes.txt
```

מצא קבצים ששונו היום:
```bash
find . -type f -mtime 0
```

מצא קבצים גדולים מ־10MB:
```bash
find . -size +10M
```

מצא קבצים עם סיומת log:
```bash
find /var/log -name "*.log"
```

מצא קובץ לפי תוכן:
```bash
grep -r "error" .
```

חפש מילה בתוך קובץ:
```bash
grep "Linux" file1.txt
```

חפש מילה ללא תלות באותיות גדולות/קטנות:
```bash
grep -i "linux" file1.txt
```

מצא קבצים בלי הרשאות קריאה:
```bash
find . ! -readable
```

בדוק למי שייך קובץ:
```bash
ls -l file.txt
```

מצא קבצים ריקים:
```bash
find . -type f -empty
```

מצא קבצים שנערכו בשעה האחרונה:
```bash
find . -type f -mmin -60
```

מצא קבצים לפי שם שמכיל חלק:
```bash
find . -name "*report*"
```

## ⚙️ הרשאות וביצוע

צור קובץ script.sh:
```bash
echo "echo Hello" > script.sh
```

תן הרשאות הרצה:
```bash
chmod +x script.sh
```

הרץ את הסקריפט:
```bash
./script.sh
```

בדוק את ההרשאות של קובץ:
```bash
ls -l script.sh
```

שנה בעלות על קובץ:
```bash
sudo chown username file.txt
```

מנע הרצת קובץ:
```bash
chmod -x script.sh
```

אפשר הרצת סקריפט דרך bash:
```bash
bash script.sh
```

צפה בתהליכים רצים:
```bash
ps aux
```

הפסק תהליך לפי מספר זיהוי:
```bash
kill PID
```

הרץ תהליך ברקע:
```bash
./script.sh &
```

הצג פקודות שהרצת:
```bash
history
```

נקה את ההיסטוריה:
```bash
history -c
```

הרץ פקודה בשם אחר:
```bash
alias ll="ls -l"
```

הסר alias:
```bash
unalias ll
```

צור סקריפט שמבצע חישוב:
```bash
echo "echo $((2+3))" > math.sh
```

## 📦 ניהול תוכנה

בדוק גרסת מערכת:
```bash
uname -a
```

בדוק אם curl מותקן:
```bash
which curl
```

התקן curl:
```bash
sudo apt install curl
```

הסר curl:
```bash
sudo apt remove curl
```

חפש חבילה במאגר:
```bash
apt search nano
```

עדכן את רשימת החבילות:
```bash
sudo apt update
```

שדרג את המערכת:
```bash
sudo apt upgrade
```

הצג גרסה של חבילה:
```bash
apt show nano
```

בדוק אם git מותקן:
```bash
git --version
```

התקן git:
```bash
sudo apt install git
```

בדוק מקום פנוי:
```bash
df -h
```

בדוק זיכרון פנוי:
```bash
free -h
```

בדוק אם תוכנה פועלת:
```bash
systemctl status ssh
```

התחל שירות:
```bash
sudo systemctl start ssh
```

הפעל שירות עם אתחול:
```bash
sudo systemctl enable ssh
```

## 🧠 כלים שימושיים

תיעוד לפקודה:
```bash
man ls
```

נקה את המסך:
```bash
clear
```

צא מהטרמינל:
```bash
exit
```

שנה סיסמה:
```bash
passwd
```

ראה מי מחובר למערכת:
```bash
who
```

בדוק את הזמן הנוכחי:
```bash
date
```

בדוק את שם המשתמש שלך:
```bash
whoami
```

ראה את שם המחשב:
```bash
hostname
```

צור alias לפקודה נפוצה:
```bash
alias cls="clear"
```

בדוק את כתובת ה-IP שלך:
```bash
ip a
```

שלח פינג לאתר:
```bash
ping google.com
```

חשב md5 של קובץ:
```bash
md5sum file.txt
```

צפה בכוננים מחוברים:
```bash
lsblk
```

מצא מיקום של תוכנה:
```bash
whereis nano
```

בדוק זמינות חיבור לאינטרנט:
```bash
curl -I http://example.com
```

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
