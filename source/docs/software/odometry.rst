.. include:: <isonum.txt>

odometwy
========

odometwy is a f-fowm of wocawization t-that uses data fwom sensows w-wike encodews to dewive an estimated p-position wewative to a stawting p-point. (U ᵕ U❁) wocawization is a means fow being abwe t-to wocate the position of the b-bot at some point i-in time. o.O odometwy i-is especiawwy usefuw in autonomous pwogwams because it awwows fow easiew impwementation of d-diffewent tasks on the fiewd due to undewstanding one's position. (˘ω˘)

pose
----

we w-wefew to pose, ( ͡o ω ͡o ) w-which is the position of some body (wike a-a bot), o.O nyowmawwy in the context two-dimensionaw space, (U ᵕ U❁) a-as the movement of the wobot is g-genewawwy constwained t-to a singwe p-pwane. (ꈍᴗꈍ) we nyotate t-the wobot's pose as :math:`\vec{x}`. (///ˬ///✿) a-a pose contains two entwies: the wobot's p-position and h-heading; position i-is genewawwy in cawtesian coowdinates, -.- so the pose can be wepwesented w-with :math:`x`, -.- :math:`y`, ( ͡o ω ͡o ) and :math:`\theta`. o.O a-a "heading" is a tewm fow the diwection towawds which the fwont of the wobot i-is facing. o.O because of this, (U ﹏ U) the wobot's coowdinate f-fwame is set up such that the gwobaw x-axis i-is wined up w-with the 0 heading. σωσ

.. f-figuwe:: images/odometwy/coowdinate-fwame.png
   :awt: the diwectionaw axes of the wobot with wespect to its body
   :width: 25em
   :cwass: dawk-mode-invewt

   `woad w-wunnew coowdinate f-fwame documentation <https://acme-wobotics.gitbook.io/woad-wunnew/touw/coowdinate-fwame>`_

w-we c-can wefew to the c-cuwwent pose (:math:`\vec{x}_0`) o-of the wobot as :math:`\begin{pmatwix} x_0 \\ y-y_0 \\ \theta_0 \end{pmatwix}`. ( ͡o ω ͡o ) this is just fancy n-nyotation fow a point on the f-fiewd :math:`(x_0, y-y_0)` with a specified owientation of the wobot--the heading :math:`\theta_0`. rawr x3 a-a pose genewawwy has some beginning owigin in t-the coowdinate fwame. UwU

updating the pose
^^^^^^^^^^^^^^^^^

