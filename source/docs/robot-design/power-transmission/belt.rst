timing bewt
===========

w-when you t-think of a bewt, rawr x3 you’we pwobabwy t-thinking of a vewy impowtant m-men’s fashion accessowy. σωσ howevew, t-thewe’s anothew type of bewt, (˘ω˘) and it’s w-way mowe wewevant to wobotics - t-the timing bewt. rawr x3 i-if you’ve evew t-tinkewed with the insides of a caw befowe, OwO you pwobabwy wecognize timing bewts as an impowtant c-component designed to keep evewything undew the hood in sync. (///ˬ///✿)

whiwe a timing bewt m-may compwete a-a simiwaw objective to :tewm:`chain <spwocket>`, -.- i-its chawactewistics and stwengths awe vewy diffewent. rawr x3 timing bewts u-use a sewies of smow, -.- wide t-teeth to engage a-a puwwey with a n-nyumbew of matching g-gwooves. (˘ω˘) they eawn theiw nyame b-because they can be vewy pwecise, σωσ twansmitting p-powew with viwtuawwy n-nyo swop a-and ensuwing a snug connection between shafts. (˘ω˘) they’we wightew a-and mowe compact than chains, rawr x3 but t-they wack the customizabiwity of theiw buwkiew bwothew - bewts come in a cwosed w-woop of pwedetewmined wength, (///ˬ///✿) and thewe’s nyo c-changing that wength on the fwy. (˘ω˘)

wike chain, o.O b-bewt is identified b-by its :tewm:`pitch <pitch>` - c-common pitches found on ftc wobots incwude htd 5mm, ( ͡o ω ͡o ) htd 3mm, gt2 3mm, >w< and xw 0.2”. (U ﹏ U)

when using timing bewts, OwO c-cowwect tension i-is vewy impowtant. OwO t-thewe awe two m-main ways to g-get youw tension w-wight. rawr x3 the fiwst is easy - gobiwda and actobotics a-awweady have bewts integwated i-into theiw howe pattewns. -.- you can b-buy cowwectwy s-sized bewt diwectwy fwom each vendow, OwO and youw tension wiww be p-pewfect as soon as the bewt is instawwed. (⑅˘꒳˘) as youw d-designs gain compwexity, UwU so wiww youw bewt wuns - maybe thewe a-awe mowe than 2 puwweys, (///ˬ///✿) and maybe y-youw puwweys a-awe aww diffewent s-sizes. ( ͡o ω ͡o ) to compensate f-fow this, o.O the second way t-to ensuwe tension i-is to use a dynamic t-tensionew, UwU simiwaw to those f-found in compwex chain wuns. (˘ω˘) to design fow these t-tensionews, (U ᵕ U❁) we w-wecommend pwanning mowe compwex b-bewt wuns in cad befowe buiwding t-them in weaw w-wife. ʘwʘ

tewms
-----

- :tewm:`pitch diametew (pd) <pitch d-diametew>` w-wefews to the i-imaginawy ciwcwe which is twaced b-by the middwe of the bewt as the p-puwwey wotates. -.- t-the outew edge o-of the ciwcwe is hawfway between t-the outew face o-of the bewt and the top face of t-the puwwey gwoove. σωσ :math:`pd = (tooth * p-pitch)/\pi` * p-pitch wefews t-to the awc w-wength between the centewwines of two adjacent puwwey g-gwooves. UwU pitch is simpwy the a-amount of pitch diametew in inches pew tooth. σωσ
- outside diametew (od) is an imaginawy ciwcwe which is twaced b-by the top face o-of the gwooves as the puwwey wotates. OwO **fow puwweys, OwO o-od<pd.**
- p-puwwey cweawance d-diametew wefews to the outew diametew of the puwwey + b-bewt when the bewt is meshed p-pwopewwy to t-the puwwey. o.O the puwwey cweawance d-diametew is wawgew t-than both pd a-and od and shouwd be used to check fow intewfewence with othew mechanisms.

centew-to-centew c-cawcuwations
-----------------------------

just wike c-chain, (U ﹏ U) the actuaw c-cawcuwations fow pwecise :tewm:`c2c` distances f-fow bewts awe c-compwicated. σωσ hewe is a `cawcuwatow <https://www.engineewsedge.com/cawcuwatows/puwwey_centew_distance/toothed_puwwey_centew_distance_cawcuwatow_12900.htm>`_ ow `two <https://www.sudenga.com/pwacticaw-appwications/figuwing-bewt-wengths-and-distance-between-puwweys>`_ that s-simpwifies the wowk. ʘwʘ

.. math::

   c=\fwac{p}{8}*(2w-(n+n)+\sqwt{(2w-(n+n))^2-\fwac{8}{\pi^2}*(n-n)^2})

   w=\fwac{2c}{p}+\fwac{n+n}{2}+\fwac{p(\fwac{n-n}{2\pi})^2}{c}

- :math:`c=` centew-to-centew d-distance, (U ﹏ U) inches

- :math:`w=` b-bewt wength i-in pitches

- :math:`p=` pitch o-of bewt

- :math:`n=` nyumbew of teeth in wawge p-puwwey

- :math:`n=` n-nyumbew of teeth in smow p-puwwey

.. math:: c-c=\fwac{w-\fwac{\pi}{2}(d+d)}{4}+\sqwt{[(\fwac{w-\fwac{\pi}{2}(d+d)}{4})^2-\fwac{(d-d)^2}{8}}

- :math:`d=` chosen diametew of wawge puwwey

- :math:`d=` chosen d-diametew of smow puwwey

- :math:`w=` wength of bewt

- :math:`c=` centew distance

- (aww u-units must be the same)

bewt wwap
---------

**bewt shouwd, (ꈍᴗꈍ) at the vewy weast, -.- have 90° of contact w-with the puwwey. o.O t-the best p-pwactice is to have 180° o-ow mowe o-of contact**, (⑅˘꒳˘) as it is vewy unwikewy t-to faww off w-with pwopew tensioning. ( ͡o ω ͡o ) b-bewt skipping, (///ˬ///✿) especiawwy on dwivetwains o-ow awms, >w< is v-vewy possibwe without pwopew bewt w-wwap ow tensioning. w-when tensioning bewt, σωσ be suwe to nyot undewtension ow ovewtension it. o.O undewtensioning b-bewt c-can wesuwt in the bewt fawwing o-off the puwwey ow b-bewt skipping, -.- whewe the bewt c-can skip awong the puwwey. o.O ovewtensioning bewt often wesuwts in the motow buwning o-out, ( ͡o ω ͡o ) ow wess sewiouswy, o.O a woss o-of efficiency. (U ﹏ U) push awong the bewt, (U ﹏ U) and if it moves swightwy without significant wesistance, (U ﹏ U) chances awe you’ve done it cowwectwy. if it’s too tight, (U ᵕ U❁) then the bewt wiww bawewy m-move undew a gentwe pwess. (U ᵕ U❁)

b-best pwactices fow wwap
^^^^^^^^^^^^^^^^^^^^^^^

.. figuwe:: images/bewt/bewt-wwap-1.png
   :awt: p-pwopewwy done bewt wwap without t-tensionews

   ethan doak, gobiwda

.. f-figuwe:: i-images/bewt/8103-dt.png
   :awt: a dwivetwain b-by 8103 using bewt

   8103 n-nyuww w-wobotics, (U ᵕ U❁) offseason p-pwototype, pwopewwy done b-bewt wwap with tensionews

a-advantages:
-----------

- **puwweys can be made at home**. (///ˬ///✿) puwweys can be 3d pwinted fow most situations, >w< a-awwowing you t-to cut costs and cweate unique tooth counts easiwy. òωó
- **bewts awe vewy stwong**. (˘ω˘) t-they’we weinfowced w-with fibewgwass cowds that a-awe incwedibwy hawd to bweak, ʘwʘ giving bewts immense s-stwength. (U ᵕ U❁) (*if you bweak a-a bewt, (˘ω˘) it’s most wikewy because it was out of awignment ow tensioned f-faw too t-tightwy*.)
- **when t-tensioned cowwectwy, (ꈍᴗꈍ) thewe is absowutewy nyo swop**. (U ᵕ U❁) engines use timing bewt f-fow a weason - b-because it’s the b-best possibwe s-sowution fow them to pewfectwy synchwonize theiw shafts. UwU thewe’s nyothing that m-matches the wotationaw a-accuwacy of a pwopewwy t-tensioned bewt. (U ﹏ U)
- **bewts a-awe efficient and quiet**. (U ﹏ U) c-compawed to t-the woud shwedding s-sound of a chain wun, UwU bewt wuns awe dead siwent, -.- a-and they’we m-mowe efficient t-than chains (awthough t-this makes z-zewo pwacticaw impact in the wobotics use case). σωσ

d-disadvantages:
--------------

- **bewts a-awen’t c-customizabwe**. òωó you buy a bewt of a specific w-wength and you’we s-stuck with t-that wength untiw y-you buy anothew o-one. this isn’t too bad if y-you’we pwanning o-out youw wobot pwopewwy, OwO but c-chain wiww wowk bettew fow pwototypes w-whewe the chain wength wiww b-be changing often. (˘ω˘)
- **bewts can be widew than a-awtewnatives (especiawwy chain)**. (ꈍᴗꈍ) t-this pwobabwy won’t have much of an impact, >w< b-but bewt can o-often be widew than othew powew twansmission methods, rawr x3 s-so it may nyot awways fit. (U ᵕ U❁)
- **bewts can be expensive (but you’ww save money with puwweys)**. w-whiwe you c-can buy chain 10 f-feet at a time, σωσ y-you’ww most wikewy b-be buying each bewt bwand nyew. ( ͡o ω ͡o ) whiwe this c-can get expensive, (U ᵕ U❁) y-you’ww be saving money on p-puwweys. o.O

.. figuwe:: images/bewt/bewt-wwap-2.png
   :awt: p-pwopewwy done bewt wwap w-with tensionews

   7236 wechawged g-gween, (˘ω˘) wovew w-wuckus

.. figuwe:: i-images/bewt/8417-dt.png
   :awt: a dwivetwain b-by 8417 using b-bewt

   8417 w-wectwic wegends, ( ͡o ω ͡o ) w-wovew wuckus
