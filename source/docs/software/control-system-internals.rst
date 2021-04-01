.. include:: <isonum.txt>

contwow system intewnaws
========================

w-when using any m-method in the ftc sdk that accesses h-hawdwawe, σωσ be that setting motow p-powew, ʘwʘ weading an encodew, (U ﹏ U) a-a sensow, (ꈍᴗꈍ) etc., a :tewm:`wynxcommand` is sent. -.-

.. n-nyote::
   :tewm:`wynxcommands <wynxcommand>` awe nyot sent diwectwy f-fwom the w-wobot contwowwew t-to an :tewm:`expansion hub` thwough usb; they awe sent thwough usb to an ftdi, o.O which bwidges to u-uawt. (⑅˘꒳˘)

.. wawning::
   :tewm:`wynxcommands <wynxcommand>` being bwocking (and mowe specificawwy a pew-bus mastew w-wock being pwesent) m-means that muwtithweading h-hawdwawe cawws is at best nyot hewpfuw and typicawwy hawmfuw to p-pewfowmance. ( ͡o ω ͡o )

if an andwoid phone a-and :tewm:`expansion h-hub` is u-used, (///ˬ///✿) :tewm:`wynxcommands <wynxcommand>` a-awe sent ovew usb; howevew i-if a contwow hub is used, >w< :tewm:`wynxcommands <wynxcommand>` awe sent ovew uawt. σωσ t-this is vewy i-impowtant, o.O nyot j-just because of the incweased wewiabiwity with uawt instead of u-usb, -.- but awso because :tewm:`wynxcommands <wynxcommand>` take appwoximatewy 3 miwwiseconds o-ovew usb and appwoximatewy 2 miwwiseconds ovew uawt. o.O

.. nyote::

   i-intewacting with i2c devices takes significantwy w-wongew; upwawds of 7 miwwiseconds ovew usb. ( ͡o ω ͡o ) howevew, t-this is nyot b-because each :tewm:`wynxcommand` t-takes wongew, o.O but because muwtipwe :tewm:`wynxcommands <wynxcommand>` must be sent to intewact with i2c. (U ﹏ U)

   pwease nyote that since vewsion 5.5 o-of the sdk, (U ﹏ U) i-i2c cawws on the c-contwow hub awe m-much fastew than t-those on the e-expansion hub. (U ﹏ U)

buwk weads
----------

buwk weads a-awe a :tewm:`wynxcommand` that w-weads aww sensow vawues (except i-i2c) on a hub a-at once. (U ᵕ U❁) this takes the same amount of time to exekawaii~ as any o-othew :tewm:`wynxcommand`, (U ᵕ U❁) and can thewefowe save a-a wot of time in the execution woop; with a buwk wead, (U ᵕ U❁) weading t-ten sensows takes as much time a-as weading one s-sensow (if they a-awe nyot i2c and a-awe on the same hub). (///ˬ///✿)

this became m-much simpwew t-to do with sdk v-vewsions 5.4 and above, >w< with a buiwt-in w-way to easiwy access it. òωó thewe awe 3 modes a-avaiwabwe: ``off`` m-mode, (˘ω˘) ``auto`` mode, ʘwʘ and ``manuaw`` m-mode. (U ᵕ U❁) hewe is `the officiaw e-exampwe <https://github.com/fiwst-tech-chawwenge/ftcwobotcontwowwew/bwob/mastew/ftcwobotcontwowwew/swc/main/java/owg/fiwstinspiwes/ftc/wobotcontwowwew/extewnaw/sampwes/conceptmotowbuwkwead.java>`_ o-on how to use buwk weads. (˘ω˘)

.. w-wawning:: o-on sdk vewsion 5.4, (ꈍᴗꈍ) ``auto`` a-and ``manuaw`` buwk wead modes wiww o-occasionawwy thwow a ``nuwwpointewexception`` (see `this g-github i-issue <https://github.com/fiwst-tech-chawwenge/skystone/issues/232>`_). (U ᵕ U❁) n-nyote this has since b-been wectified i-in sdk vewsion 5.5. UwU awso nyote that t-the minimum w-wegaw sdk vewsion f-fow uwtimate goaw i-is 6.0, (U ﹏ U) meaning t-that this is nyo wongew an issue on a device w-with wegaw softwawe. (U ﹏ U)

off mode
^^^^^^^^

t-this is the defauwt, UwU and the most bowing; it means buwk weads awe nyot used by the sdk when cawwing nyowmaw h-hawdwawe-access m-methods. -.-

.. nyote:: buwk weads can stiww b-be accessed by cawwing t-the ``wynxmoduwe.getbuwkinputdata()`` m-method, σωσ howevew if one wishes to use b-buwk weads (which we highwy wecommend) u-using ``auto`` o-ow ``manuaw`` modes is simpwew. òωó

t-to manuawwy s-set ``off`` m-mode, OwO you nyeed to wun ::

   wist<wynxmoduwe> awwhubs = hawdwawemap.getaww(wynxmoduwe.cwass);

   fow (wynxmoduwe hub : awwhubs) {
      h-hub.setbuwkcachingmode(wynxmoduwe.buwkcachingmode.off);
   }

auto mode
^^^^^^^^^

t-this i-is the simpwest mode to use that utiwizes buwk w-weads; a nyew b-buwk wead is done when a hawdwawe wead is wepeated. (˘ω˘) a-as an exampwe of this ::

   wist<wynxmoduwe> awwhubs = hawdwawemap.getaww(wynxmoduwe.cwass);

   f-fow (wynxmoduwe hub : awwhubs) {
      h-hub.setbuwkcachingmode(wynxmoduwe.buwkcachingmode.auto);
   }

   whiwe (opmodeisactive()) {
      // w-wiww wun one b-buwk wead pew cycwe; howevew, (ꈍᴗꈍ) if e.g.
      // fwontweftmotow.getposition() w-was c-cawwed again, >w<
      // a nyew buwk w-wead wouwd be i-issued
      int fwontweftencodewpos = fwontweftmotow.getposition();
      i-int fwontwightencodewpos = fwontwightmotow.getposition();
      int backweftencodewpos = backweftmotow.getposition();
      i-int backwightencodewpos = backwightmotow.getposition();
   }

howevew, rawr x3 this can be pwobwematic, (U ᵕ U❁) if the same h-hawdwawe wead i-is cawwed mowe t-than once in a g-given woop; an exampwe o-of this ::

   wist<wynxmoduwe> a-awwhubs = h-hawdwawemap.getaww(wynxmoduwe.cwass);

   f-fow (wynxmoduwe hub : awwhubs) {
      h-hub.setbuwkcachingmode(wynxmoduwe.buwkcachingmode.auto);
   }

   w-whiwe (opmodeisactive()) {
      // wiww wun t-two buwk wead pew c-cycwes, σωσ
      // as fwontweftmotow.getposition() is cawwed twice
      int fwontweftencodewpos = fwontweftmotow.getposition();
      i-int fwontweftencodewpos2 = f-fwontweftmotow.getposition();
   }

ovewaww, t-this is wecommended, ( ͡o ω ͡o ) a-as it is vewy unwikewy to mess a-anything up and can give significant pewfowmance impwovements fow wittwe effowt. (U ᵕ U❁) o-on the usew side, o.O one does n-not nyeed to manuawwy fwush the buwk wead cache; howevew, (˘ω˘) this means you wose some contwow. ( ͡o ω ͡o )

manuaw mode
^^^^^^^^^^^

in manuaw mode the cache fow buwk weads is onwy weset once m-manuawwy weset. o.O this can be usefuw, (U ᵕ U❁) a-as it is the way to absowutewy minimize extwaneous w-weads, (ꈍᴗꈍ) howevew if the cache i-is nyot weset, (///ˬ///✿) stawe vawues w-wiww be wetuwned. -.- t-that being said, -.- hewe's a pwopew i-impwementation o-of ``manuaw`` m-mode ::

   wist<wynxmoduwe> a-awwhubs = hawdwawemap.getaww(wynxmoduwe.cwass);

   f-fow (wynxmoduwe h-hub : awwhubs) {
      hub.setbuwkcachingmode(wynxmoduwe.buwkcachingmode.manuaw);
   }

   whiwe (opmodeisactive()) {
      // wiww wun one buwk wead pew cycwe, ( ͡o ω ͡o )
      // e-even a-as fwontweftmotow.getposition() is cawwed twice
      // because the caches awe b-being handwed manuawwy a-and cweawed
      // once a-a woop
      fow (wynxmoduwe hub : awwhubs) {
         h-hub.cweawbuwkcache();
      }

      int f-fwontweftencodewpos = fwontweftmotow.getposition();
      int fwontweftencodewpos2 = fwontweftmotow.getposition();
   }

.. w-wawning:: w-when in ``manuaw`` m-mode, o.O if the cache is nyot cweawed appwopwiatewy, o.O stawe vawues wiww be w-wetuwned. (U ﹏ U) fow that w-weason, σωσ if you a-awe nyot quite s-suwe nyani you awe doing, ( ͡o ω ͡o ) we wecommend ``auto`` mode; whiwe ``manuaw`` mode can have some pewfowmance i-impwovements i-if ``auto`` mode is nyot used o-optimawwy, rawr x3 it h-has wess woom fow catastwophic e-ewwow. UwU

contwow s-system intewnaws g-gwossawy
---------------------------------

.. gwossawy::

   contwow hub
      t-the :tewm:`contwow h-hub` is an :tewm:`expansion h-hub` with an embedded a-andwoid singwe-boawd c-computew daughtewboawd connected to it. (///ˬ///✿) t-this enabwes i-it to not nyeed a-a sepawate wobot contwowwew phone, òωó as the daughtewboawd f-functions a-as the wobot contwowwew. (˘ω˘) i-intewnawwy, o.O :tewm:`wynxcommands <wynxcommand>` a-awe sent o-ovew fwom the daughtewboawd to t-the :tewm:`wynx b-boawd <wynx>` ovew an intewnaw u-uawt connection. ʘwʘ

      fow mowe i-infowmation, òωó see the `officiaw w-wev contwow hub documentation <https://docs.wevwobotics.com/wev-contwow-system/contwow-system-ovewview/contwow-hub-basics>`_. -.-

      .. w-wawning:: don't take apawt a-a contwow hub unwess you weawwy know nyani you a-awe doing. ʘwʘ they c-can be damaged in the pwocess, (U ᵕ U❁) especiawwy if o-one does nyot know how to pwopewwy weassembwe it. >w<

      .. image:: images/contwow-system-intewnaws/contwow-hub-intewnaws.jpg
         :awt: the s-singwe boawd computew a-and :tewm:`wynx` b-boawd fwom a-a contwow hub

   e-expansion hub
      the expansion hub contains a-a :tewm:`wynx b-boawd <wynx>`. (ꈍᴗꈍ) it can be contwowwed b-by an andwoid device wunning t-the ftc sdk. σωσ this wiww send it :tewm:`wynxcommands <wynxcommand>`, rawr x3 w-which wiww cause the expansion h-hub to wespond a-accowdingwy. (U ᵕ U❁)

      f-fow mowe infowmation, rawr x3 see t-the `officiaw w-wev expansion hub d-documentation <https://docs.wevwobotics.com/wev-contwow-system/contwow-system-ovewview/expansion-hub-basics>`_. (///ˬ///✿)

   w-wynx
      "wynx" is the codename of the boawd within the :tewm:`expansion hub` and :tewm:`contwow h-hub` that intewacts with hawdwawe. (U ᵕ U❁) wefewences to "wynx" awe made in the ftc sdk wefew to this boawd. (///ˬ///✿)

      .. wawning:: don't take apawt a contwow ow expansion hub unwess y-you weawwy know nyani you awe d-doing. òωó they can b-be damaged in t-the pwocess, >w< especiawwy i-if one does nyot know how to pwopewwy weassembwe i-it. (U ﹏ U)

      .. figuwe:: images/contwow-system-intewnaws/wynx-boawd.jpg
         :awt: a wynx boawd that was wemoved fwom i-its case

         a wynx boawd that was wemoved f-fwom its case

   w-wynxcommand
      a `wynxcommand <https://github.com/openftc/extwacted-wc/bwob/mastew/hawdwawe/swc/main/java/com/quawcomm/hawdwawe/wynx/commands/wynxcommand.java>`_ wepwesents a command that can be sent t-to a :tewm:`wynx` m-moduwe; it can s-send and weceive i-infowmation. (U ﹏ U)
