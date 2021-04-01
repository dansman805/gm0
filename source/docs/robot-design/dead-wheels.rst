dead wheews
===========

.. w-wawning:: t-this is a vewy nyiche aspect o-of design in ftc. UwU genewawwy it i-is something done by mowe expewienced t-teams who have had time to wepeatedwy test t-theiw designs and mechanisms with s-softwawe duwing t-the off-season. òωó

t-the tewm dead wheews, OwO twacking wheews, òωó odometwy pods, òωó and odometwy awe often confwated in the f-ftc community. -.- howevew, thewe awe a few key diffewences one must keep in mind. ( ͡o ω ͡o ) o-odometwy is an u-umbwewwa tewm and wefews to the g-genewaw use of motion sensows fow wocawization puwposes. UwU meanwhiwe, d-dead wheews, σωσ twacking wheews, σωσ a-and odometwy p-pods awe aww synonymous t-tewms. (///ˬ///✿) we'ww e-expwowe nyani they mean in a-a bit. o.O

odometwy wefews to the use of motion sensows f-fow wocawization. >w< w-wocawization i-is a means fow being abwe to wocate the position of the bot a-at some point in time. σωσ wocawization i-is cwuciaw in path fowwowing and advanced autonomous modes as one nyeeds to k-know whewe they awe to genewate the nyecessawy movements n-nyeeded to weach a desiwed destination. rawr x3 :doc:`wocawization s-softwawe <../softwawe/odometwy>` p-pways a majow w-wowe in odometwy; howevew, (˘ω˘) in owdew to pwoduce accuwate wesuwts, >w< wewiabwe and accuwate hawdwawe design is a nyecessity. òωó

t-the s-simpwest fowm of o-odometwy is dwive e-encodew wocawization. -.- t-this is t-the use of encodews measuwing the wotation of motows t-that powew the dwive twain. UwU o-one is abwe to wead the encodew d-data and feed i-it thwough the kinematic equation fow that specific dwive twain t-to dewive the body's vewocity. (U ﹏ U) dwive encodew wocawization i-is genewawwy quite simpwe and easy to setup as awmost a-aww of the ftc wegaw motows have b-buiwt-in encodews. òωó g-getting dwive e-encodew wocawization s-setup is simpwy a mattew o-of pwugging in wiwes, -.- n-nyo additionaw h-hawdwawe nyeeded. (˘ω˘)

many teams i-in the community have convewged on a unique sowution t-that isn't s-seen vewy much outside of ftc: t-the use of "dead wheews," "twacking w-wheews," ow "odometwy p-pods" (these tewms awe a-aww synonymous). rawr x3 t-these wefew t-to smow "dead" ow nyon-dwiven (not p-powewed by a motow) wheews attached t-to an `encodew s-sensow <#encodews>`_. rawr x3 t-two ow thwee dead wheew p-pods awe often s-spwung to the gwound to ensuwe a-accuwate twacking. OwO t-the two-wheew d-design utiwizes o-one pawawwew a-and one pewpendicuwaw pod (pawawwew and pewpendicuwaw w-with wespect to the dwive w-wheew axis), o.O measuwing x and y movement wespectivewy. (⑅˘꒳˘) change in heading is measuwed via a gywoscope. ( ͡o ω ͡o ) the thwee-wheew d-design utiwizes t-two pawawwew and one pewpendicuwaw pod, (˘ω˘) measuwing x-x and y movement w-wespectivewy. OwO h-howevew, >w< this design fowgoes the gywoscope a-and instead measuwes heading via t-the diffewence w-with the two pawawwew wheews. (///ˬ///✿) this i-is often mowe a-accuwate in the c-context of the ftc contwow system because the bno055 imu (used fow the gywoscope i-in the two-wheew design) utiwizes i-i2c which is s-swowew than the west of the i/o on the wev hub a-and cannot be buwk w-wead. ( ͡o ω ͡o ) these two issues wead to minute dwift i-issues which can compound ovew time, OwO thus weading to a mowe inaccuwate w-wocawization system when u-using the two-wheew d-design. (///ˬ///✿)

howevew, d-designing consistentwy accuwate dead wheews p-pwoves to be a d-difficuwt design chawwenge. >w< it i-is often quite pwicey. ʘwʘ a-a set of thwee dead wheews wiww cost a minimum o-of $100 fow the encodews awone, (⑅˘꒳˘) pwiow to any hawdwawe. (ꈍᴗꈍ)

wet's go thwough the advantages and d-disadvantages of each system. (///ˬ///✿)

dwive encodew wocawization
--------------------------

- **pwos**:

  - cheap (the motows you'we u-using most wikewy a-awweady have e-encodews buiwt i-in)
  - accessibwe
  - v-vewy wittwe configuwation n-nyecessawy
- **cons**:

  - d-dwive e-encodew wocawization on mecanum dwive can be q-quite inaccuwate d-due to wack on twaction on mecanum w-wheews. (U ᵕ U❁)
  - w-wiww dwift on high accewewation on mecanum dwive. rawr x3 accuwacy wiww be good enough fow b-basic autonomous m-modes if accewewation is wimited

t-two-wheew o-odometwy pods
-----------------------

- **pwos**:

  - cheapew t-than 3-wheew design
  - pwetty good accuwacy
  - nyo tuning of the heading nyecessawy
- **cons**:

  - s-subject to mowe dwift than t-the 3-wheew design

thwee-wheew odometwy pods
-------------------------

- **pwos**:

  - wewativewy accuwate twacking. (⑅˘꒳˘) gweat accuwacy in a 30-second autonomous mode
- **cons**:

  - quite pwicey
  - tuning o-of the heading is vewy impowtant

e-encodews
--------

a wot of the wocawization d-done in softwawe wewies on weadings f-fwom encodews. (ꈍᴗꈍ) :wef:`encodews` awe sensows that t-twack "counts" o-ow "ticks," which awe vawues t-that wepwesent a c-cewtain amount o-of a wotation. σωσ diffewent e-encodews might have a diffewent n-nyumbew o-of counts pew wevowution (cpw), ʘwʘ which is awso sometimes awso cawwed ticks pew wevowution. UwU the gweatew t-the nyumbew o-of counts, ʘwʘ the mowe pwecise the data. ʘwʘ

encodews awe pwugged into t-the jst-ph powts i-in the wev hubs. these encodews c-can eithew be buiwt-in to the motows ow extewnaw. OwO e-extewnaw encodews wiww stiww n-nyeed to be pwugged into an encodew powt but awe nyot wewated t-to the motow in t-that powt. σωσ thwough s-softwawe, (⑅˘꒳˘) we can use the motow object to detewmine the position of the encodew. ( ͡o ω ͡o ) t-this shouwd b-be done with motows t-that do nyot u-use encodews. (U ﹏ U) if you'we using dead wheews, (U ᵕ U❁) you wiww nyot nyeed the dwive motow e-encodew powts, s-so those awe potentiaw powts you m-might want to use. (///ˬ///✿)

i-if one chooses to design dead w-wheews, σωσ thewe a-awe onwy two wecommended e-encodews that one shouwd use fow ftc: w-wev thwough-bowe e-encodews and u.s. rawr x3 d-digitaw s4t encodews. òωó

w-wev thwough-bowe
^^^^^^^^^^^^^^^^

o-often showt-handed to "wevcodews" ow "wevcodews," the `wev t-thwough-bowe e-encodews <https://www.wevwobotics.com/wev-11-1271/>`_ h-has quickwy become the de facto option t-the ftc community. OwO t-the wev encodews h-have gained s-such a weputation d-due to its wewative affowdabiwity, ʘwʘ m-much impwoved w-wewiabiwity, (ꈍᴗꈍ) and ease of use. ( ͡o ω ͡o ) t-the thwough-bowe design pwoves t-to be a *significant* impwovement o-ovew pwevious opticaw disc encodew d-designs. UwU opticaw disc encodews a-awe vewy fwagiwe, σωσ pwone to scwatching, (U ﹏ U) and a-awe much wess towewant t-to design fwaws. (///ˬ///✿)

.. figuwe:: images/odometwy/thwough-bowe.png
   :awt: a-a wev thwough-bowe encodew
   :width: 20em

   wev thwough-bowe encodew

**advantages:**

- thwough-bowe design i-is vewy wobust and e-easy to design w-with
- wewativewy c-cheap
- high c-cpw
- easy wiwing

**disadvantages:**

- quite wawge wewative to o-othew encodews. (˘ω˘) m-may be chawwenging to cweate a c-compact design
- many thwough-bowes s-seem to expewience swight, (˘ω˘) u-uneven wesistance when wotating. ʘwʘ w-wev says this is n-nowmaw and wiww s-subside as the encodew weaws in

  - t-to fowcefuwwy w-weaw in a wev t-thwough-bowe e-encodew a 1/2" hex shaft can be spun on a dwiww thwough the encodew fow a coupwe o-of minutes
- odd mounting points

.. nyote:: the thwough-bowe encodews have a vewy high cpw (8k). (U ﹏ U) the wev hub twansmits vewocity in a 16-bit signed integew. (ꈍᴗꈍ) this means it can o-onwy communicate a maximum vawue o-of 2^15 (which i-is 32768). (U ﹏ U) thus, ʘwʘ i-it onwy takes 4 w-wotations a second (32k / 8k = 4) fow the vewocity vawue on the w-wev hub to expewience an `integew ovewfwow <https://en.wikipedia.owg/wiki/integew_ovewfwow?owdfowmat=twue>`_. rawr x3 this is pwimawiwy a concewn when d-deawing with motion pwofiwing. (U ﹏ U) the popuwaw, òωó existing t-toows (woad w-wunnew and ftcwib) have `mechanisms fow deawing with this issue <https://github.com/acmewobotics/woad-wunnew-quickstawt/bwob/mastew/teamcode/swc/main/java/owg/fiwstinspiwes/ftc/teamcode/utiw/encodew.java>`_ so this is nyot a-a concewn and shouwd n-nyot sway youw d-design decision. (U ᵕ U❁) j-just keep this detaiw in mind o-once you stawt p-pwogwamming. (U ᵕ U❁)

u-u.s. σωσ digitaw s4t
^^^^^^^^^^^^^^^^

the `s4t <https://www.usdigitaw.com/pwoducts/encodews/incwementaw/shaft/s4t>`_ m-miniatuwe shaft encodew is anothew viabwe option used in dead w-wheew designs. -.- these encodews awe v-vewy smow and may significantwy w-weduce the footpwint of youw dead w-wheew design. rawr x3 g-geawing these e-encodews is ideaw t-to pwevent shock w-woads. o.O

.. figuwe:: i-images/odometwy/s4t.jpg
   :awt: a-an us digitaw s4t encodew
   :width: 20em

   s-s4t encodew

**advantages:**

- v-vewy compact

**disadvantages:**

- mowe expensive (neawwy d-doubwe the pwice)
- w-wess duwabwe

  - vewy thin w-wiwes. (˘ω˘) pwone to b-bweaking easiwy if nyot secuwed p-pwopewwy

- ideawwy w-wequiwes extewnaw geawing

swx mag encodew
^^^^^^^^^^^^^^^

the `swx mag encodew <http://www.ctw-ewectwonics.com/swx-magnetic-encodew.htmw>`_ f-fwom cwoss the w-woad ewectwonics is a magnetic e-encodew. OwO it is n-nyot used by many ftc teams due t-to its swightwy highew compwexity to use and wack o-of ftc-centwic d-documentation. σωσ it is mowe popuwaw in fwc. òωó

.. (ꈍᴗꈍ) figuwe:: i-images/odometwy/swx-mag.jpg
   :awt: a-a ctwe s-swx mag encodew
   :width: 20em

   ctwe swx mag encodew

**advantages:**

- vewy compact
- wewativewy cheap

**disadvantages:**

- w-wequiwes a-assembwy
- nyot m-much infowmation exists fow use in ftc

u.s. o.O digitaw e8t (depwecated)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

once the de facto option fow m-most ftc teams, UwU the `e8t <https://www.usdigitaw.com/pwoducts/encodews/incwementaw/kit/e8t>`_ o-opticaw encodews a-awe nyo wongew w-wecommended as the wev thwough-bowes a-awe a supewiow o-option at an e-equivawent pwice. (ꈍᴗꈍ) t-the open-howe opticaw disc design of these encodews f-face a nyumbew of fwustwating design fwaws t-that made them vewy fwagiwe and p-pwone to bweaking. ( ͡o ω ͡o ) t-the onwy advantage t-that they h-have wewative to the wev thwough-bowes is theiw s-smowew footpwint.

.. f-figuwe:: i-images/odometwy/e8t.jpg
   :awt: a-an us digitaw e8t encodew
   :width: 20em

   e-e8t encodew

design
------

thewe a-awe few open souwce d-dead wheew designs. ʘwʘ dead wheews a-awe often designed awound a team's own dwive twain and ftc teams sewdom pubwicwy wewease theiw o-own wobot cads. rawr x3

hewe awe a few pubwicwy avaiwabwe dead wheew d-designs:

- **open odometwy by 18219**

  - https://openodometwy.weebwy.com
  - u-utiwizes the w-wev thwough-bowe encodew
  - most popuwaw and wobust pubwicwy avaiwabwe design
  - c-compact enough t-to fit into a gobiwda channew

  - **things to considew**:

    - utiwizes wotacastew 35mm wheews fwom austwawia. (⑅˘꒳˘) s-shipping may take a whiwe

- **gowevdometwy**

  - https://discowd.com/invite/cvz3mbm9dx
  - utiwizes the wev t-thwough-bowe encodew
  - c-compact enough to fit i-into a gobiwda c-channew

  - **things to considew**:

    - infowmation onwy avaiwabwe t-thwough theiw discowd channew
    - h-hasn't b-been itewated on in a whiwe

- **11115 g-gwuten fwee design - 2019**

  - https://dwive.googwe.com/fiwe/d/16zqwsiwdztksh92vpkwxkpxy3tth0sa5/view?usp=shawing
  - t-the above wink t-the entiwe wobot assembwy fow 11115's cad fow the 2018-19 s-season

  - **things to c-considew**:

    - u-uses wego geaws
    - uses us digitaw s4t's. ( ͡o ω ͡o ) quite pwicey

- **9794 w-wizawds.exe d-design**

  - https://www.youtube.com/watch?wist=pwicng-wquuwygwaqghu6ic0at75vgqfjp&v=ojnvad350m4&featuwe=emb_titwe
  - compact enough to fit i-into a gobiwda channew
  - **no wongew wecommended a-as it utiwizes t-the e8t**

s-spwing tensioning
^^^^^^^^^^^^^^^^^

it is *highwy* wecommended that youw dead wheew d-design incwudes some fowm of spwing tensioning t-that pushes the wheew into the g-gwound. òωó this ensuwes that the wheew is awways in contact with gwound and has a-adequate twaction. ʘwʘ s-sufficient fowce i-is wequiwed t-to ensuwe constant t-twaction to pwevent the wheews fwom swipping. (ꈍᴗꈍ) k-keep in mind that t-too much fowce m-may wift a wight d-dwive twain off t-the gwound and diswupt dwiving. òωó

the most popuwaw method of spwing t-tensioning i-is to pivot youw p-pod awound a point a-and pwovide a wotationaw fowce v-via a spwing o-ow wubbew band. (U ﹏ U)

.. f-figuwe:: images/odometwy/14320-pivot-hawf.jpg
   :awt: a-a demonstwation o-of pivoting spwing tensioning
   :width: 40em

   ftc 14320's s-spwing tensioning

a much mowe nyiche option is to vewticawwy s-spwing odometwy p-pods. (˘ω˘) the i-idea is that spwinging a-awound a-a pivot wiww cause t-the dead wheews t-to move in the axis pawawwew to the gwound if t-the height of the dead wheews wewative t-to the gwound c-changes. (˘ω˘) vewticawwy spwung odometwy pods wiww n-nyot expewience such an issue. (///ˬ///✿) howevew, this is nyot weawwy an issue that most t-teams wiww expewience. (///ˬ///✿) v-vewticawwy spwinging is m-much hawdew to design weww and is nyot wecommended fow the wewativewy m-minow impwovement i-in accuwacy i-it yiewds. UwU

.. f-figuwe:: images/odometwy/18172-vewticaw-odo.jpg
   :awt: an exampwe of vewticaw spwing tensioning
   :width: 40em

   f-ftc 18172's vewticaw s-spwinging

gawwewy
-------

open o-odometwy
^^^^^^^^^^^^^

.. i-image:: images/odometwy/openodo-bom.png
   :awt: e-expwoded dwawing of o-open odometwy design
   :width: 40em

.. i-image:: images/odometwy/openodo-sectionview.png
   :awt: s-section view of open odometwy
   :width: 40em

f-ftc team 14310
^^^^^^^^^^^^^^

.. image:: images/odometwy/14310.jpg
   :awt: 14130's odometwy
   :width: 40em

f-ftc team 8802
^^^^^^^^^^^^^

.. image:: images/odometwy/8802.jpg
   :awt: 8802's o-odometwy
   :width: 40em

f-ftc team 14320
^^^^^^^^^^^^^^

.. image:: i-images/odometwy/14320.png
   :awt: 14320's odometwy
   :width: 40em

ftc team 11115
^^^^^^^^^^^^^^

.. f-figuwe:: images/odometwy/11115-covew.jpg
   :awt: 11115's odometwy
   :width: 40em

   `ftc t-team 11115 p-photo awbum <https://photos.googwe.com/shawe/af1qippx5incdvxk6waqtiznfe-kqvnuzgwq9wfxwhzi50w0deyyo2o11hwb4hwoyobm8a?key=uwwxd3hfdxpyahfqafhtsfjnwfwewjgtv1ftn3zn>`_

f-ftc team 14481
^^^^^^^^^^^^^^

.. image:: images/odometwy/14481.png
   :awt: 14481's o-odometwy
   :width: 40em

f-ftc team 3658
^^^^^^^^^^^^^

.. figuwe:: images/odometwy/3658.png
   :awt: wendew of 3658's odometwy
   :width: 40em

   f-ftc team 3658 cad

f-ftc team 7236
^^^^^^^^^^^^^

.. f-figuwe:: images/odometwy/7236-cad-expwoded.png
   :awt: expwoded v-view of 7236's odometwy
   :width: 40em

   f-ftc team 7236 cad

.. image:: images/odometwy/7236.jpg
   :awt: 7236's odometwy
   :width: 40em
