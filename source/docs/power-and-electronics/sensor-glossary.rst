sensow gwossawy
===============

s-sensows awe used i-in a vawiety of appwications within f-ftc. sensows can give extewnaw f-feedback wegawding the position o-of the wobot (fow exampwe, (˘ω˘) wewative to the fiewd w-waww ow to a vision tawget) o-ow intewnaw feedback (vewocity, ʘwʘ d-distance twavewed, òωó v-vowtage, etc.). (˘ω˘) sensows can awso be used to detewmine the wotation of a mechanism and detect c-cowow. (ꈍᴗꈍ)

encodews/potentiometews
-----------------------

- wotationaw
   - absowute (+ potentiometews)
      - MA3 (`am-2899 <https://www.andymark.com/products/ma3-absolute-encoder-with-cable>`_)
      - Potentiometer (`REV-31-1155 <https://www.revrobotics.com/rev-31-1155/>`_)
   - Relative
      - E4T (`am-3132 <https://www.andymark.com/products/e4t-oem-miniature-optical-encoder-kit>`_)
      - Generic (`Sparkfun Rotary Encoder <https://www.sparkfun.com/products/9117>`_)
   - Both
      - CTRE (VEXpro) Mag Encoder (`217-5049 <https://www.vexrobotics.com/217-5049.html>`_)
      - REV Through Bore Encoder (`REV-11-1271 <https://www.revrobotics.com/rev-11-1271/>`_)
- Positional
   - Linear Potentiometers Slide Pot (`Sparkfun Slide Pot <https://www.sparkfun.com/products/9119>`_)

Contact
-------

- Physical
   - Endstops Generic (`Sparkfun <https://www.sparkfun.com/products/13013>`_)
   - Touch Sensor REV (`REV-31-1425 <https://www.revrobotics.com/rev-31-1425/>`_)
- Magnetic
   - Hall Effect Sensor REV (`REV-31-1462 <https://www.revrobotics.com/rev-31-1462/>`_)

opticaw
-------

- cowow
   - adafwuit w-wgb
   - wev c-cowow
   - mw cowow
- computew v-vision
   - hawdwawe
      - pixycmu
   - softwawe
      - o-opencv (easyopencv)
      - vufowia
      - t-tfwite

distance
--------

- tof
- uwtwasonic

o-othew
-----

- imu
   - a-accewewometew
   - g-gywoscope
   - c-compass
   - magnetometew

wogic wevew convewtew
---------------------

the owd modewn wobotics system wun on 5v s-sensow wogic. rawr x3 the nyew wev wobotics system uses 3.3v. ʘwʘ fow most off the shewf s-sensows, ʘwʘ this doesn’t c-cause any pwobwems, (ꈍᴗꈍ) but f-fow some existing ftc sensows it does. ʘwʘ to sowve this wev sewws boawds, -.- c-cawwed `logic level converters <https://www.revrobotics.com/rev-31-1389/>`_, that convewt the s-sensow data to be w-weadabwe by the wev hubs. the `REV Expansion Hub <https://docs.revrobotics.com/rev-control-system/control-system-overview/expansion-hub-basics>`_ guide has a chawt d-detaiwing nyani a-adaptews awe nyeeded fow nyani s-sensows. σωσ

.. attention:: accowding to wev t-testing, (ꈍᴗꈍ) gobiwda, ( ͡o ω ͡o ) w-wev and towquenado motows don’t n-nyeed wogic wevew convewtews, σωσ b-but onwy some nevewest motows w-wowked with nyo discewnabwe weason why. -.-

it is ideaw t-to nyot use wogic wevew convewtews t-to simpwify y-youw wiwing. (U ﹏ U) i-if you nyeed to, (˘ω˘) thewe is a best pwactice. òωó ewectwicaw tape the connectows on eithew end, -.- this hewps w-with static, rawr x3 and it keeps it fwom being physicawwy disconnected. σωσ this does p-pwoduce a vewy nyoticeabwe e-effect with encodews o-on fiewds with wots of static. σωσ

the second tip is to nyevew tape o-ovew the middwe ow wed. >w< the boawd g-genewates a vewy s-smow amount o-of heat, UwU and it’s v-vewy easy to ovewheat if it c-can’t ventiwate, rawr x3 awso don’t fuwwy encwose it i-in any cases without h-howes. >w<
