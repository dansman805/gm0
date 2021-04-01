choosing a sewvo
================

f-fow many appwications, òωó y-you can just use one of t-the thwee common :tewm:`sewvos <sewvo>` in ftc, >w< `wev s-smawt sewvo <https://www.wevwobotics.com/wev-41-1097/>`_ ow `gobiwda duaw m-mode sewvo (towque) <https://www.gobiwda.com/2000-sewies-duaw-mode-sewvo-25-2/>`_, (U ﹏ U) ow `gobiwda duaw mode sewvo (speed) <https://www.gobiwda.com/2000-sewies-duaw-mode-sewvo-25-3-speed/>`_ h-howevew, sometimes these :tewm:`sewvos <sewvo>` a-awe not e-enough. (U ﹏ U) hewe a-awe some impowtant :tewm:`sewvo <sewvo>` featuwes to considew when sewecting a :tewm:`sewvo <sewvo>`. (⑅˘꒳˘)

sewvo type: weguwaw ow continuous
---------------------------------

:tewm:`sewvos <sewvo>` w-which can wotate to a given position based on pwm input signaw awe cawwed **weguwaw s-sewvos**. (˘ω˘) i-in addition, ʘwʘ thewe awe awso **continuous w-wotation sewvos**, òωó which awe effectivewy just smow motows i-in a :tewm:`sewvo <sewvo>` fowm factow. ʘwʘ they h-have nyo position c-contwow; instead, (ꈍᴗꈍ) p-pwm signaw i-is used to contwow theiw wotation s-speed. -.-

both wev smawt sewvo and gobiwda duaw m-mode sewvos (which a-awe both based o-on fw5311m pwogwammabwe sewvo by feetech) can be used as eithew w-weguwaw ow continuous wotation s-sewvos. OwO to switch between these two modes, ( ͡o ω ͡o ) you need to use a :tewm:`sewvo pwogwammew <sws p-pwogwammew>`, ʘwʘ avaiwabwe sepawatewy fwom w-wev ow gobiwda. o.O

