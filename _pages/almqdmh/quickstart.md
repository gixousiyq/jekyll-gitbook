---
icon: bullseye-arrow
---

# ماهي لغة الصدأ؟

{% hint style="info" %}
أنا إنسان غير محبٍ للمقدمات التاريخية، لذلك سندخل في خضّم الموضوع مباشرةً
{% endhint %}

### تصنيف لغات البرمجة

تُصِّنف لغات البرمجة إلى قسمين، قسم منخفض المستوى؛ ويحوي لغاتًا مثل لغة التجميع (Assembly)، التي تعتبر تمثيلاً للأوامر المكتوبة بصيغة العد الثنائي (Binary) التي ينفذها المعالج؛ ممثلةً بطريقةٍ يستطيع البشر فهمها، هذا مثال لشكل كتابتها:

<figure><img src="../.gitbook/assets/image(4).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
البرنامج المكتوب أعلاه لا يعمل إلا على المعالجات المبنية بمعمارية x86، ويعمل حصراً على أنظمة التشغيل المبنية على النواة Linux مثل Ubuntu و Fedora و Android ...
{% endhint %}

ولكونها معقدة وصعبة الفهم، ولكونك تحتاج لإعادة كتابة برنامجك لكل نظام تشغيل ومعمارية معالج مختلفة، اُستحدثت لغات تسمى لغاتٍ عالية المستوى قريبة من لغة البشر، واستحدثوا أداةً جديدةً تسمى البَنّاء او المترجم (Compiler)، يترجم النصوص البرمجية القريبة من لغات البشر إلى برنامج بصيغة العد الثنائي (Binary) يحوي أوامراً يستطيع المعالج تنفيذها، أحدثت هذه اللغات ثورة في مجال الحواسيب، فهي أتاحت لك كتابة البرنامج مرة واحدة وبنصٍّ واحد ومن ثم تستطيع تشغيله على أي معمارية معالج أو أي نظام تشغيل (تقريباً 😅)، أبرز هذه اللغات وأشهرها هي لغة C، وهذا مثال لشكلها:

<figure><img src="../.gitbook/assets/image(3).png" alt=""><figcaption></figcaption></figure>

