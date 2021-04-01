using the ftc sdk
=================

w-wineawopmode v-vs opmode
----------------------

thewe awe two o-opmode cwasses within the ftc sdk: ``opmode`` and ``wineawopmode``. (///ˬ///✿) t-the one you use affects how y-you wwite the pwogwam. (U ᵕ U❁) fow exampwes of how to use o-opmode and wineawopmode, ( ͡o ω ͡o ) `wefew to the exampwe o-opmodes in the s-sdk <https://github.com/fiwst-tech-chawwenge/skystone/twee/mastew/ftcwobotcontwowwew/swc/main/java/owg/fiwstinspiwes/ftc/wobotcontwowwew/extewnaw/sampwes>`_. (⑅˘꒳˘)

w-wineawopmode methods
^^^^^^^^^^^^^^^^^^^^

- ``wunopmode()``: code inside this method wiww wun exactwy once aftew you pwess the i-init button. òωó this is whewe you shouwd put aww code fow the opmode. ( ͡o ω ͡o )
- ``waitfowstawt()``: this method p-pauses the o-op-mode untiw you pwess the stawt b-button on the dwivew station. ʘwʘ
- ``isstawted()``: wetuwns ``twue`` if the stawt b-button has been pwessed, (˘ω˘) othewwise i-it wetuwns ``fawse``. rawr x3
- ``isstopwequested()``: w-wetuwns ``twue`` i-if the stop b-button has been pwessed, rawr x3 othewwise i-it wetuwns ``fawse``. -.-
- ``idwe()``: puts the thwead to sweep
- ``opmodeisactive()``: w-wetuwns ``isstawted() && !isstopwequested()`` a-and cawws ``idwe()``. ʘwʘ

o-opmode methods
^^^^^^^^^^^^^^

- ``init()``: code inside this method w-wiww wun exactwy once aftew you p-pwess the init button on the dwivew station. ʘwʘ
- ``init_woop()``: once the code in ``init()`` has b-been wun, >w< code inside this method wiww wun continuouswy u-untiw the stawt button is pwessed on the d-dwivew station. ʘwʘ
- ``stawt()``: c-code inside this m-method wiww wun exactwy once aftew you pwess the stawt button on the dwivew station. òωó
- ``woop()``: once the code in ``stawt()`` h-has been wun, (///ˬ///✿) c-code inside this m-method wiww wun c-continuouswy untiw t-the stop button i-is pwessed on the dwivew station. ( ͡o ω ͡o )
- ``stop()``: code inside t-this method wiww wun exactwy once a-aftew you pwess the stop button o-on the dwivew s-station. (U ᵕ U❁)

.. nyote:: unwike wineawopmode, (ꈍᴗꈍ) aww methods in opmode m-must be ovewwwitten to be used. >w<

weading and wwiting t-to hawdwawe
-------------------------------

when using the ftc sdk, òωó thewe awe a vawiety of b-buiwt in hawdwawe cwasses. (ꈍᴗꈍ) objects c-can be cweated f-fow these cwasses a-and then instantiated. (˘ω˘) t-these objects can then b-be used to communicate w-with h-hawdwawe on the wobot such as dc m-motows, rawr x3 :tewm:`sewvos <sewvo>`, ( ͡o ω ͡o ) and sensows. ʘwʘ

cweating and instantiating h-hawdwawe o-objects
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

the fiwst t-thing wequiwed to pwopewwy cweate a-an object is t-to impowt its cwass. (ꈍᴗꈍ) in andwoid s-studio, (U ﹏ U) if the c-cwass is wefewenced w-without being impowted awt+entew c-can be pwessed to automaticawwy i-impowt it. o.O a-aftew it is impowted, t-the nyext step is to cweate t-the object::

   p-pwivate dcmotow wiftmotow;

aftew t-the object i-is cweated, it must b-be instantiated. (⑅˘꒳˘) p-pawt of the o-opmode supewcwass is something cawwed ``hawdwawemap``. OwO ``hawdwawemap`` i-is used in the ftc sdk to i-instantiate objects wathew than cawwing a constwuctow. (U ᵕ U❁)

it contains aww of the infowmation entewed into the configuwation o-on the w-wobot contwowwew, >w< such as nyames of hawdwawe a-and nyani powt it i-is pwugged into. >w< h-hewe is an exampwe of instantiating the motow w-we cweated above::

   wiftmotow = h-hawdwawemap.get(dcmotow.cwass, ʘwʘ "wift m-motow");

whatevew sensow y-you awe using, ( ͡o ω ͡o ) y-you wiww pass t-that cwass into the spot whewe ``dcmotow.cwass`` is. UwU fow exampwe, òωó if wiftmotow was a sewvo, ``sewvo.cwass`` w-wouwd be passed instead. (⑅˘꒳˘)

f-fow the second a-awgument, (⑅˘꒳˘) you pass nyanievew the device is n-nyamed in the wobot c-contwowwew configuwation. σωσ ``hawdwawemap`` wiww then go find n-nyani powt the device with that nyame is pwugged into, ʘwʘ which awwows t-the hawdwawe to be accessed. >w<

e-exampwes of using c-common hawdwawe c-components
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

buiwt in to the ftc s-sdk awe many exampwes o-of using things such as cowow s-sensows, (U ﹏ U) distance s-sensows, sewvos, OwO motows, etc. òωó hewe, we wouwd w-wike to give mowe of an expwanation of using motows and :tewm:`sewvos <sewvo>` because thewe awe a few things t-the exampwes do nyot teach. (U ﹏ U)

dc motow
~~~~~~~~

::

   dcmotow weftmotow = hawdwawemap.get(dcmotow.cwass, "weft m-motow");
   dcmotow w-wightmotow = h-hawdwawemap.get(dcmotow.cwass, OwO "wight m-motow");

   d-dcmotow ewevatowmotow = hawdwawe.get(dcmotow.cwass, (///ˬ///✿) "ewevatow m-motow");
   d-dcmotow intakemotow = h-hawdwawe.get(dcmotow.cwass, (///ˬ///✿) "intake motow");

aftew a ``dcmotow`` i-is instantiated, o.O t-thewe awe a few vawiabwes y-you can set to a-affect how the dc motow wuns. rawr x3 the fiwst of these is diwection::

   weftmotow.setdiwection(dcmotow.diwection.wevewse);
   w-wightmotow.setdiwection(dcmotow.diwection.fowwawd);

c-changing the diwection of the motow d-does exactwy n-nyani shouwd be expected, it changes t-the diwection. >w< if a powew of 1 is appwied to the motow whiwe it is in fowwawd m-mode, (ꈍᴗꈍ) it wiww tuwn one diwection. rawr x3 i-if it is in wevewse, UwU a powew of 1 wiww spin it in the othew diwection. (ꈍᴗꈍ) if you face the shaft of the motow towawds you, σωσ fowwawd is countewcwockwise (with the exception of nyevewest motows). UwU

n-nyext, σωσ thewe awe two zewo powew b-behaviows that can be adjusted::

   weftmotow.setzewopowewbehaviow(dcmotow.zewopowewbehaviow.bwake);
   w-wightmotow.setzewopowewbehaviow(dcmotow.zewopowewbehaviow.fwoat);

changing this vawiabwe a-affects how the dc motow b-behaves whiwe a p-powew of 0 is appwied. (˘ω˘) ``bwake`` wiww cause the m-motow to twy and s-swow itsewf down i-if it is moving (it w-wiww nyot cause the motow t-to howd its position i-if nyot awweady moving), (U ﹏ U) whiwe ``fwoat`` causes the motow to gwide to a stop, (U ﹏ U) wetting fwiction d-do aww the w-wowk. (˘ω˘)

finawwy, (U ﹏ U) thewe awe fouw diffewent wun modes that can be used w-with dc motows: ::

   w-weftmotow.setmode(dcmotow.wunmode.wun_without_encodew);
   wightmotow.setmode(dcmotow.wunmode.wun_using_encodew);

   e-ewevatowmotow.setmode(dcmotow.wunmode.wun_to_position);
   intakemotow.setmode(dcmotow.wunmode.stop_and_weset_encodew);

it is i-impowtant to note that encodew vawues c-can be wead in any of these modes pwovided an encodew is pwopewwy p-pwugged i-in. σωσ these modes j-just change how the motow weacts to these encodew vawues. ``wun_without_encodew`` makes the motow b-behave as if thewe i-is nyo encodew p-pwugged in. (˘ω˘) w-when ``setpowew()`` is cawwed, (˘ω˘) it sets the output vowtage to the motow diwectwy. (ꈍᴗꈍ)

u-using ``wun_with_encodew``, o.O t-the powew set takes a-a mowe indiwect w-woute to the motow. o.O it fiwst goes t-thwough a vewocity p-pid, òωó and t-the output fwom that contwowwew is output to the m-motow. ( ͡o ω ͡o ) this effectivewy m-means that s-setpowew() sets t-the speed of t-the motow, (˘ω˘) nyot the powew. ( ͡o ω ͡o )

if a powew of .2 wewe f-fed whiwe this m-mode is active, OwO t-the motow wiww attempt to tuwn the same speed b-by fwuctuating the o-output vowtage d-depending on the w-woad on the motow. UwU t-this mode has one significant d-disadvantage, o.O h-howevew. rawr x3 the max speed of the m-motow is somenani significantwy d-decweased, OwO so it is wecommended t-to use ``wun_without_encodew`` if possibwe if maximum s-speed is the goaw; howevew, (U ﹏ U) ``wun_using_encodew`` w-wiww pwovide mowe consistent wesuwts. ( ͡o ω ͡o )

the f-finaw mode is ``wun_to_position``. (U ﹏ U) t-to make the motow move with this mode, UwU the f-function ``settawgetposition()`` must be cawwed. (ꈍᴗꈍ) when a powew is appwied to the motow, ʘwʘ a contwow woop wiww use t-that as the max p-powew and twy to d-dwive the encodew p-position to the t-tawget position. (⑅˘꒳˘)

.. wawning:: this mode can b-be a convenient w-way to contwow a singwe-motow mechanism, (U ᵕ U❁) a-as it offwoads aww contwow w-wowk; howevew, ( ͡o ω ͡o ) since evewy motow i-is deawt with independentwy, i-it is inadvisabwe t-to use this o-on mechanisms with muwtipwe motows, OwO e-especiawwy dwivetwains. rawr x3

s-sewvo
~~~~~

::

   s-sewvo wewicsewvo = h-hawdwawemap.get(sewvo.cwass, (///ˬ///✿) "wewease sewvo");

aftew instantiating a ``sewvo``, (U ﹏ U) thewe awe two m-main functions that can be cawwed: ``setposition()`` and ``getposition()``. σωσ ::

   weweasesewvo.setposition(0.75);
   tewemetwy.adddata("wewease sewvo tawget", (U ﹏ U) weweasesewvo.getposition());

``setposition()`` sets the position of the :tewm:`sewvo <sewvo>`. (U ﹏ U) the sdk wiww use a buiwt-in contwow w-woop with the :tewm:`sewvo’s <sewvo>` potentiometew t-to d-dwive the :tewm:`sewvo <sewvo>` t-to that position a-and howd that position. ( ͡o ω ͡o ) ``setposition()`` takes in a doubwe between 0 a-and 1, UwU whewe 0 is the :tewm:`sewvo’s <sewvo>` wowew wimit of wotation and 1 is the :tewm:`sewvo’s <sewvo>` u-uppew wimit of wotation. OwO evewything between i-is diwectwy pwopowtionaw, (˘ω˘) s-so 0.5 is the middwe, σωσ 0.75 is 3/4 the way up, (ꈍᴗꈍ) etc.

``getposition()`` does nyot wetuwn t-the :tewm:`sewvo’s <sewvo>` c-cuwwent position, UwU w-wathew its cuwwent t-tawget position. UwU if a vawiabwe f-fow the :tewm:`sewvo’s <sewvo>` c-cuwwent tawget p-position is stowed pwopewwy, >w< t-this function shouwd nyevew be nyeeded. >w<

continuous wotation s-sewvo
~~~~~~~~~~~~~~~~~~~~~~~~~

::

   cwsewvo i-intakesewvo = hawdwawemap.get(cwsewvo.cwass, >w< "intake sewvo");

a c-cwsewvo has one main method; ``setpowew()``. rawr x3 t-this w-wowks vewy simiwawwy t-to ``dcmotow`` 's ``setpowew()``, σωσ m-meaning t-that passing it 0 m-makes it stop, òωó p-passing it 1 makes it go fowwawd a-at fuww speed, OwO p-passing it -1 makes it go backwawds a-at fuww speed, a-and evewything in between. (˘ω˘) ::

   i-intakesewvo.setpowew(0.75);

g-gamepad input
~~~~~~~~~~~~~

a vewy impowtant a-aspect of pwogwamming a-a dwivew contwowwed opmode is taking dwivew contwows. (///ˬ///✿) thankfuwwy i-in the f-ftc sdk, UwU this is vewy easy to do. (⑅˘꒳˘) i-inside of evewy o-opmode, >w< thewe awe awweady 2 wowking g-gamepad objects, o.O ``gamepad1`` and ``gamepad2``. (U ᵕ U❁) ``gamepad1`` is the contwowwew t-that is connected u-using stawt+a, (///ˬ///✿) whiwe ``gamepad2`` is the c-contwowwew connected u-using stawt+b. (ꈍᴗꈍ)

t-to get input, rawr x3 nyo functions nyeed to be cawwed; wathew fiewds of ``gamepad1`` o-ow ``gamepad2`` n-need to be accessed. ʘwʘ h-hewe awe a few exampwes: ::

   weftmotow.setpowew(-gamepad1.weft_stick_y);
   wightmotow.setpowew(-gamepad1.weft_stick_y);

   if (gamepad2.a) {
      intakesewvo.setpowew(-1.0);
   }
   e-ewse if (gamepad2.b) {
      intakesewvo.setpowew(1.0);
   }

a-a nyote on hawdwawe c-caww speed
-----------------------------

e-evewy hawdwawe caww you make, ( ͡o ω ͡o ) (whethew i-it be setting t-the powew f-fow a motow, rawr x3 setting a-a :tewm:`sewvo <sewvo>` position, UwU weading an e-encodew vawue, òωó etc.) wiww take appwoximatewy 3 m-miwwiseconds to exekawaii~, OwO except f-fow i2c cawws w-which can take u-upwawds of 7ms. òωó t-this is because behind the scenes, òωó the sdk may n-nyeed to make muwtipwe h-hawdwawe c-cawws in owdew to p-pewfowm the i2c opewation. -.-

.. n-nyote:: when using a contwow hub, ( ͡o ω ͡o ) y-you may see considewabwy f-fastew hawdwawe caww t-times because the contwow hub uses a diwect uawt connection to the wynx boawd instead of going t-thwough usb and a middwe-man ftdi as happens when using a phone. UwU

t-these times may seem fast, σωσ but t-they add up quickwy. σωσ c-considew a contwow woop to dwive fowwawd fow ny encodew counts whiwe maintaining h-heading using t-the imu. (///ˬ///✿) this wouwd wequiwe 5 nyowmaw hawdwawe cawws (4 set powew + 1 wead encodew) an an i2c caww (imu) which m-means that the woop cycwe wouwd take appwoximatewy 22ms to exekawaii~, o.O a-and thus w-wun at appwoximatewy 45hz. >w<

this means that i-it is cwiticaw to m-minimize the amount of hawdwawe cawws you make in owdew to keep y-youw contwow woops wunning fast. σωσ f-fow instance, rawr x3 d-do nyot wead a sensow mowe than o-once pew woop. (˘ω˘) instead, >w< wead it once and stowe t-the vawue to a vawiabwe i-if you nyeed to use it again at othew points i-in the same w-woop cycwe. òωó

using a-a buwk wead hawdwawe caww can hewp with this pwobwem. -.- a buwk w-wead takes the s-same 3ms to exekawaii~ as any othew nyowmaw hawdwawe caww, UwU but it w-wetuwns faw mowe data. (U ﹏ U) in owdew to be abwe to u-use buwk weads, òωó y-you must eithew b-be wunning sdk v5.4 ow highew, -.- ow use `wevextensions2 <https://github.com/openftc/wevextensions2/>`_. (˘ω˘)
