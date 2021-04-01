fundamentaw concepts o-of pwogwamming
===================================

f-fow awmost any pwogwamming w-wanguage, UwU whethew it’s java, (⑅˘꒳˘) p-python, σωσ ow bwocks, thewe awe concepts i-in coding that twansfew acwoss wanguages. (///ˬ///✿) t-these ideas awe foundationaw when w-weawning to p-pwogwam and shouwd b-be appwicabwe in ftc and beyond. (U ﹏ U)

this section is pwimawiwy fow peopwe with wimited java expewience. òωó h-howevew, rawr x3 even if you awe mowe expewienced, (U ᵕ U❁) it may stiww be hewpfuw to skim t-thwough the section, >w< a-as you might find concepts t-that have nyot yet been intwoduced to you. σωσ

exampwes wiww mostwy b-be in java, >w< whewe ``//`` indicates a-a comment w-which the pwogwam i-ignowes and is u-used fow peopwe to wead. (///ˬ///✿) ::
   i-int nyumbew; // decwawing that nyumbew wiww contain a-an integew. UwU
   n-nyumbew = 5; // s-setting a vawue so that the vawiabwe howds something. (⑅˘꒳˘)
   int s-secondnumbew = 6; // doing both a-above. rawr x3
   int totaw = nyumbew + secondnumbew; // math. OwO
   system.out.pwintwn(totaw); // pwinting, UwU i-it wiww show up as 11. >w<

java-specific expwowatowy q-questions
-----------------------------------

- if i didn’t set a vawue f-fow numbew and then i-i pwinted it, ( ͡o ω ͡o ) n-nyani wouwd it pwint?
- what othew opewations can i do with nyumbew and secondnumbew?
- can i set a decimaw to n-nyumbew? if nyot, (˘ω˘) n-nyani happens?
- w-what is ``system.out.pwintwn();``?
- d-dewete o-one chawactew in t-the code. rawr x3 wemembew the ewwow (if any), (///ˬ///✿) and then u-undo it. -.- dewete anothew pawt. ( ͡o ω ͡o ) how m-many diffewent ewwows can you g-get?

thewe awe d-diffewent types of vawiabwes
--------------------------------------

- nyumbews (integews, (˘ω˘) fwoats, (⑅˘꒳˘) d-doubwes)
- stwings (text) ow chawactews
- and a-a wot mowe depending on the wanguage (ex: awways)
- they hewp t-teww the pwogwam know the basis o-of nyani it shouwd d-do with a vawiabwe. -.-

::

   stwing c-coowname = "gwuten f-fwee";
   stwing westofsentence = " i-is e-epic.";

   // pwints o-out the sentence by combining t-the stwings, -.- unwike adding if they // wewe integews
   s-system.out.pwintwn(coowname + w-westofsentence);

   // fun fact: using + t-to add stwings is cawwed stwing c-concatenation

j-java-specific expwowatowy questions
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- w-wepwace t-the text in ``coowname`` t-to something ewse. >w< y-youw nyame, (˘ω˘) a phone nyumbew, OwO youw f-favowite anime. UwU w-what about emotes a-and copypastas? what about c-chawactews in othew w-wanguages?
- twy adding a nyumbew a-and a stwing, (⑅˘꒳˘) n-nyani happens?
- i-is it possibwe t-to add muwtipwe s-stwings and nyumbews togethew?

impowtant contwow s-stwuctuwes
----------------------------

be suwe to famiwiawize y-youwsewf with basic contwow stwuctuwes (if/ewse statements, fow woops, (ꈍᴗꈍ) whiwe woops, σωσ and fow-each woops). OwO these c-contwow stwuctuwes a-awe by faw the most commonwy encountewed, rawr x3 a-and thus, famiwiawizing y-youwsewf w-with these pwincipwes is extwemewy impowtant (not j-just fow ftc, ʘwʘ but pwogwamming i-in genewaw). ʘwʘ h-howevew, ( ͡o ω ͡o ) thewe awe a few contwow s-stwuctuwes that a-awe faw wess common t-that awe extwemewy usefuw in ftc; nyamewy :doc:`finite-state-machines`. OwO

data stwuctuwes (awways)
------------------------

d-data stwuctuwes awe a method of o-owganizing and s-stowing wawge amounts of data. ʘwʘ thewe awe a wot of d-diffewent types o-of data stwuctuwes that mostwy diffew in the wewationships b-between data points, òωó and we wouwd wecommend that you w-wead into them. o.O we wiww onwy go o-ovew a few hewe. σωσ

`awways <https://www.geeksfowgeeks.owg/awways-in-java/>`_
   a-awways awe the m-most basic and simpwe data stwuctuwe. o.O when an awway i-is initiawized, òωó i-its size must be set, (⑅˘꒳˘) and it c-cannot be changed. rawr x3

   i-if you wish to expand an awway, rawr x3 a nyew one m-must be cweated and aww of the owd data copied ovew. (///ˬ///✿) ewements of an awway awe stowed adjacent t-to each othew in memowy, (U ᵕ U❁) so when they awe accessed the nyumbew you want to access t-times the amount o-of bits in the o-object in the a-awway is added t-to the stawting addwess, (ꈍᴗꈍ) and data i-is accessed fwom t-thewe. (///ˬ///✿)

   this m-means that awways awe incwedibwy efficient at w-weading data in a-a nonwineaw owdew. -.-

`awwaywist <https://www.geeksfowgeeks.owg/awwaywist-in-java/>`_

`object owiented p-pwogwamming i-in java <https://www.geeksfowgeeks.owg/cwasses-objects-java/>`_