كما تلاحظ، اللغة أسهل بكثيرٍ للفهم من لغة التجميع، فبرنامجنا يبدأ التنفيذ من الدالة `()main` ، ثم يطبع كلمة `سيي` إلى الطرفية (Terminal, Console, stdout)، ويلحقها بـ `n\` التي نستخدمها لنقول للحاسوب أن السطر قد انتهى، بحيث يبدأ سطراً جديداً، ثم بعد ذلك يعيد قيمة 0 إلى نظام التشغيل التي تفيد أن البرنامج نُفِّذ بنجاحٍ دون أخطاء.

مع كونها لغةً أسهل بالفهم من لغة التجميع، لكنها ما زالت صعبة، لذلك اُستحدثت لغات ذات مستوى أعلى منها، لغات تكتب بلغة مقاربة للغة البشر بشكل أكبر بكثير، وأسهل بالتعلم لكونك لا تحتاج لأن تدير المساحة من ذاكرة الوصول العشوائي (RAM) التي يستحوذ عليها برنامجك، مما يوفر عليك الكثير من حبات البانادول.

تستخدم هذه اللغات أداة أخرى لتشغيلها تسمى المفسّر او المترجم الفوري (Interpreter)، يقرأ نصك البرمجي سطراً سطراً وينفذه بشكل متتابع، وهذا هو الفرق الجوهري بين اللغات اللتي تُبنى مثل C واللغات التي تُفسّر مثل python، حيث التي تُبنى تحول بالكامل لملف بصيغة العد الثنائي (Binary) وهو الذي يعرفه عامة الناس كملف بصيغة `exe` ؛ ينفذه المعالج مباشرةً دون تفسير، أما التي تُفَّسر او تترجم فورياً فيجب عليك وضع الملف وليكن ملفاً بصيغة `py`  المستخدم بلغة python في المترجم أو التطبيق الخاص باللغة مثل تطبيق python، الذي يقرأ برنامجك سطراً سطراً ويحوله إلى تعليمات ينفذها المعالج، هذا مثال لبرنامج كُتب بـ python:

<figure><img src="../.gitbook/assets/image(6).png" alt=""><figcaption></figcaption></figure>

كما تلاحظ اللغة لا أبسط منها 😅، وفعلياً عندما أكتب برنامجاً بها أشعر أنني أكتب نصاً باللغة الإنجليزية وليس برنامجاً

قد يقول قائل: لماذا لا نستخدم لغة الـ python البسيطة السهلة في كل برامجنا بدلاً من لغات مثل C؟ الجواب بكل بساطة يكمن في سرِّين: السرعة والصلاحية.

لغة مثل C أسرع بعشرات المرات من لغة مثل python، وقد رأيت مقارناتٍ وإحصائيات وجدت أن هنالك فرقاً في الاداء مقداره 70 مرة لصالح C، بالعربي في بعض الحالات C أسرع من python بـ 70 مرة!&#x20;

السبب الذي يجعل C صاروخاً مقارنةً بـ python هو كما قلنا سابقا لأن C تبنى مباشرةً إلى أوامر ينفذها المعالج، وتعطيك تحكماً كاملاً بالمساحة التي يحتلها برنامجك من ذاكرة الوصول العشوائي (RAM)، مما يعطيك القدرة على جعل برنامجك أصغر وأسرع ما يكون، وأيضا القدرة على احتلال الذاكرة كاملة لصالح برنامجك او إهلاك المعالج بتعليمات لا طائل منها، فهو سيف ذو حدين لكن إن استغل لصالحك بلغ مبالغً لا تتصورها

اما python فهي لغة تُفَّسر، هذا التفسير يضيف تعقيداً لها، فالمُفَّسر برنامج كسائر البرامج، يستهلك موارداً قد تكون باهظةً في بعض الأحيان، وأيضا المُفَّسر لا يعطيك الصلاحية لإدارة الحيز الذي يشغله برنامجك في ذاكرة الوصول العشوائي (RAM)، لذلك لا يصلح لبناء أنظمة التشغيل التي تطلب الوصول الكامل واللا محدود لكل موارد الجهاز، وها هنا مربط الفرس

أغلب الأنظمة الحاسوبية الحديثة تبنى بلغات مثل C و ++C ولذلك نسميهم **لغات برمجة الأنظمة**، وهذا جدول سيلخص لك كل شيء تكلمنا عنه أنفاً:



|        اللغات       | لغات برمجة الأنظمة | اللغات المُفَّسرة |
| :-----------------: | :----------------: | :---------------: |
|      **السرعة**     |     سريعة جداً     |    بطيئة نسبياً   |
| **الوصول والإدارة** |   غير مقيد (كامل)  |        مقيد       |
|  **سهولة الكتابة**  |  صعبة على المبتدئ  |        سهلة       |

{% hint style="info" %}
لغات برمجة الأنظمة: مثل ++C و C و Go و Rust ...

اللغات المُفِّسرة: مثل python و java و javascript و Lua ...
{% endhint %}

## محل الصدأ من الإعراب

هنا الزبدة والخلاصة التي كنت أمهد لها، الصدأ (Rust) لغة برمجة للأنظمة، تجمع بين سرعة C والسهولة في الكتابة والمميزات التي تريح المبرمج وطريقة كتابة النص البرمجي التي أعشقها، وأهم ما يمزيها الأمان.

الصدأ (Rust) قامت على ثغر وفجوة كانت في لغات برمجة الأنظمة، كلها كان يعيبها انعدام الأمان والصلاحية المفرطة إلى موارد الجهاز (على الرغم من وجود نظام تشغيل!) بدون محاسبة، الصدأ (Rust) يميزها مترجمها الذي ينصحك ويوجهك، من أفضل المترجمات التي تعاملت معها، لكن يعيبه أنه بطيء في البناء.

الصدأ قد تكون معقدة في البداية، لكن ريثما تتمكن منها ستعلم مدى قوتها خصوصا لو كنت قادماً من لغة مثل C .

برامج الصدأ لا تُفسّر، بل يشغلها المعالج مباشرة، مما يمنحها سرعةً جبارة