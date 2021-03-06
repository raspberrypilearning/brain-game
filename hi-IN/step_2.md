## प्रश्न बनाना

आइए हम खिलाड़ी द्वारा उत्तर देने के लिए यादृच्छिक प्रश्न बनाने से शुरू करते हैं।



+ नया Scratch प्रोजेक्ट प्रारंभ करें, और कैट स्प्राइट हटाएं, ताकि आपका प्रोजेक्ट खाली हो। आप <a href="http://jumpto.cc/scratch-new" target="_blank">jumpto.cc/scratch-new</a> पर ऑनलाइन Scratch एडिटर खोज सकते हैं।

+ अपनी गेम के लिए कैरेक्टर और बैकड्रॉप चुनें। आप अपनी पसंद की कोई भी चुन सकते हैं! उदाहरण इस प्रकार है:

	![screenshot](images/brain-setting.png)

+ `number 1`{:class="blockdata"} (नंबर 1) और `number 2`{:class="blockdata"} (नंबर 2) नामक 2 चर बनाएँ। ये चर 2 संख्याओं को स्टोर करेंगे जिन्हें साथ-साथ गुणा किया जाएगा।

	![screenshot](images/brain-variables.png)

+ इन दोनों चरों को 2 और 12 के मध्य `क्रमरहित`{:class="blockoperators"} संख्या पर सेट करने के लिए, अपने कैरेक्टर पर कोड जोड़ें।

	```blocks
		जब ⚑ क्लिक किया गया हो
		[number 1 v] पर ((2) से (12) तक क्रमरहित चुनने) सेट करे
		[number 2 v] पर ((2) से (12) तक क्रमरहित चुनने) सेट करे
	```

+ आप फिर खिलाड़ी से उत्तर की मांग कर सकते हैं, और उन्हें बता सकते हैं कि वे सही हैं या गलत।

	```blocks
		जब ⚑ क्लिक किया गया हो
		[number 1 v] पर ((2) से (12) तक क्रमरहित चुनने) सेट करे
		[number 2 v] पर ((2) से (12) तक क्रमरहित चुनने) सेट करे
		((number 1) ([x] (number 2) जोड़े) जोड़े) जोङें अौरइंतजार करे
		अगर <(जवाब) = ((number 1) * (number 2))> हो तो
end
			[हाँ! :)] सेकंड तक (2) बोले
		या
			[नहीं :(] सेकंड तक (2) बोले
		end
	```

+ एक प्रश्न का सही ढंग से उत्तर देकर और एक का गलत उत्तर देकर, अपने प्रोजेक्ट की पूरी तरह से जांच करें।

+ इस कोड के चारों आसपास `हमेशा के लिए`{:class="blockcontrol"} लूप जोड़ें, ताकि खिलाड़ी से बहुत-सारे प्रश्न पूछे जा सकें।

+ `समय`{:class="blockdata"} नामक चर का उपयोग करके, स्टेज पर काउंटडाउन टाइमर बनाएँ। यदि आपको सहायता चाहिए तो 'घोस्टबस्टर्स' प्रोजेक्ट में (चरण 5 में) टाइमर बनाने के निर्देश दिए गए हैं!

+ अपने प्रोजेक्ट का पुनः परीक्षण करें - आपको समय समाप्त होने तक प्रश्न पूछने में सक्षम होना चाहिए।



