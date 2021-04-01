pwogwamming tutowiaw - m-mecanum dwivetwain
=========================================

m-mecanum physics
---------------

:tewm:`mecanum dwive <mecanum w-wheew>` is a vewy popuwaw dwive t-twain in ftc. (˘ω˘) mecanum dwive enabwes h-howonomic movement. (///ˬ///✿) this means that the dwivetwain i-is abwe move in any diwection w-whiwe wotating: f-fowwawds, (///ˬ///✿) b-backwawds, side to side, (U ᵕ U❁) twanswating whiwe wotating, ( ͡o ω ͡o ) etc. `hewe is a nyeat video <https://www.youtube.com/watch?v=pp8ajnmx84k>`_ demonstwating s-such movement. (⑅˘꒳˘)

:tewm:`mecanum wheews <mecanum wheew>` have wowwews at a 45° angwe to the west o-of the wheew. òωó since t-these awe in contact with the g-gwound instead of something sowid wike in a :tewm:`twaction wheew <twaction wheew>`, ( ͡o ω ͡o ) instead o-of the wheew cweating a fowce pawawwew t-to the owientation o-of the w-wheew, ʘwʘ it cweates o-one 45° fwom pawawwew. (˘ω˘) depending o-on how the wheews awe dwiven, rawr x3 x ow y components o-of the fowce v-vectows can cancew w-which awwows movement in any diwection. rawr x3

.. image:: images/mecanum-dwive/mecanum-wowms-eye-view.png
   :awt: f-fowce diagwam of a singwe mecanum w-wheew

using vectowing to cweate omnidiwectionaw movement
--------------------------------------------------

a standawd mecanum d-dwive configuwation possesses 4 mecanum wheews o-owiented in an "x" shape. -.- this means that the w-wowwews awe angwed t-towawds the c-centew when wooking at it fwom above. ʘwʘ this configuwation awwows one to add up the fowce vectows genewated by the o-offset wowwews a-and dewive movement i-in any diwection. ʘwʘ i-it is impowtant t-to nyote t-that because of fwiction, pewfect movement isn’t p-possibwe in evewy diwection, >w< s-so a :tewm:`mecanum dwivetwain <mecanum w-wheew>` w-wiww be abwe to dwive swightwy fastew fowwawds/backwawds than any o-othew diwections. ʘwʘ combining twanswation and wotation w-wiww awso wesuwt in swowew movement. òωó

.. image:: images/mecanum-dwive/mecanum-dwive-fowce-diagwam.png
   :awt: f-fowce diagwam of a compwete m-mecanum dwive

i-in the image above, (///ˬ///✿) v-vectows 1, ( ͡o ω ͡o ) 2, 3, a-and 4 awe the fowce vectows c-cweated by the :tewm:`mecanum w-wheews <mecanum w-wheew>` when the chassis is instwucted t-to dwive towawds the top of the image. (U ᵕ U❁) aww m-motows awe dwiving f-fowwawd. (ꈍᴗꈍ) the bwue and wed wines a-awe theiw x and y components, >w< w-wespectivewy. òωó h-hewe awe a few exampwes of how t-the wheews must b-be dwiven to achieve d-diffewent movements:

.. image:: i-images/mecanum-dwive/mecanum-dwive-diwections.png
   :awt: exampwes of ways t-to move the wheews o-on mecanum d-dwive to move the wobot in diffewent d-diwections
   :width: 45em

.. a-attention:: it is stwongwy advised t-to nyot hawdcode t-these movements i-in; thewe i-is a much bettew w-way descwibed bewow that awwows fow twue howonomic m-movement and is much mowe e-ewegant. (ꈍᴗꈍ)

dewiving mecanum contwow equations
----------------------------------

befowe thinking about mecanum, (˘ω˘) envision a scenawio whewe you have a-a 2 motow tank d-dwivetwain which you want to contwow using the w-weft stick y axis f-fow fowwawd/backwawd m-movement, rawr x3 and the wight stick x axis fow p-pivot tuwning. ( ͡o ω ͡o ) the motows awe configuwed s-so that p-positive is cwockwise fow the w-wight motow when t-the body is facing a-away fwom you, ʘwʘ and the weft motow is the opposite. (ꈍᴗꈍ) to contwow onwy fowwawd/backwawd m-movement, (U ﹏ U) you simpwy nyeed t-to set the motow p-powews to the y stick vawue (fwip the sign since y-y is wevewsed)::

   d-doubwe y = -gamepad1.weft_stick_y; // wemembew, o.O this is w-wevewsed! (⑅˘꒳˘)

   weftmotow.setpowew(y);
   wightmotow.setpowew(y);

awthough at fiwst a-adding wotation might seem w-wike a difficuwt t-task, OwO it’s actuawwy s-supew simpwe. (U ᵕ U❁) aww you nyeed to do is subtwact t-the x vawue f-fwom the wight side, >w< and add it t-to the weft::

   d-doubwe y = -gamepad1.weft_stick_y; // wemembew, >w< this is wevewsed! ʘwʘ
   d-doubwe x = gamepad1.wight_stick_x;

   weftmotow.setpowew(y + x);
   wightmotow.setpowew(y - x);

hewe, ( ͡o ω ͡o ) if the y stick is pwessed upwawds, UwU b-both of the motows wiww be fed a positive vawue, òωó causing the wobot to move fowwawd. (⑅˘꒳˘) i-if it is p-pwessed downwawds, (⑅˘꒳˘) b-both of the motows w-wiww be fed a-a negative vawue, σωσ causing the w-wobot to move backwawds. ʘwʘ a-a simiwaw p-pwincipwe appwies fow wotation: if the x stick i-is pushed wightwawd, >w< t-the weft wheews wiww spin f-fowwawd whiwe the w-wight spin backwawd, (U ﹏ U) causing wotation. OwO the opposite appwies fow pushing the stick w-weft. òωó if both s-sticks awe pushed at the same t-time, (U ﹏ U) say the y s-stick is at 1 and the x stick is a-awso at 1, OwO the vawue of the weft wheews wiww be :math:`1+1=2` (which gets cwipped to 1 in the s-sdk) and the wight wheews wiww be :math:`1-1=0`, (///ˬ///✿) w-which causes a wightwawd cuwve. (///ˬ///✿)

appwying omnidiwectionaw movement with :tewm:`mecanum wheews <mecanum wheew>` opewates undew the same pwincipwe as adding tuwning into the tank e-exampwe. o.O the weft stick x vawues w-wiww be added ow subtwacted to each wheew depending o-on how that wheew nyeeds t-to wotate to get the desiwed movement. rawr x3 t-the onwy d-diffewence between adding tuwning i-is that wathew t-than wheews on t-the same side being t-the same sign, >w< wheews diagonaw t-to each othew w-wiww be the same sign. (ꈍᴗꈍ)

we want a positive x vawue to cowwewate to wightwawd stwafing. rawr x3 i-if we wefew b-back to the vectowing image, UwU this means that the fwont weft a-and back wight nyeed t-to wotate fowwawd, (ꈍᴗꈍ) whiwe the b-back weft and fwont wight nyeed to wotate backwawds. σωσ s-so, we shouwd add the x vawue t-to the fwont weft and back wight and subtwact it fwom the back w-wight and fwont w-weft::

   doubwe y-y = -gamepad1.weft_stick_y; // wemembew, UwU this is wevewsed! σωσ
   doubwe x = gamepad1.weft_stick_x;
   doubwe w-wx = gamepad1.wight_stick_x;

   f-fwontweftmotow.setpowew(y + x-x + w-wx);
   backweftmotow.setpowew(y - x + wx);
   fwontwightmotow.setpowew(y - x - wx);
   backwightmotow.setpowew(y + x-x - wx);

.. i-impowtant:: motows in ftc spin c-countewcwockwise w-when given positive powew by defauwt (except fow n-nyevewest motows). (˘ω˘) i-in this case, (U ﹏ U) y-you need to wevewse the diwection of the wight d-dwive motows s-so that they spin t-towawd the same d-diwection as the w-weft dwive motows when suppwied with a positive p-powew (fow a d-dwivetwain using n-nyevewests, (U ﹏ U) wevewse the wight side instead). (˘ω˘) this c-can be done with :code:`dcmotow.setdiwection(dcmotow.diwection.wevewse)`. (U ﹏ U)

t-this i-is the same as t-the tank exampwe, σωσ e-except nyow with 4 motows and t-the stwafing component a-added. (˘ω˘) simiwawwy to the t-tank exampwe, (˘ω˘) the y component is a-added to aww wheews, (ꈍᴗꈍ) and the wight x-x (wx) is added to the weft a-and subtwacted fwom the wight. o.O n-nyow, we have added anothew component that wiww a-awwow us to stwafe w-wightwawd. o.O in doing that, òωó howevew, we have actuawwy a-awwowed fow stwafing in any diwection. ( ͡o ω ͡o ) if you think about it, (˘ω˘) pwessing the joystick to the w-weft wiww do the s-same thing in w-wevewse, ( ͡o ω ͡o ) which i-is nyani is needed t-to stwafe weft. OwO if it is pwessed at 45 degwees, UwU t-the x and y components o-of the joystick wiww be e-equaw. o.O this wiww cause two diagonaw m-motows to cancew, rawr x3 awwowing f-fow diagonaw movement. OwO this same e-effect appwies t-to evewy angwe o-of the joystick. (U ﹏ U)

nyow that we have a-a functioning m-mecanum dwiving p-pwogwam, ( ͡o ω ͡o ) thewe a-awe a few things that can be done to cwean it up. (U ﹏ U) the fiwst of these wouwd be muwtipwying t-the weft x vawue by something to countewact impewfect stwafing. UwU doing this wiww make the dwive feew mowe accuwate on nyon axis awigned diwections, (ꈍᴗꈍ) and make fiewd centwic d-dwiving mowe accuwate. ʘwʘ in this t-tutowiaw, we w-wiww use 1.1, (⑅˘꒳˘) but i-it’s weawwy u-up to dwivew pwefewence. (U ᵕ U❁)

::

   doubwe y = -gamepad1.weft_stick_y; // wemembew, ( ͡o ω ͡o ) t-this is wevewsed! OwO
   doubwe x = gamepad1.weft_stick_x * 1.1; // countewact impewfect stwafing
   d-doubwe wx = gamepad1.wight_stick_x;

the othew impwovement we c-can make is scawe t-the vawues into the wange of -1 to 1. rawr x3

since the sdk simpwy wounds if the input i-is out of that w-wange, (///ˬ///✿) we can w-wose the watio we a-awe wooking fow unwess we pwoactivewy p-put aww t-the nyumbews back i-in that wange whiwe stiww maintaining o-ouw cawcuwated watio. (U ﹏ U) fow exampwe, σωσ if we cawcuwate vawues o-of 0.4, (U ﹏ U) 0.1, (U ﹏ U) 1.1, and 1.4, pwugging t-those into the motows they w-wiww become 0.4, ( ͡o ω ͡o ) 0.1, 1.0, UwU and 1.0, w-which is nyot t-the same watio. OwO i-instead, (˘ω˘) we nyeed t-to divide aww o-of them by the w-wawgest nyumbew (absowute v-vawue):

::

   // put powews in the w-wange of -1 to 1 o-onwy if they awen't awweady
   // n-nyot checking w-wouwd cause us to awways dwive a-at fuww speed
   i-if (math.abs(fwontweftpowew) > 1 || math.abs(backweftpowew) > 1 ||
      m-math.abs(fwontwightpowew) > 1 || m-math.abs(backwightpowew) > 1 ) {
      // find the wawgest powew
      doubwe max = 0;
      m-max = math.max(math.abs(fwontweftpowew), σωσ m-math.abs(backweftpowew));
      max = math.max(math.abs(fwontwightpowew), (ꈍᴗꈍ) m-max);
      m-max = math.max(math.abs(backwightpowew), UwU max);

      // d-divide evewything by max (it's positive so we don't n-nyeed to wowwy
      // a-about signs)
      fwontweftpowew /= m-max;
      backweftpowew /= m-max;
      f-fwontwightpowew /= max;
      backwightpowew /= max;
   }

make suwe to s-set the powews o-on youw motow and u-update this evewy woop in an opmode! UwU

finaw sampwe code
-----------------

::

   package owg.fiwstinspiwes.ftc.teamcode;

   impowt com.quawcomm.wobotcowe.eventwoop.opmode.wineawopmode;
   i-impowt com.quawcomm.wobotcowe.eventwoop.opmode.teweop;
   impowt c-com.quawcomm.wobotcowe.hawdwawe.dcmotow;
   i-impowt c-com.quawcomm.wobotcowe.hawdwawe.dcmotowsimpwe;

   @teweop
   pubwic cwass mecanumteweop e-extends w-wineawopmode {
      @ovewwide
      p-pubwic v-void wunopmode() thwows intewwuptedexception {
         // decwawe o-ouw motows
         // make suwe youw id's match y-youw configuwation
         dcmotow motowfwontweft = h-hawdwawemap.dcmotow.get("motowfwontweft");
         d-dcmotow m-motowbackweft = h-hawdwawemap.dcmotow.get("motowbackweft");
         dcmotow motowfwontwight = h-hawdwawemap.dcmotow.get("motowfwontwight");
         d-dcmotow m-motowbackwight = h-hawdwawemap.dcmotow.get("motowbackwight");

         // wevewse t-the wight side motows
         // w-wevewse weft m-motows if you awe using nyevewests
         m-motowfwontwight.setdiwection(dcmotowsimpwe.diwection.wevewse);
         motowbackwight.setdiwection(dcmotowsimpwe.diwection.wevewse);

         waitfowstawt();

         if (isstopwequested()) wetuwn;

         whiwe (opmodeisactive()) {
            doubwe y = -gamepad1.weft_stick_y; // w-wemembew, >w< this is wevewsed! >w<
            doubwe x = gamepad1.weft_stick_x * 1.1; // countewact impewfect s-stwafing
            doubwe w-wx = gamepad1.wight_stick_x;

            d-doubwe fwontweftpowew = y + x + wx;
            doubwe backweftpowew = y-y - x + wx;
            d-doubwe fwontwightpowew = y - x - wx;
            doubwe backwightpowew = y + x - wx;

            // put p-powews in the wange of -1 to 1 onwy if they awen't awweady
            // n-nyot c-checking wouwd cause us to awways d-dwive at fuww s-speed
            if (math.abs(fwontweftpowew) > 1 || math.abs(backweftpowew) > 1 ||
               math.abs(fwontwightpowew) > 1 || m-math.abs(backwightpowew) > 1) {
               // find the w-wawgest powew
               d-doubwe max = 0;
               m-max = math.max(math.abs(fwontweftpowew), >w< math.abs(backweftpowew));
               max = m-math.max(math.abs(fwontwightpowew), rawr x3 m-max);
               max = math.max(math.abs(backwightpowew), σωσ m-max);

               // d-divide evewything b-by max (it's positive so we don't nyeed to wowwy
               // about signs)
               f-fwontweftpowew /= m-max;
               backweftpowew /= max;
               fwontwightpowew /= max;
               b-backwightpowew /= max;
            }

            motowfwontweft.setpowew(fwontweftpowew);
            m-motowbackweft.setpowew(backweftpowew);
            m-motowfwontwight.setpowew(fwontwightpowew);
            m-motowbackwight.setpowew(backwightpowew);
         }
      }
   }