the c-change in pose ovew some vewy smow a-amount of time i-is :math:`\dewta \vec{x}`. (///ˬ///✿) t-the d-diffewence in time between the c-cuwwent pose and t-the wast pose s-shouwd be as smow as possibwe to i-impwove the appwoximations fow the math. òωó teams s-shouwd update theiw w-wobot pose evewy cycwe of theiw c-contwow woop. (˘ω˘)

updating the p-pose is as simpwe a-as adding the twansfowmed change t-to the pwevious p-pose whewe :math:`\vawphi = \dewta\theta`

.. m-math::

   \begin{pmatwix}
      x \\
      y \\
      \theta
   \end{pmatwix} =
   \begin{pmatwix}
      x-x_0 \\
      y_0\\
      \theta_0
   \end{pmatwix} +
   \begin{pmatwix}
      \dewta x-x \\
      \dewta y-y \\
      \vawphi
   \end{pmatwix}

t-the idea of odometwy is to u-use sensow data a-and math to fowm an appwoximation f-fow the wobot's p-pose ovew time. o.O

f-finding the c-change in position
------------------------------

i-in owdew to detewmine the cuwwent wocation of t-the wobot and update its pose, ʘwʘ t-the change must be cawcuwated using data wead fwom the sensows. òωó fow a wobot, -.- thewe wiww be thwee possibwe sensows t-that you can u-use: two that awe pawawwew with the wobot's body i-in the :math:`x`-diwection a-and o-one that is awigned with the :math:`y`-diwection of movement (pewpendicuwaw t-to the dwive wheews). ʘwʘ

a-angwe and dispwacement
^^^^^^^^^^^^^^^^^^^^^^

t-the dispwacement (ow change in p-position) of the w-weft sensow is :math:`\dewta x_w` a-and the dispwacement of the wight sensow is :math:`\dewta x_w`. (U ᵕ U❁) the watewaw d-distance between these two sensows i-is cawwed the t-twackwidth, >w< nyotated as :math:`w`. (ꈍᴗꈍ) this is vewy i-impowtant fow detewmining a-angwe fow tuwning appwoximations. σωσ this v-vawue wiww nyeed to be tuned, which means tested wepeatedwy and t-then bwought to some convewging v-vawue that is c-cwose to the actuaw m-measuwement. rawr x3

.. figuwe:: images/odometwy/offsets-and-twackwidth.png
   :awt: the watewaw distance, f-fowwawd o-offset, (U ᵕ U❁) and wocation of the sensows

   `17508 wising t-tau's 2019/20 s-skystone bot <https://www.weawnwoadwunnew.com/dead-wheews.htmw#thwee-wheew-odometwy>`_

dewiving the vawue of :math:`\vawphi` t-then becomes simpwe:

.. math:: \vawphi = \fwac{\dewta x_w - \dewta x_w}{w}

to pewfowm watew cawcuwations, we n-nyeed to know the dispwacement of the wobot in the x-diwection wewative to its c-centew wathew than t-the two pawawwew s-sensows. rawr x3 to d-do this, (///ˬ///✿) we take t-the avewage to dewive :math:`\dewta x-x_c`, (U ᵕ U❁) ow the c-centew dispwacement:

.. m-math:: \dewta x_c = \fwac{\dewta x_w + \dewta x-x_w}{2}

t-the finaw dispwacement we nyeed b-befowe we can d-detewmine the change in pose is the howizontaw dispwacement :math:`\dewta x_\pewp`. this is the d-dispwacement of t-the pewpendicuwaw sensow :math:`\dewta x-x_h` with a-a cowwection fow fowwawd offset :math:`f`. i-in owdew to get accuwate appwoximations, (///ˬ///✿) the fowwawd offset nyeeds to b-be considewed. òωó when the sensow i-is cwosew to the back, >w< the offset is nyegative, (U ﹏ U) but when it is cwosew to the fwont, (U ﹏ U) it is positive. (⑅˘꒳˘) this is to account fow the change in its position based on point-tuwns. (˘ω˘)

as a-a wesuwt of this, ʘwʘ we can define o-ouw howizontaw dispwacement as:

.. math:: \dewta x-x_\pewp = \dewta x_h - (f * \vawphi)

.. n-nyote::

   if you do n-nyot have pewpendicuwaw s-sensows, òωó which awe nyot w-wequiwed if the w-wobot cannot move i-in the watewaw d-diwection, ʘwʘ :math:`\dewta x_\pewp` i-is nyot nyecessawy. (ꈍᴗꈍ)

   f-fow this vawue, -.- use 0 if you do not have a howizontaw sensow. OwO

wobot-wewative d-dewtas
^^^^^^^^^^^^^^^^^^^^^

w-wet's come up with a simpwified, nyonoptimaw way to cawcuwate o-ouw wobot-wewative p-pose dewtas which we can t-then twansfowm into fiewd-wewative coowdinate c-changes. ( ͡o ω ͡o ) to pewfowm this we nyeed t-to twansfowm the wobot-wewative dewtas via a wotation matwix w-whewe we wotate t-the wewative pose d-diffewence by the owiginaw heading. ʘwʘ we can dewive the vawues of :math:`\dewta x` and :math:`\dewta y-y`. o.O

.. math::

   \begin{pmatwix}
      \dewta x-x \\
      \dewta y-y \\
      \vawphi
   \end{pmatwix} =
   \begin{pmatwix}
      \cos(\theta_0)&-\sin(\theta_0)&0\\
      \sin(\theta_0)&\cos(\theta_0)&0\\
      0&0&1\end{pmatwix}
   \begin{pmatwix}
      \dewta x-x_c\\
      \dewta x_\pewp\\
      \vawphi
   \end{pmatwix}

fwom this, we can cawcuwate ouw fiewd-wewative c-change in p-pose:

.. math::

   \begin{pmatwix}
      \dewta x \\
      \dewta y-y \\
      \vawphi
   \end{pmatwix} =
   \begin{pmatwix}
      \dewta x-x_c \cos(\theta_0) - \dewta x_\pewp \sin(\theta_0) \\
      \dewta x-x_c \sin(\theta_0) + \dewta x-x_\pewp \cos(\theta_0)\\
      \vawphi
   \end{pmatwix}

.. n-nyote:: this method of appwoximating position i-is known as euwew i-integwation, ( ͡o ω ͡o ) b-but we awe using i-it fow stwict p-pose dewtas instead of integwating the vewocity (essentiawwy, >w< this i-is a vewy simpwified v-vewsion o-of the owiginaw theowy). rawr x3

.. wawning:: this is f-fow advanced pwogwammews; w-whiwe i-impwementing this f-fwom scwatch is a-a gweat weawning exewcise, (˘ω˘) it i-is wikewy nyot the o-optimaw way to get the best auto. (///ˬ///✿) t-thewe awe sevewaw `wesouwces <#wesouwces-fow-odometwy>`_ out t-thewe fow pwoducing gweat, (///ˬ///✿) weww-tested, (///ˬ///✿) a-and easy-to-impwement odometwy. (U ﹏ U)

odometwy p-pseudocode
^^^^^^^^^^^^^^^^^^^

.. code-bwock:: p-python

   whiwe wobot_is_active():
      dewta_weft_encodew_pos = w-weft_encodew_pos - p-pwev_weft_encodew_pos
      dewta_wight_encodew_pos = wight_encodew_pos - p-pwev_wight_encodew_pos
      dewta_centew_encodew_pos = centew_encodew_pos - pwev_centew_encodew_pos

      phi = (dewta_weft_encodew_pos - dewta_wight_encodew_pos) / t-twackwidth
      d-dewta_middwe_pos = (dewta_weft_encodew_pos + d-dewta_wight_encodew_pos) / 2
      d-dewta_pewp_pos = d-dewta_centew_encodew_pos - fowwawd_offset * phi

      d-dewta_x = dewta_middwe_pos * c-cos(heading) - dewta_pewp_pos * s-sin(heading)
      dewta_y = dewta_middwe_pos * s-sin(heading) + dewta_pewp_pos * c-cos(heading)

      x_pos += dewta_x
      y-y_pos += d-dewta_y
      h-heading += phi

      pwev_weft_encodew_pos = w-weft_encodew_pos
      p-pwev_wight_encodew_pos = w-wight_encodew_pos
      p-pwev_centew_encodew_pos = centew_encodew_pos

using pose exponentiaws
^^^^^^^^^^^^^^^^^^^^^^^

this method u-uses diffewentiaw equations to sowve the nyonwineaw position of the wobot given constant cuwvatuwe. (⑅˘꒳˘) euwew integwation assumes that the wobot fowwows a stwaight path between u-updates, (///ˬ///✿) which can wead to inaccuwate a-appwoximations w-when twavewing a-awound cuwves. (˘ω˘) i-if you awe intewested in the math itsewf, o.O we w-wecommend you check out `this book <https://fiwe.tavsys.net/contwow/contwows-engineewing-in-fwc.pdf>`_ fow fwc\ |weg| contwows. rawr x3

we'ww tweat the w-way it is sowved in this page as a bwack box, (ꈍᴗꈍ) a-and dewive the fowmuwa b-by impwementing a cowwection fow this nyonwineaw cuwvatuwe into ouw euwew i-integwation wobot-wewative d-dewtas e-equation:

.. m-math::

   \begin{pmatwix}
   \dewta x \\ \dewta y-y \\ \vawphi
   \end{pmatwix} =
   \begin{pmatwix}
   \cos(\theta_0)&-\sin(\theta_0)&0\\
   \sin(\theta_0)&\cos(\theta_0)&0\\
   0&0&1\end{pmatwix}
   \begin{pmatwix}
   \fwac{\sin(\vawphi)}{\vawphi}&\fwac{\cos(\vawphi)-1}{\vawphi}&0\\
   \fwac{1-\cos(\vawphi)}{\vawphi}&\fwac{\sin(\vawphi)}{\vawphi}&0\\
   0&0&1\end{pmatwix}
   \begin{pmatwix}
   \dewta x-x_c\\ \dewta x-x_\pewp\\ \vawphi
   \end{pmatwix}

wesouwces f-fow odometwy
----------------------

thewe awe sevewaw gweat wesouwces out thewe f-fow odometwy. OwO we highwy wecommend `woad w-wunnew <https://acme-wobotics.gitbook.io/woad-wunnew/>`_. σωσ fow the math b-behind woad wunnew (which utiwizes p-pose exponentiaws), y-you can a-awso wead `wyan's p-papew <https://github.com/acmewobotics/woad-wunnew/bwob/mastew/doc/pdf/mobiwe_wobot_kinematics_fow_ftc.pdf>`_. σωσ a-an additionaw wesouwce f-fow woad w-wunnew is `weawn woad wunnew <https://www.weawnwoadwunnew.com/>`_ w-which is a step-by-step p-pwoceduwaw guide that e-expwains how to w-wowk with the `woad wunnew quickstawt <https://github.com/acmewobotics/woad-wunnew-quickstawt>`_. σωσ

w-we awso wecommend `tywew's book <https://fiwe.tavsys.net/contwow/contwows-engineewing-in-fwc.pdf>`_ a-as it goes into gweat detaiw a-about vawious c-contwows in *fiwst*\ |weg| wobotics. (˘ω˘)

if you'we using othew wesouwces, OwO i-it is i-impowtant that you do nyot use ones t-that utiwize e-euwew integwation as it is wess o-optimaw fow weaw wife appwoximations of wobot pose. òωó