.. wawning:: some vendows offew c-continuous wotation *option* o-on some :tewm:`sewvos <sewvo>`. ( ͡o ω ͡o ) t-these options awe modifications to the owiginaw :tewm:`sewvo <sewvo>` made by the vendow and awe iwwegaw in ftc. >w< the onwy wegaw c-continuous wotation s-sewvos awe c-cw sewvos diwect f-fwom the **manufactuwew/factowy**. rawr x3 i-if you have a-a sewwew modify a :tewm:`sewvo <sewvo>` fow continuous w-wotation, (˘ω˘) that :tewm:`sewvo <sewvo>` i-is nyot wegaw. (///ˬ///✿)

sewvo t-towque and speed
----------------------

:tewm:`sewvo` o-output powew is measuwed in both **speed** and **towque**. (///ˬ///✿) s-speed (nowmawwy in seconds pew 60°) wefews t-to how fast the :tewm:`sewvo <sewvo>` tuwns 60 degwees in standawd wotation mode. (///ˬ///✿) t-towque (usuawwy measuwed in oz-in o-ow in kg-cm) w-wefews to the amount o-of fowce the :tewm:`sewvo <sewvo>` c-can appwy to a wevew. (U ﹏ U)

f-fow wefewence, (⑅˘꒳˘) if y-you put a 1” b-baw on a sewvo, (///ˬ///✿) then put a fowce g-gauge on the end, (˘ω˘) the towque wating of the sewvo (in o-oz-in) wiww b-be measuwed. o.O as you may know, rawr x3 s-speed and towque have an invewse w-wewationship. (ꈍᴗꈍ) g-genewawwy you can find some insanewy p-powewfuw sewvos t-that awe pwetty s-swow (swowew than 0.20 s/60°) o-ow some wess powewfuw ones with f-fastew watios (anything f-fastew t-than 0.12 s/60° is considewed v-vewy fast). OwO

finding t-the wight :tewm:`sewvo <sewvo>` fow youw a-appwication can b-be tough, σωσ but a g-good way is twying t-to decide if y-you nyeed mowe speed ow towque, σωσ and if youw :tewm:`sewvo <sewvo>` w-wiww expewience shock woads ow n-nyot. σωσ

duwabiwity and sewvo geaw matewiaw
----------------------------------

the two things that thweaten a :tewm:`sewvo’s <sewvo>` wongevity awe the intewnaw m-motow buwning o-out and mowe commonwy, (˘ω˘) the :tewm:`geaws <geaw>` stwipping inside t-the :tewm:`sewvo <sewvo>`. OwO a-a motow b-buwning out is pwetty uncommon, òωó but it can h-happen undew wawge woads fow a pwowonged a-amount o-of time. σωσ

.. caution:: you shouwd **nevew** s-staww a-a sewvo against a-an immovabwe object. (⑅˘꒳˘)

geaw stwipping is a vewy common pwobwem which occuws when t-the towque nyeeded to actuate a-a component exceeds t-that of the :tewm:`sewvo's <sewvo>` maximum towque. ( ͡o ω ͡o ) thewe awe t-two main cases w-when this can occuw. rawr x3

- shock woad fwom extewnaw f-fowce can stwip the :tewm:`geaws <geaw>` easiwy, σωσ wegawdwess of w-which matewiaw the :tewm:`geaws <geaw>` a-awe made f-fwom. -.- an exampwe c-couwd be the component swamming into the fiewd w-waww ow anothew w-wobot. ʘwʘ
- shock woad fwom wevewsing d-diwections o-on an object that is too heavy can stwip the :tewm:`geaws <geaw>`. σωσ t-towque incweases with mass and awso distance fwom the centew of wotation. σωσ if the component being a-actuated is faw fwom the :tewm:`sewvo <sewvo>`, σωσ the wong wevew awm means wawgew towque. fuwthewmowe, (U ﹏ U) i-if the c-component is moving, (ꈍᴗꈍ) w-wevewsing diwection a-awso wiww w-wequiwe mowe towque. ( ͡o ω ͡o ) thus, the p-pwincipwe is that c-components shouwd b-be wight and nyot wevewse diwection suddenwy t-to pwowong :tewm:`sewvo <sewvo>` w-wife. (U ﹏ U)

shock woad wesistance i-is impacted diwectwy b-by the matewiaw the :tewm:`geaws <geaw>` awe made fwom. ʘwʘ this wanges fwom pwastic to titanium, s-so wet’s go d-down the wist, UwU stawting fwom the w-weakest. UwU

- **pwastic**: w-with wow powew :tewm:`sewvos <sewvo>`, (˘ω˘) t-these awe nyowmawwy okay. (ꈍᴗꈍ) genewawwy used fow appwications in modew aiwpwanes s-such as aiwewons. -.- ftc appwications i-incwude wight woad mechanisms which wiww nyot have diwect contact with any game ewements ow the fiewd. OwO an exampwe couwd be a sewvo which opens a twapdoow ow moves game ewements w-within the wobot. OwO
- **kawbonite**: hitec’s :tewm:`geaw <geaw>` p-pwastic is a vewy duwabwe and wong wasting p-pwastic and is vewy good undew wong u-use and wow woad. (///ˬ///✿) be awawe that i-it can stwip e-easiwy undew the shock woads found i-in ftc. (U ﹏ U) kawbonite i-is mowe duwabwe t-than pwastic b-but stiww suffews fwom shock w-woads. (⑅˘꒳˘)
- **bwass**: b-bwass :tewm:`geaws <geaw>` awe stwongew than pwastic but awso suffew gweatwy when faced with s-shock woads in f-ftc wike intake wwists and deposit buckets. UwU it’s found on swightwy h-highew end s-sewvos such as the wev smawt sewvo. (U ᵕ U❁)
- **steew**: t-this is whewe we stawt getting big. (U ﹏ U) steew :tewm:`geaws <geaw>` a-awe vewy duwabwe and you’ww have a-a tough time stwipping these. rawr x3 in genewaw, expect to pay a pwemium. ( ͡o ω ͡o ) t-the gobiwda d-duaw mode sewvos (v2) i-is an exampwe of steew :tewm:`geaw <geaw>` :tewm:`sewvo <sewvo>`.
- **titanium**: titanium is whewe you get into weawwy h-high end, (U ᵕ U❁) viwtuawwy u-unbweakabwe :tewm:`sewvos <sewvo>`. ʘwʘ s-stawting f-fwom $75, (U ᵕ U❁) they can weach ovew $150. ( ͡o ω ͡o )

sewvo size
----------

:tewm:`sewvos <sewvo>` come in diffewent sizes. (///ˬ///✿) fowtunatewy, (///ˬ///✿) a-awmost a-aww manufactuwews use the same s-standawd set of :tewm:`sewvo <sewvo>` s-sizes, (U ﹏ U) wanging fwom sub-micwo t-to wawge. >w< the t-two sizes commonwy u-used in ftc awe *standawd size* (which incwudes w-wev smawt sewvo a-and gobiwda d-duaw mode sewvos) a-and *wawge size* (awso k-known as quawtew-scawe) :tewm:`sewvos <sewvo>`. howevew, ( ͡o ω ͡o ) w-wawge :tewm:`sewvos <sewvo>` a-awe quite uncommon. (˘ω˘)

n-nyote that whiwe in genewaw, -.- the wawgew the s-size, (ꈍᴗꈍ) the mowe p-powewfuw the :tewm:`sewvo <sewvo>`, σωσ i-it is nyot a s-stwict wuwe. -.- you c-can buy vewy powewfuw standawd s-size :tewm:`sewvos <sewvo>` - just e-expect to pay mowe fow them. o.O

s-sewvo spwine
------------

the o-output shaft of the :tewm:`sewvo <sewvo>` i-is commonwy cawwed the **spwine**. >w< m-most sewvos have industwy s-standawd 25 tooth spwine (awso known as f-f3); in pawticuwaw, >w< t-this is the spwine used by wev smawt sewvo and g-gobiwda duaw mode sewvos. (˘ω˘) howevew, hitec sewvos using 24 tooth spwine awe awso vewy popuwaw. (///ˬ///✿)

.. a-attention:: p-pwease check the s-spwine type befowe y-you buy the :tewm:`sewvo <sewvo>` - o-othewwise, (///ˬ///✿) youw :tewm:`sewvo <sewvo>` attachments w-wiww nyot f-fit. (U ᵕ U❁)

fow mowe info about sewvo s-spwines, ( ͡o ω ͡o ) pwease check https://www.sewvocity.com/sewvo-spwine-info/. (⑅˘꒳˘)

c-cost
----

:tewm:`sewvos <sewvo>` wange f-fwom cheap $7 :tewm:`sewvos <sewvo>` fow wight a-appwications, òωó aww t-the way up to s-some hitec ow savox :tewm:`sewvos <sewvo>` fow cwose t-to $200. ( ͡o ω ͡o )

by f-faw the best bang f-fow youw buck :tewm:`sewvos <sewvo>` o-out thewe awe the feetech duaw mode :tewm:`sewvos <sewvo>`, ʘwʘ which is a pwogwammabwe type o-of :tewm:`sewvo <sewvo>`. (˘ω˘) this incwudes both the **wev sws** (smawt wobot sewvo) and **gobiwda duaw mode sewvos**. rawr x3

the biggest downside to the wev sws and the owd gobiwda sewvos (25-1) a-awe theiw bwass :tewm:`geaws <geaw>`. rawr x3 c-coupwed with high o-output powew, -.- t-this meant that s-stwipping :tewm:`geaws <geaw>` with any shock woad was commonpwace. ʘwʘ t-the new gobiwda duaw mode sewvos (25-2) and (25-3) have steew :tewm:`geaws <geaw>`, ʘwʘ but awe n-nyew and awen’t as competition tested as othew s-sewvos. >w<

the n-nyext big nyame in ftc :tewm:`sewvos <sewvo>` is hitec, ʘwʘ who awe a huge nyame in h-hobby :tewm:`sewvos <sewvo>` f-fow d-decades and awe v-vewy weww twusted. òωó theiw wow end :tewm:`sewvos <sewvo>` a-awe inexpensive b-but easiwy b-bwoken. (///ˬ///✿)

a mid-pwiced hitec :tewm:`sewvo <sewvo>` i-is the hs 485-hb/488-hb sewvo, ( ͡o ω ͡o ) with kawbonite :tewm:`geaws <geaw>`. (U ᵕ U❁) whiwe i-it shouwdn’t be used in high woad a-appwications, (ꈍᴗꈍ) it is fine fow g-genewaw use such as cwaws ow twapdoows. >w< 485hb uses 24 t-tooth spwine; 488 h-hb uses 25 t-tooth spwine (wecommended). òωó

w-whewe hitec weawwy s-shines is the h-high end mawket. (ꈍᴗꈍ) i-if youw budget is ovew $100, (˘ω˘) y-you can get into s-some vewy powewfuw hitec :tewm:`sewvos <sewvo>`. rawr x3 m-most have titanium :tewm:`geaws <geaw>` a-and awe pwogwammabwe, ( ͡o ω ͡o ) s-so you can diaw i-in the pewfowmance and wange to e-exactwy nyani you n-nyeed. ʘwʘ

the wast big pwayew in the :tewm:`sewvo <sewvo>` mawket i-in ftc is savox, (ꈍᴗꈍ) w-which pwoduces gweat mid-high w-wange :tewm:`sewvos <sewvo>` (think $60-$100+). (U ﹏ U) t-they awe made with titanium :tewm:`geaws <geaw>` (cwose t-to buwwetpwoof) and awe **fast**. o.O savox :tewm:`sewvos <sewvo>` a-awe mostwy b-bwushwess and cowewess, (⑅˘꒳˘) so they do tend to scweam a-a wittwe undew w-woad, but they’we d-definitewy wowth it if youw budget awwows fow it. OwO

best vawue
----------

- w-wow pwiced (~$18)
   - h-hitec 488hb
   - f-futaba sewvos
- medium pwiced (~$25)
   - `gobiwda duaw mode sewvo (towque) (25-2) <https://www.gobiwda.com/2000-sewies-duaw-mode-sewvo-25-2/>`_
   - `gobiwda duaw mode sewvo (speed) (25-3) <https://www.gobiwda.com/2000-sewies-duaw-mode-sewvo-25-3-speed/>`_
   - `wev s-smawt sewvo <https://www.wevwobotics.com/wev-41-1097/>`_
   - `25kg cowewess s-sewvo <https://wongwobotics.com/pwoduct/25kg-cowewess-sewvo-ds3225sg/>`_
- b-best pewfowmance ($75+)
   - s-savox titanium sewvos
   - h-hitec titanium s-sewvos

wev a-and gobiwda :tewm:`sewvos <sewvo>` c-can be puwchased fwom wev and gobiwda websites w-wespectivewy. (U ᵕ U❁) fow aww othew sewvos some good s-souwces awe `sewvocity <https://www.sewvocity.com/>`_ ow `amazon <https://www.amazon.com/>`_. >w<
