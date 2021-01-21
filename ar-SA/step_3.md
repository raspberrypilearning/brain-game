## التحدي: تغيير المظاهر

--- task ---

قم بإنشاء مؤقت للعد التنازلي على المنصة (الخلفية) بمساعدة متغير جديد يسمى `الوقت`{:class="block3variables"}. يجب أن يبدأ المؤقت من 30 ثانية والعد التنازلي حتى 0 ثانية.

![كائن منصة العمل](images/stage-sprite.png)

--- hints ---


--- hint ---

قم بإنشاء `متغير`{:class="block3variables"} ، يمكنك تسميته "الوقت" وضبط قيمته على `30`.

ثم أضف تعليمة برمجية لحساب `الوقت`{:class="block3variables"} وصولاً إلى 0 في غضون 30 ثانية. للقيام بذلك ، اطرح `1` من `الوقت`{:class="block3variables"} كل `1` ثانيًا ، وكرر هذه العملية حتى يصبح `الوقت`{:class="block3variables"} تساوي `0`.

--- /hint ---

--- hint ---

فيما يلي الكتل البرمجية التي تحتاجها:

```blocks3
repeat until < >

end

wait (1) seconds

change [الوقت v] by (1)

(الوقت)

when flag clicked

<() = ()>

set [الوقت v] to [0]
```

--- /hint ---

--- hint ---

هذا ما يجب أن يبدو عليه التعليمة البرمجية الجديدة:

```blocks3
when flag clicked
set [الوقت v] to [30]
repeat until <(الوقت) = (0)>
    wait (1) seconds
    change [الوقت v] by (-1)
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

قم بإنشاء `بث`{:class="block3control"} التي ترسل الرسالة "نهاية". إن `بث الرسالة`{:class="block3control"} يشبه إعلان على مكبر صوت: يمكن سماعه من قبل جميع الكائنات الخاصة بك. أضف التعليمة البرمجية`بث الرسالة`{:class="block3control"} إلى نهاية التعليمة البرمجية المؤقت بحيث يرسل التعليمة البرمجية وتنتهي الرسالة عندما يكون `الوقت`{:class="block3variables"} قد تم العد إلى `0`.

![كائن منصة العمل](images/stage-sprite.png)

```blocks3
    broadcast (النهاية v)
```

--- /task ---

--- task ---

حدد كائن الشخصية الخاصة بك وأضف بعض التعليمات البرمجية له بحيث`توقف الكائنات الاخرى`{:class="block3control"} عندما تتلقى رسالة`النهاية`{:class="block3control"}.

![الكائن كيكا](images/giga-sprite.png)

```blocks3
    when I receive [النهاية v]
    stop [other scripts in sprite v]
```

--- /task ---

--- task ---

اختبر لعبتك مرة أخرى. يجب أن تستمر في طرح الأسئلة حتى يصبح المؤقت للعد التنازلي يساوي 0.

--- /task ---