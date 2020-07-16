## टायमर जोडा

\--- task \---

एक उलटी मोजणी करणारा टाइमर तयार करा मंचावर एका नवीन चलच्या मदतीने ज्याला म्हणतात `time`{:class="block3variables"}. टाइमर ची सुरवात ३० सेकंद पास्न झाली पाहिजे आणि उलटी मोजणी ० सेकंद पर्यंत.

![Stage sprite](images/stage-sprite.png)

\--- hints \---

\--- hint \---

एक `variable`{:class="block3variables"} तयार करा, त्याला 'वेळ' असा बोलवा, आणि त्याच्या मूल्य `30`वर सेट करा.

मग उलटी मोजणी मध्ये कोड जोडा`time`{:class="block3variables"}० ते ३० सेकंदात. हे करण्या साठी, वजाबाकी करा`1` मधून `time`{:class="block3variables"} प्रत्येक`1`सेकंद, आणि हे पुन्हा करा जोपर्यंत`time`{:class="block3variables"}ची बरोबरी `0` ची सोबत होत नाही.

\--- /hint \---

\--- hint \---

आपल्याला आवश्यक असलेले ब्लॉक येथे आहेत:

```blocks3
repeat until < >

end

wait (1) seconds

change [time v] by (1)

(time)

when flag clicked

<() = ()>

set [time v] to [0]
```

\--- /hint \---

\--- hint \---

तुमचा नवीन कोड कसा असावा हे येथे आहेः:

```blocks3
when flag clicked
set [time v] to [30]
repeat until <(time) = (0)>
    wait (1) seconds
    change [time v] by (-1)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

एक`broadcast`{:class="block3control"} तयार करा जे 'शेवट' हे संदेश पाठवतो. एक`broadcast`{:class="block3control"} हे स्पीकरवरील घोषणेसारखे आहे: हे तुमच्या सर्व स्प्राइट्सद्वारे ऐकले जाऊ शकते. `broadcast`{:class="block3control"} ब्लॉक जोडा टाइमर कोडच्या शेवटला ज्याणेंकरून कोड 'शेवट' हा संदेश पाठवेल जेव्हा `time`{:class="block3variables"}पर्यंत मोजले आहे.

![Stage sprite](images/stage-sprite.png)

```blocks3
    broadcast (end v)
```

\--- /task \---

\--- task \---

तुमचा पात्र sprite निवडा आणि काही कोड जोडा जेणेकरून sprite `stops the other scripts`{:class="block3control"} जेव्हा ते प्राप्त करते `end`{:class="block3control"}संदेश.

![Giga sprite](images/giga-sprite.png)

```blocks3
    when I receive [end v]
    stop [other scripts in sprite v]
```

\--- /task \---

\--- task \---

आपल्या खेळाची परत चाचणी करा. जेव्हा टाइमर 0 पर्यंत मोजला जात नाही तोपर्यंत हे प्रश्न विचारणे सुरू ठेवावे.

\--- /task \---