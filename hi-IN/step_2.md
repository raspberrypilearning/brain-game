## प्रश्न बनाना

आप ऐसे यादृच्छिक प्रश्न बनाकर शुरू करेंगे जिनका खिलाड़ी को जवाब देना है।

\--- task \---

एक नया स्क्रैच प्रोजेक्ट खोलें।

** ऑनलाइन: ** [ rpf.io/scratch-new ](http://rpf.io/scratch-new) पर एक नया ऑनलाइन स्क्रैच प्रोजेक्ट खोलें {: लक्ष्य = "_ blank"}।

** ऑफ़लाइन: ** ऑफ़लाइन संपादक में एक नया प्रोजेक्ट खोलें।

यदि आपको स्क्रैच ऑफ़लाइन संपादक को डाउनलोड और इंस्टॉल करने की आवश्यकता है, तो आप इसे [rpf.io/scratchoff](http://rpf.io/scratchoff) {:target="_blank"} पर पा सकते हैं।

\--- /task \---

\--- task \---

Add a character sprite and a backdrop for your game. You can choose any you like! Here's an example:

![screenshot](images/brain-setting.png)

\--- /task \---

\--- task \---

Make sure you have your character sprite selected. Create two new variables, called `number 1`{:class="block3variables"} and `number 2`{:class="block3variables"}, to store the numbers for the quiz questions.

![screenshot](images/giga-sprite.png)

![screenshot](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Add code to your character sprite to set both of the `variables`{:class="block3variables"} to a `random`{:class="block3operators"} number between 2 and 12.

![screenshot](images/giga-sprite.png)

```blocks3
जब झंडा क्लिक किया
[संख्या 1 v] को (यादृच्छिक (2) से (12) के बीच चुने) स्थिर करें 
[संख्या 2 v] को (यादृच्छिक (2) से (12) के बीच चुने) स्थिर करें
```

\--- /task \---

\--- task \---

Add code to `ask`{:class="block3sensing"} the player for the answer, and then `say for 2 seconds`{:class="block3looks"} whether the answer was right or wrong:

![screenshot](images/giga-sprite.png)

```blocks3
जब झंडा क्लिक किया
[संख्या 1 v] को (यादृच्छिक (2) से (12) के बीच चुने) स्थिर करें 
[संख्या 2 v] को (यादृच्छिक (2) से (12) के बीच चुने) स्थिर करें

+ पूछें (जोड़ें (संख्या 1) (जोड़ें [x] (संख्या 2))) और प्रतीक्षा करें 
+ यदि <(उत्तर) = ((संख्या 1) * (संख्या 2))> तो
+ कहें [हाँ! :)] (2) सेकंड के लिए
+ अन्यथा
+ कहें [नहीं :(] (2) सेकंड के लिए
+ अंत
```

\--- /task \---

\--- task \---

Test your project twice: answer one question correctly, and the other incorrectly.

\--- /task \---

\--- task \---

Add a `forever`{:class="block3control"} loop around this code, so that the game asks the player lots of questions in a row.

\--- hints \---

\--- hint \---

You need to add a `forever`{:class="block3control"} block, and put all of the code except the `when flag clicked`{:class="block3control"} block into it.

\--- /hint \---

\--- hint \---

Here is the block you need:

```blocks3
हमेशा के लिए
अंत
```

\--- /hint \---

\--- hint \---

Here is what your code should look like:

```blocks3
जब झंडा क्लिक किया

+ हमेशा के लिए 
   [संख्या 1 v] को (यादृच्छिक (2) से (12) के बीच चुने) स्थिर करें 
   [संख्या 2 v] को (यादृच्छिक (2) से (12) के बीच चुने) स्थिर करें
   पूछें (जोड़ें (संख्या 1) (जोड़ें [x] (संख्या 2))) और प्रतीक्षा करें 
   यदि <(उत्तर) = ((संख्या 1) * (संख्या 2))> तो
   कहें [हाँ! :)] (2) सेकंड के लिए
   अन्यथा
   कहें [नहीं :(] (2) सेकंड के लिए
   अंत
```

\--- /hint \---

\--- /hints \---

\--- /task \---