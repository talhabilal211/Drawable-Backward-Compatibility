### Drawable Backward Compatibiity 
* Basically vector drawable are XML with set of ``lines`` , ``points`` and ``curves`` associated with color . They are used for maintaining image scalability , means they don't reduce their image quality with change of screen density . 
 * They do not have backward compatibility yet as we use ``Support Library`` , which is used for ``API Level 21 or hight`` so in that case we can import svg's to drawable 21 folder and same images( in PNG format ) to their associated folders . 
We publish the apk in playstore in bundle form so when apk is downloading it is decided what bundle your mobile requires according to its density and that apk has less size as actual 
* How can we place PNG and svg in drawbales ? Here is the Explaination.

Directory Name | Media Type 
-------------- | -------------
drawable | Put here all background drawable.
drawable-v21 | Put here all vertor drawables in ``svg's formate`` 
drawable-ldpi | put here ``ldpi`` images in PNG formate.
drawable-hdpi | put here ``hdpi`` images in PNG formate.
drawable-xhdpi | put here ``xhdpi`` images in PNG formate.
drawable-xxhdpi | put here ``xxhdpi`` images in PNG formate.
drawable-xxxhdpi | put here ``xxxhdpi`` images in PNG formate.
drawable-nodpi | put here those images which is not required for [pre-sclling](https://stackoverflow.com/a/34370735/6762459).
drawable-anydpi | put here those images whch has to be used if already exist in [other](https://stackoverflow.com/a/34370735/6762459) folder


 In simple words you just need to place all svg's to drawable-v21 folder so when your device desity meet to v21 or hight it will automatically access drawable from ``drawable-v21`` folder and if some drawable are to present in ``drawable-v21`` then they will be accessed from other folder automatically. 
