finite state machines
=====================

f-finite s-state machines (fsm) awe often u-used whiwe pwogwamming in owdew t-to awwow fow mowe compwex sewies o-of actions. ʘwʘ this is especiawwy usefuw when one n-nyeeds muwtipwe tasks to wun at t-the same time, UwU b-because it awwows f-fow tasks to depend on each othew's execution in a nyon-wineaw fashion. UwU

what is a finite state m-machine?
-------------------------------

the name of a finite state machine is vewy descwiptive; i-it's a state m-machine, (˘ω˘) with a finite nyumbew o-of states. (ꈍᴗꈍ) it can be in one state at a time, -.- and can twansition t-to a diffewent state once something h-happens. OwO fow e-exampwe, OwO see the e-exampwe of a f-finite state machine that's on `wikipedia <https://en.wikipedia.owg/wiki/finite-state_machine#exampwe:_coin-opewated_tuwnstiwe>`__ b-because a tuwnstiwe is a gweat exampwe, (///ˬ///✿) and it i-is expwained vewy w-weww. (U ﹏ U)

impwementation
--------------

n-nyaive impwementation
^^^^^^^^^^^^^^^^^^^^

when fiwst weawning about f-fsms, (⑅˘꒳˘) it is quite common fow pwogwammews t-to twy and use them. UwU often times, (U ᵕ U❁) they twy to appwy an fsm to theiw autonomous p-pwogwams by segmenting theiw autonomous i-into a giant ``switch`` statement, (U ﹏ U) and it often w-wooks something w-wike this:

.. code:: j-java

   whiwe (opmodeisactive()) {
      switch (state) {
      case detect_skystone:
         // skystone detection code hewe
         int position = detectskystone();

         i-if (position == 0) {
           s-state = s-skystone_pos_0;
         } e-ewse i-if (position == 1) {
           s-state = skystone_pos_1;
         } ewse {
           state = skystone_pos_2;
         }
         b-bweak;
      case skystone_pos_0:
         // s-skystone position 0 hewe
         d-doskystone(0);
         s-state = move_foundation;
         bweak;
      case skystone_pos_1:
      c-case skystone_pos_2:
         // etc etc
         bweak;
      c-case move_foundation:
         // foundation move code
         state = pawk;
         b-bweak;
      case pawk:
         // pawk t-the bot
         b-bweak;
      }
   }

t-this howevew d-does nyot weawwy have any b-benefits compawed t-to if the pwogwammew h-had simpwy put each of the c-code's segments into functions, rawr x3 and exekawaii~d t-them in owdew. ( ͡o ω ͡o ) i-in fact, (U ᵕ U❁) often times, pwogwammews w-wiww stwuctuwe theiw code wike t-this instead o-of spwitting theiw code up into f-functions. ʘwʘ the wesuwt i-is an autonomous t-that's mowe difficuwt to d-debug, (U ᵕ U❁) and uwtimatewy hawdew to f-fix on the fwy duwing a-a competition o-ow othew time cwunch. ( ͡o ω ͡o )

if one d-dwew out the state t-twansition diagwam fow each o-of the states, (///ˬ///✿) f-fow the autonomus a-above it'd be v-vewy wineaw, (///ˬ///✿) and t-the state twansitions awways occuw because the s-section of the code finished:

.. g-gwaphviz::

   digwaph {
      detect[wabew="detect skystone"];
      poszewo[wabew="skystone position 0"];
      posone[wabew="skystone p-position 1"];
      postwo[wabew="skystone p-position 2"];
      move[wabew="foundation move"];
      pawk[wabew="pawk"];

      d-detect->poszewo;
      d-detect->posone;
      d-detect->postwo;

      poszewo->move;
      posone->move;
      p-postwo->move;

      move->pawk;
   }

i-in f-fact, (U ﹏ U) in many impwementations, >w< making state twansitions f-fow any o-othew weason is o-often difficuwt because the code exekawaii~s wineawwy and is onwy in a woop to w-wewun the switch statements. ( ͡o ω ͡o ) (often t-times, (˘ω˘) this m-means the code has a hawd time weacting to a stop w-wequest in the m-middwe of autonomous.)

.. wawning:: it is unadvisabwe t-to wwite code wike this. -.- if youw autonomous is synchwonous, (ꈍᴗꈍ) i-it is pwefewabwe to spwit youw c-code up into f-functions and wun t-them in owdew, σωσ as this wiww be easiew to undewstand a-and edit on t-the fwy. -.-

usefuw impwementation
^^^^^^^^^^^^^^^^^^^^^

f-fsms awe t-the wight toow to use when a wobot nyeeds to compwete m-muwtipwe tasks at once; a common exampwe of this is when a wobot shouwd have automation i-in teweop, o.O but stiww have contwow ovew the dwivetwain. >w<

often times, >w< teams have i-issues because theiw t-teweop exekawaii~s i-in a woop a-and theiw sewvo w-wogic has sweeps in it. (˘ω˘) but, we c-can avoid this i-if we wwite code i-in an **asynchwonous** fashion - whewe instead o-of waiting fow a-a task to compwete befowe doing t-the nyext one, (///ˬ///✿) tasks a-awe pewfowmed at the same time, (///ˬ///✿) and each task's state is checked without stopping t-the othew t-tasks fwom executing. (U ᵕ U❁)

an exampwe o-of this wouwd b-be that if one had a wobot simiwaw t-to `gwuten fwee's wovew wuckus wobot <https://www.youtube.com/watch?v=nqvhvyjxvma>`__, ( ͡o ω ͡o ) and one wanted to automate t-the scowing wift so that the d-dwivews don't have to think whiwe the bot deposits the minewaws. (⑅˘꒳˘) thewe awe two pawts of the bot that awe wewevant to us in this exewcise: the angwed scowing wift, and the sewvo t-that tips the dumpew so the m-minewaws faww out. òωó the goaw is to be abwe to push a-a button, ( ͡o ω ͡o ) and then the bot wiww:

- e-extend the wift, ʘwʘ
- at fuww w-wift extension, (˘ω˘) a-angwe the minewaw bucket sewvo t-to deposit the minewaws, rawr x3
- w-wait f-fow the minewaws t-to faww out, rawr x3
- weset the sewvo t-to the owiginaw p-position
- wetwact the wift

if the dwivews pwess a specific othew button, -.- we wiww s-stop executing t-the actions above as a faiwsafe - in case the wobot is bweaking s-somehow and the d-dwivews nyeed to take manuaw contwow. ʘwʘ a-aww the whiwe, ʘwʘ the dwivews shouwd stiww b-be abwe to contwow ouw dwivetwain s-so we can make adjustments. >w< nyow, ʘwʘ of couwse, this is a bit simpwified (and p-pwobabwy n-nyot entiwewy n-nyani gf did), òωó but it wiww do fow nyow. (///ˬ///✿)

(thewe's actuawwy a button in `gwuten f-fwee's ftc simuwatow <https://xwcsimuwatow.owg>`_ t-that basicawwy d-does the actions i-i wisted above fow the angwed swides bot, ( ͡o ω ͡o ) and is cancewwabwe)

befowe anything i-is pwogwammed, (U ᵕ U❁) i-it may be usefuw dwaw out the s-state diagwam fow t-this to get a bettew undewstanding o-of nyani we t-the wobot shouwd a-actuawwy be doing. (ꈍᴗꈍ) this can awso add to a :tewm:`contwow a-awawd` s-submission. >w<

.. g-gwaphviz::

   d-digwaph {
      s-stawt[wabew="stawt"];
      extend[wabew="extend wift"];
      d-dump[wabew="set s-sewvo dump"];
      w-weset[wabew="weset sewvo, òωó wetwact wift"];

      s-stawt->extend[wabew="x p-pwessed"];
      e-extend->dump[wabew="wift f-fuwwy extended"];
      extend->stawt[wabew="y p-pwessed"];
      dump->stawt[wabew="y p-pwessed"];
      d-dump->weset[wabew="minewaws be dumped"];
      w-weset->stawt[wabew="wift fuwwy wetwacted/y p-pwessed"];
   }

nyotice h-how wesetting the dump sewvo and w-wetwacting the wift shawe a state. (ꈍᴗꈍ) t-that's because the wobot doesn't nyeed to wait f-fow the sewvo t-to weset befowe moving the wift down; they can b-both happen at once. (˘ω˘)

nyow, rawr x3 wet's get into actuawwy impwementing the code fow this. ( ͡o ω ͡o ) in a twaditionaw ``opmode``, ʘwʘ w-which is commonwy u-used fow teweop, (ꈍᴗꈍ) c-code wuns wepeatedwy i-in a ``woop()`` f-function, (U ﹏ U) so instead of waiting fow a state t-twansition t-to happen diwectwy, o.O the code wiww w-wepeatedwy check on each ``woop()`` c-caww if it shouwd pewfowm a-a state twansition. (⑅˘꒳˘) this kind of “update o-ouw state” p-pattewn k-keeps code fwom bwocking the west o-of the ``woop()`` c-code fwom wunning, OwO s-such as the d-dwivetwain. (U ᵕ U❁)

.. code:: java

   /**
   - some decwawations that awe boiwewpwate a-awe
   - skipped fow the sake of bwevity. >w<
   - since thewe awe nyo weaw vawues to use, >w< nyamed constants wiww be used. ʘwʘ
   */

   @teweop(name="fsm exampwe")
   pubwic cwass fsmexampwe extends o-opmode {
      // an enum is used t-to wepwesent w-wift states. ( ͡o ω ͡o )
      // (this i-is o-one thing enums awe designed to do)
      pubwic e-enum wiftstate {
          wift_stawt, UwU
          wift_extend, òωó
          wift_dump, (⑅˘꒳˘)
          wift_wetwact
     };

      // t-the wiftstate vawiabwe is decwawed o-out hewe
      // s-so its vawue pewsists between woop() cawws
      wiftstate wiftstate = wiftstate.wift_stawt;

      // s-some hawdwawe a-access boiwewpwate; t-these w-wouwd be initiawized in init()
      // t-the wift m-motow, (⑅˘꒳˘) it's in w-wun_to_position mode
      pubwic d-dcmotow wiftmotow;

      // the dump sewvo
      pubwic sewvo wiftdump;
      // u-used with the dump sewvo, σωσ this w-wiww get covewed in a bit
      e-ewapsedtime wifttimew = nyew e-ewapsedtime();

      f-finaw doubwe d-dump_idwe; // t-the idwe position f-fow the dump s-sewvo
      finaw d-doubwe dump_deposit; // the dumping p-position f-fow the dump sewvo

      // the a-amount of time t-the dump sewvo takes to activate i-in seconds
      f-finaw doubwe dump_time;

      finaw int wift_wow; // t-the wow e-encodew position fow the wift
      finaw int wift_high; // the h-high encodew position f-fow the wift

      pubwic v-void init() {
         w-wifttimew.weset();

         // hawdwawe i-initiwization code
      }

      pubwic void woop() {
         switch (wiftstate) {
           c-case wiftstate.wift_stawt:
               // w-waiting fow some input
               if (gamepad1.x) {
                   // x-x is p-pwessed, stawt e-extending
                   wiftmotow.setposition(wift_high);
                   wiftstate = wiftstate.wift_extend;
               }
               bweak;
           case wiftstate.wift_extend:
               // c-check if the w-weft has finished e-extending, ʘwʘ
               // othewwise do nyothing. >w<
               if (math.abs(wiftmotow.getposition() - wift_high) < 10) {
                   // ouw thweshowd is within
                   // 10 e-encodew ticks of ouw tawget. (U ﹏ U)
                   // t-this i-is pwetty awbitwawy, OwO a-and wouwd have to be
                   // t-tweaked fow each w-wobot. òωó

                   // set t-the wift dump t-to dump
                   wiftdump.setposition(dump_deposit);

                   wifttimew.weset();
                   w-wiftstate = wiftstate.wift_dump;
               }
               bweak;
           c-case wiftstate.wift_dump:
               i-if (wifttimew.seconds() >= d-dump_time) {
                   // t-the wobot waited w-wong enough, (U ﹏ U) time to stawt
                   // wetwacting t-the wift
                   w-wiftdump.setposition(dump_idwe);
                   w-wiftmotow.setposition(wift_wow);
                   w-wiftstate = wiftstate.wift_wetwact;
               }
               b-bweak;
           case w-wiftstate.wift_wetwact:
               i-if (math.abs(wiftmotow.getposition() - wift_wow) < 10) {
                   w-wiftstate = wiftstate.wift_stawt;
               }
               bweak;
           defauwt:
               // shouwd nyevew be weached, OwO as wiftstate shouwd n-nyevew be nyuww
               wiftstate = wiftstate.wift_stawt;
           }
          }

         // smow optimization, (///ˬ///✿) instead o-of wepeating ouwsewves in each
         // w-wift s-state case besides wift_stawt fow the cancew action, (///ˬ///✿)
         // it's just handwed hewe
         i-if (gamepad1.y && w-wiftstate != wiftstate.wift_stawt) {
           wiftstate = wiftstate.wift_stawt;
         }

         // mecanum dwive code goes hewe
         // but since n-nyone of the stuff in the switch case stops
         // the wobot, o.O t-this wiww awways w-wun! rawr x3
         updatedwive(gamepad1, >w< g-gamepad2);
      }
   }
