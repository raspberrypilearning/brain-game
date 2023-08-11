## إنشاء الأسئلة

لنبدأ بإنشاء الأسئلة العشوائية ليجيب عنها اللاعب.

\--- task \---

افتح مشروع سكراتش (Scratch) جديدًا وفارغًا.

**Online:** open a new online Scratch project at [rpf.io/scratch-new](https://rpf.io/scratch-new){:target="_blank"}.

**من دون اتصال انترنيت:** افتح مشروع سكراتش Scratch جديد عبر محرر Scratch الموجود على جهازك دون اتصال بالانترنيت.

If you need to download and install the Scratch offline editor, you can find it at [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

\--- /مهمة \---

\--- مهمة \---

اختر كائن و خلفية شاشة للعبتك. يمكنك اختيار ما يعجبك! إليك مثالًا:

![لقطة الشاشة](images/brain-setting.png)

\--- /مهمة \---

\--- مهمة \---

تأكد من أنك حددت شخصيتك المتحركة. قم بإنشاء متغيرين جديدين ، يدعى ` رقم 1 ` {: class = "block3variables"} و ` رقم 2 ` {: class = "block3variables"} ، لتخزين أرقام أسئلة الاختبار.

![لقطة الشاشة](images/giga-sprite.png)

![لقطة الشاشة](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /مهمة \---

\--- task \---

أضف تعليمة برمجية لكائن الشخصية الخاص بك لتعيين كلاً من `المتغيرات`{:class="block3variables"} إلى رقم `عشوائي`{:class="block3operators"} بين 2 و12.

![لقطة الشاشة](images/giga-sprite.png)

```blocks3
when flag clicked
set [number 1 v] to (pick random (2) to (12))
set [number 2 v] to (pick random (2) to (12))
```

\--- /task \---

\--- task \---

أضف تعليمة برمجية إلى `اسأل`{:class="block3sensing"} اللاعب للإجابة، ثم `قل لمدة ثانيتين`{:class="block3looks"} سواء كان الجواب صحيحاً أو خاطئًا:

![لقطة الشاشة](images/giga-sprite.png)

```blocks3
when flag clicked
set [number 1 v] to (pick random (2) to (12))
set [number 2 v] to (pick random (2) to (12))

+ ask (join (number 1)(join [ x ] (number 2))) and wait
+ if <(answer) = ((number 1)*(number 2))> then
+ say [yes! :)] for (2) seconds
+ else
+ say [no :(] for (2) seconds
+ end
```

\--- /task \---

\--- task \---

اختبر مشروعك مرتين: أجب عن سؤال بشكل صحيح ، والآخر بشكل غير صحيح.

\--- /task \---

\--- task \---

أضف `حلقة كرِّر باستمرار`{:class="blockcontrol"} حول التعليمة البرمجية هذه، لتظهر أسئلة كثيرة للاعب.

\--- تلميحات \---

\--- تلميحات \---

تحتاج إلى إضافة لنبة حلقة تكرارية`للأبد`{:class="block3control"} ، ووضع جميع التعليمات البرمجية فيها باستثناء`عند نقر العلم`{:class="block3control"}.

\--- /hint \---

\--- hint \---

هنا الكتلة (اللبنة) التي تحتاجها:

```blocks3
forever
end
```

\--- /hint \---

\--- hint \---

و هذا ما يجب أن تبدو عليه التعليمات البرمجية الخاصة بك:

```blocks3
when flag clicked

+ forever
    set [number 1 v] to (pick random (2) to (12))
    set [number 2 v] to (pick random (2) to (12))
    ask (join (number 1)(join [ x ] (number 2))) and wait
    if <(answer) = ((number 1)*(number 2))> then
        say [yes! :)] for (2) seconds
    else
        say [no :(] for (2) seconds
    end
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---