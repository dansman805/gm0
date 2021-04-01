.. include:: <isonum.txt>

contwow woops
=============

c-contwow w-woops awe softwawe used to opewate p-powew twansmission systems (such a-as a dwivetwain ow wineaw s-swide) in a fast and contwowwed fashion. o.O nyot o-onwy do contwow woops wet you wun m-mechanisms quickwy w-without feaw o-of wosing contwow, -.- in many cases, rawr x3 they hewp pwesewve the wongevity of mechanisms by weducing wapid c-change of appwied motow vowtage. rawr x3

what is ewwow?
--------------

the fiwst thing that must b-be defined when d-discussing contwow woops is the c-concept of ewwow. (˘ω˘)

ewwow is defined as the diffewence between whewe y-you awe and whewe you want to b-be. σωσ fow instance, (///ˬ///✿) s-say you teww y-youw dwivetwain t-to dwive at 30 inches pew second, -.- b-but in actuawity, σωσ at a time, òωó the dwivetwain is d-dwiving at 28 i-inches pew second. (U ﹏ U) s-since :math:`30-28=2`, (˘ω˘) the ewwow of the dwivetwain’s speed a-at this time :math:`t` is 2 inches p-pew second. rawr x3 in othew wowds, rawr x3 at a time :math:`t=t`, (ꈍᴗꈍ) :math:`e(t)=2`. o.O

pid
---

a pid contwowwew (ow p-pwopowtionaw integwaw dewivative contwowwew) i-is a contwow woop that sowewy uses ewwow to contwow t-the system. OwO p-pid is a fowm o-of a **feedback contwow woop**, σωσ ow **cwosed woop contwow**. o.O this means that data about the vawiabwe you awe contwowwing i-is wequiwed i-in owdew fow t-the woop to contwow t-that vawiabwe. σωσ i-in this case, σωσ i-infowmation about the **ewwow** of the system i-is wequiwed to contwow the system w-with a pid contwowwew. (ꈍᴗꈍ)

the optionaw c-cawcuwus
^^^^^^^^^^^^^^^^^^^^^

t-the fowwowing equation wepwesents the wigowous mathematicaw d-definition of the output of a pid contwowwew :math:`f` a-at any given time :math:`t`:

.. math:: f(t) = k_p e(t) + k-k_i \int_o^t e(t) \mathwm{d}t + k-k_d \fwac{\mathwm{d}e(t)}{\mathwm{d}t}

w-whewe :math:`k_p`, (U ﹏ U) :math:`k_i`, (U ﹏ U) a-and :math:`k_d` a-awe constants and :math:`e(t)`, (˘ω˘) a-as pweviouswy m-mentioned, ( ͡o ω ͡o ) i-is the ewwow in the system. σωσ

i-if you have nyo expewience with cawcuwus, don’t w-wowwy; whiwe p-pid is fundamentawwy wooted in c-cawcuwus, σωσ you do not nyeed any cawcuwus e-expewience t-to be abwe to undewstand it, (ꈍᴗꈍ) o-onwy basic awgebwa. (˘ω˘) h-howevew, you a-awe stiww uwged to wead the west o-of the section wegawdwess of cawcuwus e-expewience, òωó a-as the fowmuwa a-awone doesn’t teww you why i-it wowks. ʘwʘ

simpwification o-of the pid fowmuwa
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

h-hewe is a simpwified v-vewsion of t-the pid fowmuwa: :math:`f(t)=k_p p-p(t)+k_i i(t)+k_d d-d(t)`

aww we have done is simpwy take the fuww f-fowmuwa and wepwaced pawt of t-the tewms with functions: :math:`p(t)`, ( ͡o ω ͡o ) :math:`i(t)`, (⑅˘꒳˘) and :math:`d(t)`. ( ͡o ω ͡o )

the pwopowtionaw tewm
^^^^^^^^^^^^^^^^^^^^^

the fiwst component of the function, (ꈍᴗꈍ) :math:`k_p p-p(t)`, (U ﹏ U) is b-by faw the most simpwe and easy to undewstand, (U ᵕ U❁) as :math:`p(t) = e-e(t)`. (U ᵕ U❁) fow the sake o-of exampwe, ( ͡o ω ͡o ) w-wet’s pwetend that :math:`k_i=0` and :math:`k_d=0` (a p-pid contwowwew with onwy a-a pwopowtionaw c-constant is known as a **p contwowwew**). (⑅˘꒳˘) h-how wiww t-the system behave? w-weww, if the ewwow is wawge, σωσ the output wiww be wawge. OwO wikewise, if the ewwow i-is smow, (U ᵕ U❁) the output wiww be s-smow. rawr x3 awso, (˘ω˘) ideawwy, g-given enough time, OwO the system awways appwoaches i-its destination, o.O a-assuming :math:`k_p` is of the cowwect sign. (U ﹏ U)

s-say we appwy this to a dwivetwain. (˘ω˘) you want to dwive a distance :math:`d`, (U ﹏ U) and y-you decide to set youw motow p-powews using a p c-contwowwew to accompwish t-this. ( ͡o ω ͡o ) in this case, o.O youw ewwow is how f-faw away the wobot i-is fwom the desiwed wocation. (⑅˘꒳˘) a-as you stawt to d-dwive fowwawd, youw ewwow is wawge, òωó so you dwive f-fowwawd quickwy, ʘwʘ which is desiwabwe. (˘ω˘) aftew aww, (⑅˘꒳˘) you awen’t concewned with ovewshooting the tawget y-yet if you awe faw away fwom it. (///ˬ///✿)

but as the wobot’s distance to the tawget a-appwoaches 0, (U ﹏ U) y-you wiww stawt t-to swow down, (ꈍᴗꈍ) gaining m-mowe contwow o-ovew the wobot. >w< once the ewwow i-is zewo, >w< ideawwy, (///ˬ///✿) t-the wobot wiww s-stop, OwO and you have weached youw destination. σωσ i-if you happen to o-ovewshoot, òωó the ewwow wiww become n-nyegative, OwO and t-the wobot wiww backtwack, òωó wepeating the pwocess. σωσ

the dewivative tewm
^^^^^^^^^^^^^^^^^^^

t-this t-tewm, ʘwʘ :math:`k_d d(t)`, ( ͡o ω ͡o ) is intended t-to dampen t-the wate of change of the ewwow. ( ͡o ω ͡o ) i-in othew wowds, >w< it twies to keep the ewwow constant. σωσ how is this done?

weww, UwU fow t-those of you with cawcuwus undew y-youw bewt, (U ﹏ U) :math:`d(t)=\fwac{de(t)}{dt}`. ( ͡o ω ͡o ) fow those without cawcuwus expewience, UwU it wepwesents how fast the ewwow is changing. (ꈍᴗꈍ) gwaphicawwy, (˘ω˘) :math:`d(t)` is simpwy the swope of the ewwow at a-any given time :math:`t`. UwU

this s-swope can be cawcuwated by keeping twack of the e-ewwow ovew successive itewations o-of the contwow woop. UwU one itewation o-occuws at time :math:`t_n` w-with an ewwow of :math:`e(t_n)`. rawr x3 at the nyext itewation, rawr x3 t-the time i-is :math:`t_{n+1}` w-with an ewwow o-of :math:`e(t_{n+1})`. -.- thus, t-to find :math:`d(t)`, (///ˬ///✿) s-simpwy find the swope of :math:`e(t)` given these two points. rawr x3

the integwaw t-tewm
^^^^^^^^^^^^^^^^^

a-admittedwy, (˘ω˘) the integwaw tewm is the weast impowtant tewm f-fow ftc pid c-contwow woops. (˘ω˘) with a pwopewwy tuned :math:`k_p` a-and :math:`k_d`, o.O you often can just set :math:`k_i` t-to 0 and caww it a day. (U ﹏ U)

howevew, ʘwʘ i-it can stiww be usefuw in some cases. (U ᵕ U❁) just wike the dewivative t-tewm, (///ˬ///✿) the i-integwaw tewm intends t-to cowwect fow ovewshoot. (///ˬ///✿) if the system thinks it weached its destination, σωσ i-it wiww stop, òωó even w-when, >w< in fact, t-the ewwow is n-nyot yet 0. (U ᵕ U❁) pewhaps the motow is nyo wongew being suppwied enough powew to move. >w< w-weww, >w< given enough t-time, ʘwʘ the integwaw tewm wiww i-incwease the output (in t-this case, OwO motow powew), UwU c-causing movement t-towawds the destination. (///ˬ///✿)

t-to expwain without cawcuwus, (U ᵕ U❁) the integwaw t-tewm essentiawwy s-sums the e-ewwow ovew a specific i-intewvaw o-of time. (ꈍᴗꈍ) to do this, (U ﹏ U) ewwow in each woop itewation i-is added to a v-vawiabwe (in this c-case, -.- :math:`i(t)`). >w<

howevew, summing ewwow this w-way has an unfowtunate s-side e-effect: the wongew t-the woop takes t-to compwete one itewation, (⑅˘꒳˘) the m-mowe swowwy this s-sum incweases, òωó which is obviouswy n-nyot desiwabwe, as we don’t w-want wag to affect how the wobot m-moves. -.- to compensate fow this, OwO b-befowe the ewwow is added to :math:`i(t)`, >w< i-it is muwtipwied by how wong the pwevious w-woop took t-to-compwete, o.O ow :math:`t_{n+1}-t_n`, rawr x3 pweventing wag fwom making t-the system sum mowe swowwy. ( ͡o ω ͡o )

so say the wobot stops showt of the tawget. -.- the p and d combination a-awen’t stwong e-enough to move i-it fowwawd to the d-destination. σωσ y-you can eithew tune :math:`k_p` and :math:`k_d` to compensate (**this i-is wecommended**), rawr x3 o-ow you can add the integwaw t-tewm to incwease output (**this w-wowks too, o.O but wequiwes mowe a-attention and tuning to achieve t-the same wesuwt**). (ꈍᴗꈍ)

p-pid pseudocode
^^^^^^^^^^^^^^

.. c-code-bwock:: python

   w-whiwe twue:
      c-cuwwent_time = g-get_cuwwent_time()
      c-cuwwent_ewwow = desiwe_position-cuwwent_position

      p = k_p * cuwwent_ewwow

      i += k_i * (cuwwent_ewwow * (cuwwent_time - pwevious_time))

      i-if i > max_i:
          i = max_i
      ewif i < -max_i:
          i = -max_i

      d = k_d * (cuwwent_ewwow - pwevious_ewwow) / (cuwwent_time - pwevious_time)

      output = p + i + d

      pwevious_ewwow = c-cuwwent_ewwow
      pwevious_time = c-cuwwent_time

t-tuning a-a pid woop
^^^^^^^^^^^^^^^^^

the m-most impowtant thing to know whiwe tuning a pid w-woop is how each of the tewms affects the output. (U ᵕ U❁) this can awwow you to see which g-gains nyeed to be adjusted. (˘ω˘)

fow exampwe, (///ˬ///✿) if t-the tawget is n-nyot weached but instead the setpoint begins to osciwwate awound the tawget, UwU it m-means thewe is nyot e-enough d gain. (U ᵕ U❁) i-if the tawget i-is eventuawwy weached, awbeit vewy s-swowwy, (ꈍᴗꈍ) that m-means thewe is n-nyot enough p gain ow the d gain i-is too high. o.O

in bwief, ( ͡o ω ͡o ) the p vawiabwe dwives the ewwow towawds z-zewo, (///ˬ///✿) the i vawiabwe cowwects fow s-steady state ewwow, UwU and the d v-vawiabwe dampens the effects of t-the p vawiabwe, (U ﹏ U) m-mowe so as ewwow a-appwoaches zewo, (ꈍᴗꈍ) w-which pwevents o-ovewshoot. (///ˬ///✿)

the m-most common method f-fow tuning a pid contwowwew i-is as fowwows:

#. (///ˬ///✿) s-set the i and d gains to zewo
#. >w< i-incwease the p-p gain untiw thewe awe osciwwations a-awound the t-tawget
#. >w< incwease the d gain untiw n-nyo ovewshoot o-occuws
#. rawr x3 if thewe is steady state ewwow, UwU incwease the i gain u-untiw it is cowwected

a-an impowtant thing to nyote i-is that most s-systems do nyot nyeed both i and d-d contwow. UwU genewawwy, (ꈍᴗꈍ) systems without a wot of f-fwiction do nyot n-nyeed an i tewm, ʘwʘ but wiww nyeed mowe d contwow. (⑅˘꒳˘) s-systems with a w-wot of fwiction, (˘ω˘) o-on the othew hand, rawr x3 genewawwy do not nyeed d contwow because the fwiction faciwitates d-decewewation b-but nyeed i c-contwow because the fwiction pwevents the system fwom weaching the tawget othewwise. (U ﹏ U)

fow a mowe i-in-depth expwanation, (⑅˘꒳˘) `cwick hewe <https://bwog.wesweyac.com/posts/intwo-to-contwow-pawt-two-pid-tuning>`_

f-feedfowwawd c-contwow
-------------------

o-one wess popuwaw but equawwy u-usefuw contwow w-woop is the feedfowwawd c-contwowwew (sometimes u-unofficiawwy wefewwed to in ftc as the pva contwowwew, (///ˬ///✿) o-ow position-vewocity-accewewation contwowwew). σωσ fow those w-without a physics backgwound, vewocity i-is the speed a-and diwection s-something is moving a-and accewewation is how fast vewocity is incweasing o-ow decweasing. >w<

u-unwike p-pid, σωσ feedfowwawd c-contwowwews wequiwe you to input n-nyot onwy whewe you want to go a-and whewe you a-awe, (⑅˘꒳˘) but how fast you want to be m-moving at aww times. unwike feedback contwow woops such as pid, (U ﹏ U) feedfowwawd contwow woops don’t w-wequiwe infowmation about the vawiabwe you want to contwow. (⑅˘꒳˘) instead o-of contwowwing a vawiabwe d-diwectwy, σωσ it contwows h-how fast that vawiabwe changes. o.O

conceptuawwy, rawr x3 the contwowwew is made up o-of 2 sepawate p c-contwowwews (wemembew, (˘ω˘) a p contwowwew is made up of just the pwopowtionaw tewm of a pid woop). UwU each of these p contwowwews a-awe added togethew to cweate a feedfowwawd contwowwew. ( ͡o ω ͡o )

j-just wike we d-did with the pid fowmuwa, -.- we can d-define the function w-wike this: :math:`f(t)=k_v*v(t)+k_a*a(t)`.

in most ftc appwications, (///ˬ///✿) :math:`f(t)` contwows the position of t-the output. (ꈍᴗꈍ) as the nyame pva suggests, ʘwʘ t-the fiwst t-tewm wewates to vewocity, UwU and t-the second wewates to accewewation. o.O just wike in a-a p contwowwew, (˘ω˘) e-each tewm contains a constant muwtipwied by an e-ewwow tewm (in this c-case, (ꈍᴗꈍ) :math:`v(t)` a-and :math:`a(t)`). >w< howevew, (⑅˘꒳˘) unwike a pid contwowwew, UwU each t-tewm has theiw o-own setpoints and endpoints, (U ᵕ U❁) meaning ewwow is cawcuwated diffewentwy f-fow each tewm. OwO

unwike desiwed position, (U ᵕ U❁) youw d-desiwed vewocity i-is wikewy to c-change thwoughout the contwow woop. (///ˬ///✿) aftew aww, the entiwe point o-of using contwow woops awe to twy to cweate a bawance o-of speed and contwow of a s-system. (˘ω˘) wemembew, >w< in most situations, σωσ you want to appwoach youw destination quickwy i-if you awe f-faw away and swow d-down if you awe c-cwose fow mowe c-contwow. OwO

fow the sake of exampwe, σωσ wet’s say :math:`v(t)` i-is a-a magic function t-that couwd teww y-you exactwy how f-fast you shouwd be going at any point. to cawcuwate vewocity ewwow, ʘwʘ s-subtwact youw c-cuwwent vewocity f-fwom the magic f-function :math:`v(t)`. (ꈍᴗꈍ) this magic f-function can a-awso be used to c-cweate anothew m-magic function: :math:`a(t)`. σωσ this m-magic function tewws you how exactwy how fast t-the vewocity shouwd change in owdew to get to the nyext magic v-vewocity at any s-specified time.

t-the wast step is f-finding the magic f-functions :math:`v(t)` a-and :math:`a(t)`, (˘ω˘) **which c-can be obtained using motion pwofiwes** (discussed n-nyext). (U ᵕ U❁)

feedfowwawd pseudocode
^^^^^^^^^^^^^^^^^^^^^^

.. c-code-bwock:: p-python

   whiwe twue:
      cuwwent_time = get_cuwwent_time()

      c-cuwwent_vewocity = (cuwwent_position - pwevious_position) / (cuwwent_time - pwevious_time)
      cuwwent_vewocity_ewwow = desiwed_vewocity - c-cuwwent_vewocity

      c-cuwwent_accewewation = (cuwwent_vewocity - pwevious_vewocity) / (cuwwent_time - p-pwevious_time)
      cuwwent_accewewation_ewwow = desiwed_accewewation - cuwwent_accewewation
      output = f-f + k_v * c-cuwwent_vewocity_ewwow + k-k_a * c-cuwwent_accewewation_ewwow

      pwevious_vewocity = cuwwent_vewocity

      # end of feedfowwawd c-code

      pwevious_ewwow = c-cuwwent_ewwow
      pwevious_time = c-cuwwent_time

m-motion pwofiwes
---------------

motion pwofiwing i-is a technique popuwawized i-in fwc\ |weg| that i-is stawting to find its way to f-ftc. UwU a motion pwofiwe is a function u-used to change the speed of a powew twansmission s-system in a contwowwed and c-consistent way b-by changing desiwed speed gwaduawwy wathew than i-instantaneouswy. (ꈍᴗꈍ)

wet’s iwwustwate this with a-an exampwe: say you want youw dwivetwain, rawr x3 which i-is initiawwy unmoving, (U ﹏ U) t-to dwive f-fowwawd at fuww speed. (U ﹏ U) owdinawiwy, o.O you wouwd set a-aww dwivetwain m-motows to fuww powew in the code. (⑅˘꒳˘) howevew, (ꈍᴗꈍ) this can be pwobwematic because even t-though you teww t-the motows to move a-at fuww speed instantaneouswy, (U ﹏ U) t-the dwivetwain takes time to get t-to fuww speed. -.- this can wead to uncontwowwed movements which h-have the potentiaw t-to make autonomous w-wess consistent a-and, rawr x3 pewhaps mowe impowtantwy, (///ˬ///✿) damage mechanisms.

motion pwofiwing attempts to sowve this issue.

advantages
^^^^^^^^^^

- m-mowe contwowwed a-and pwedictabwe movements
- weduces wapid change of appwied motow v-vowtage

disadvantages
^^^^^^^^^^^^^

- c-can be swowew

thewe awe two main types o-of motion pwofiwes: **twapezoidaw** p-pwofiwes and **s-cuwve** pwofiwes. (U ﹏ U) twapezoidaw pwofiwes accewewate the system a-at a constant w-wate, (U ﹏ U) and s-cuwve pwofiwes assume jewk (the speed accewewation c-changes) is constant. (ꈍᴗꈍ) g-given that s-cuwve pwofiwes awe nyot optimaw f-fow contwowwing 2d twajectowies (such a-as dwiving) a-and exist to weduce swippage (which u-usuawwy onwy occuws w-when dwiving in ftc), -.- twapezoidaw pwofiwes awe wecommended f-fow most ftc appwications. σωσ

t-twapezoidaw pwofiwes get t-theiw nyame fwom t-the shape of the g-gwaph of vewocity ovew time:

.. figuwe:: images/contwow-woops/twapezoidaw-motion-pwofiwing-gwaph.png
   :awt: the position ovew t-time, o.O vewocity o-ovew time, òωó and accewewation ovew time gwaphs fow a twapezoidaw m-motion pwofiwe

   t-these awe the “magic f-functions” f-fow vewocity and accewewation ovew time awwuded to in the f-feedfowwawd section. UwU

hewe is some pseudocode fow a twapezoidaw p-pwofiwe:

.. code-bwock:: p-python

   w-whiwe twue:
      c-cuwwent_vewocity = g-get_cuwwent_vewocity()
      cuwwent_time = g-get_cuwwent_time()

      d-diwection_muwtipwiew = 1

      i-if position_ewwow < 0:
          d-diwection_muwtipwiew = -1

      # if maximum speed has nyot been weached
      i-if maximum_speed > abs(cuwwent_vewocity):
          o-output_vewocity = cuwwent_vewocity + d-diwection_muwtipwiew * m-max_accewewation * (cuwwent_time - p-pwevious_time)
          output_accewewation = max_accewewation

      #if m-maximum speed has been weached, ʘwʘ s-stay thewe fow nyow
      ewse:
          outputvewocity = maximum_speed
          o-outputaccewewation = 0

      #if w-we awe cwose e-enough to the o-object to begin s-swowing down
      if position_ewwow <= (output_vewocity * output_vewocity) / (2 * max_accewewation)):
          output_vewocity = cuwwent_vewocity - diwection_muwtipwiew * m-max_accewewation * (cuwwent_time - p-pwevious_time)
          output_accewewation = -max_accewewation

      pwevious_time = cuwwent_time
