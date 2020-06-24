## إنشاء الأسئلة

لنبدأ بإنشاء الأسئلة العشوائية ليجيب عنها اللاعب.

--- task ---

افتح مشروع سكراتش (Scratch) جديدًا وفارغًا.

**اتصال بالانترنيت:** افتح مشروع سكراتش Scratch جديد عبر الانترنيت من [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**من دون اتصال انترنيت:** افتح مشروع سكراتش Scratch جديد عبر برنامج سكراتش الموجود على جهازك دون اتصال بالانترنيت.

اذا تحتاج تنزيل وتنصيب برنامج السكراتش Scratch على جهازك الشخصي، ستجده في [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

--- /task ---

--- task ---

اختر كائن و خلفية شاشة للعبتك. يمكنك اختيار ما يعجبك! إليك مثالًا:

![لقطة الشاشة](images/brain-setting.png)

--- /task ---

--- task ---

تأكد من أنك حددت شخصيتك المتحركة. قم بإنشاء متغيرين جديدين ، يدعى `رقم 1 `{:class="block3variables"} و `رقم 2 `{:class="block3variables"} ، لتخزين أرقام أسئلة الاختبار.

![لقطة الشاشة](images/giga-sprite.png)

![لقطة الشاشة](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

أضف تعليمة برمجية لكائن الشخصية الخاص بك لتعيين كلاً من `المتغيرات`{:class="block3variables"} إلى رقم `عشوائي`{:class="block3operators"} بين 2 و12.

![لقطة الشاشة](images/giga-sprite.png)

```blocks3
when flag clicked
set [العدد 1 v] to (pick random (2) to (12))
set [العدد 2 v] to (pick random (2) to (12))
```

--- /task ---

--- task ---

أضف تعليمة برمجية إلى `اسأل`{:class="block3sensing"} اللاعب للإجابة، ثم `قل لمدة ثوانين`{:class="block3looks"} سواء كان الجواب صحيحاً أو خاطئًا:

![لقطة الشاشة](images/giga-sprite.png)

```blocks3
when flag clicked
set [العدد 1 v] to (pick random (2) to (12))
set [العدد 2 v] to (pick random (2) to (12))
+ ask (join (العدد 1)(join [ x ] (العدد 2))) and wait
+ if <(answer) = ((العدد 1)*(العدد 2))> then
+ say [نعم! :)] for (2) seconds
+ else
+ say [لا :(] for (2) seconds
+ end
```

--- /task ---

--- task ---

اختبر مشروعك مرتين: أجب عن سؤال بشكل صحيح ، والآخر بشكل غير صحيح.

--- /task ---

--- task ---

أضف `حلقة كرِّر باستمرار`{:class="block3control"} حول التعليمة البرمجية هذه، لتظهر أسئلة كثيرة للاعب.

--- hints ---

--- hint ---

تحتاج إلى إضافة لنبة حلقة تكرارية`للأبد`{:class="block3control"} ، ووضع جميع التعليمات البرمجية فيها باستثناء`عند نقر العلم`{:class="block3control"}.

--- /hint ---

--- hint ---

هنا الكتلة (اللبنة) التي تحتاجها:

```blocks3
forever
end
```

--- /hint ---

--- hint ---

و هذا ما يجب أن تبدو عليه التعليمات البرمجية الخاصة بك:

```blocks3
when flag clicked
+ forever
    set [العدد 1 v] to (pick random (2) to (12))
    set [العدد 2 v] to (pick random (2) to (12))
    ask (join (العدد 1)(join [ x ] (العدد 2))) and wait
    if <(answer) = ((العدد 1)*(العدد 2))> then
        say [نعم! :)] for (2) seconds
    else
        say [لا :(] for (2) seconds
    end
end
```

--- /hint ---

--- /hints ---

--- /task ---