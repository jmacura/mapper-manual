---
title: Aplikace Mapper pro Android
authors:
  - Kai Pastor
  - Thomas Schoeps
keywords: Android
edited: 4. září 2018
redirect_from:
  - /android/
  - '/Android Manual/'
  - /mapper-manual/pages/android-index.html
---

## Úvodní informace

Verze aplikace OpenOrienteering Mapper pro systém Android není tak intuitivní jako
verze pro počítače, proto si prosím přečtěte tyto důležité informace.

[Požadavky a doporučení na zařízení](android-requirements.md){: .subpage}

[Příprava mapy na PC](android-pc.md){: .subpage}

[Ukládání map a podkladů na zařízeních se systémem Android](android-storage.md){: .subpage}

{% if doxygen %}
**Poznámka:** [online verze](https://www.openorienteering.org/mapper-manual/) této příručky (anglicky) může obsahovat více informací a opravy.
{% endif %}


## Používání aplikace Mapper

Po spuštení aplikace se zobrazí seznam mapových souborů dostupných na [podporovaných umístěních k ukládání](android-storage.md). K úpravě mapy stiskněte název souboru.

![ ](images/Android_UI_explanation.png)

Editor mapy je trochu odlišný od verze pro počítače. Tato stránka se soustředí na specifika mobilní verze. Pokud vás zajímá význam ostatních symbolů, prohlédněte si [Nástrojové lišty](toolbars.md) v manuálu pro PC verzi.

#### ![ ](../mapper-images/arrow-thin-upleft.png) Skrýt horní lištu

Použitím tohoto tlačítka můžete skrýt horní nabídku s nástroji, čímž získáte více místa pro mapu. Obdobné tlačítko zůstane viditelné, aby bylo možné horní nabídku znovu zobrazit.


#### ![ ](../mapper-images/compass.png) Přepínač kompasu

Pokud aktivujete toto tlačítko, zobrazí se v levém horním rohu obrazovky kompas. Červená jehla ukazuje směr na sever, zatímco černo-bílé pruhy vymezují směr natočení vašeho zařízení. Když je jehla rovnoběžně mezi černými pruhy, je zařízení natočeno k severnímu magnetickému pólu. Jakmile je jehla blízko severnímu směru, objeví se zelená kružnice, který usnadňuje přesně poznat, jak dobře je zařízení srovnáno se severním směrem: čím větší kružnice, tím lepší je srovnání. Kompas funguje ve třech dimenzích, takže nemusíte držet zařízení perfektně ve vodorovném směru, aby se otáčel.

Poznámka: užitečnost kompasu závisí na přítomnosti gyroskopu, jak je zmíněno v kapitole doporučení na zařízení.

Upozornění: kompas je velmi citlivý na magnetické materiály. Android se snaží eliminovat vliv lokálních magnetických polí, to ale vyžaduje kalibraci. Tu provedete tak, že budete zařízením pohybovat ve tvaru čísla 8 a současně s ním budete otáčet (ve vodorovné poloze). Zároveň musí být kompas aktivován. Pokud se lokální vlivy změní, musíte zařízení kalibrovat znovu.


#### ![ ](../mapper-images/tool-gps-display.png) Přepínač zobrazení (GPS) polohy

Toto tlačítko lze použít jen pokud je mapa, se kterou právě pracujete, správně georeferencovaná. V opačném případě je šedé a nelze stisknout. Po aktivaci tohoto tlačítka a po určení vaší polohy (to může trvat i několik minut) se ukáže v mapě červená tečka označující vaši aktuální pozici, získanou z GPS nebo z jiné služby poskytující informace o poloze (Wi-fi, GSM síť, ...). Pokud je navíc dostupný i odhad přesnosti polohy (HDOP), zobrazí se kolem tečky ještě červená kružnice, která ukazuje přesnost určení vaší polohy. Pravděpodobnost, že se nacházíte uvnitř této kružnice je cca 70 %.

Po dobu, kdy je zobrazení polohy aktivní, je vaše trasa automaticky zaznamenávána do souboru GPX s názvem "<název mapy> - GPS-<ROK-MĚSÍC-DEN>.gpx", který se ukládá do složky s aktuálně otevřenou mapou. Tento soubor je přiložen jako podklad k aktuální mapě. Svou trasu tak můžete snadno zobrazit nebo skrýt stejně jako ostatní podklady.

Berte na vědomí, že některá zařízení mohou přerušit záznam trasy, když je displej zařízení vypnutý nebo aplikace běží jen na pozadí z důvodu úspory baterie. Pokud chcete zajistit nepřerušované nahrávání trasy, nechte aplikaci OO Mapper stále aktivní.


#### ![ ](../mapper-images/gps-distance-rings.png) Přepínač vzdálenostních prstenců

Toto tlačítko lze použít jen pokud je aktivní i zobrazení polohy. Po aktivaci tohoto přepínače se zobrazí okolo vaší aktuální pozice další kružnice (prstence) ve vzdálenosti 10 a 20 metrů. Ty mohou být použity k hrubému odhadu vzdáleností v terénu.


#### ![ ](../mapper-images/rotate-map.png) Přepínač automatického natočení k severu

Když je aktivní tento přepínač, mapa se pomocí vnitřního kompasu v zařízení automaticky natáčí k severu. Aktualizace natočení probíhá 1 za sekundu, což je záměrně nízká frekvence kvůli úspoře baterie. I tak budete při používání této funkce pravděpodobně potřebovat náhradní baterie nebo dobíjení. Během jakékoli interakce s mapou a dalších 1,5 s poté se mapa nenatáčí, aby nedocházelo k nechtěným otočením během editace. Pokud je zároveň aktivováno i zobrazení polohy, pak se na displeji ukáže polopřímka, která začíná v bodě vaší aktuální pozice a míří směrem, kterým se díváte (za předpokladu, že držíte zařízení před sebou, displejem nahoru).


-----

#### ![ ](../mapper-images/map-parts.png) Map parts selector

This button opens a popup for changing the active map part.


#### ![ ](../mapper-images/tool-touch-cursor.png) Touch cursor toggle

This symbol activates a helper cursor which allows slow, but precise editing with fingers only. The cursor consists of a circular area and a pointer above the circle.

![ ](images/touch_cursor.png)

Touching the map anywhere outside the circle moves the pointer to this position. Touching the circle simulates a real touch at the pointer position above the circle.


#### ![ ](../mapper-images/templates.png) Template control

This shows a list of all opened templates. Touching a template toggles its visibility.


#### ![ ](../mapper-images/close.png) Close button

This closes the active map and returns to the map selection screen.


#### ![ ](../mapper-images/three-dots.png) Overflow button

Depending on the screen size of your device, some of the symbols available not fit onto the screen. They are instead placed in a list which is shown on touching the overflow button. If all symbols fit on the screen, this button is unused.


-----

#### ![ ](../mapper-images/view-zoom-out.png) Zoom out / Zoom to fixed

A short press will zoom out by one step. A long press will open a menu where you can jump to a fixed zoom (cf. screenshot).


#### ![ ](../mapper-images/move-to-gps.png) Move to location

When positioning services are enabled, this will move the map so that your current location is in the middle of the screen.


#### ![ ](../mapper-images/gps-temporary-point.png) Mark temporary position

This records a single point at your current location to act as a drawing help. Note that this marker is not saved in the map.


#### ![ ](../mapper-images/gps-temporary-path.png) Record temporary trace

This symbol is enabled when the location display is active. It records a temporary trace of the location, which is intended to act as a guideline for drawings. Using the trace directly is rarely useful because of the inaccurateness of location services.
Note that the temporary trace is not saved in the map.


#### ![ ](../mapper-images/gps-temporary-clear.png) Clear temporary markers

This removes the temporay traces and position markers. (They will also be discarded when closing the map file.)


#### ![ ](../mapper-images/paint-on-template-settings.png) Paint-on-template settings

This button allows to select the active image for scribbling (using the symbol above it).


-----

#### ![ ](../mapper-images/draw-freehand.png) Free-hand draw tool

Allows to draw paths free-handedly.


#### ![ ](../mapper-images/draw-point-gps.png) Draw at location tool

Sets a point object at your current location. Selecting this button first enters an averaging mode. While it is active, the input from the location service is averaged to get a more accurate estimate. Touch the map display anywhere to finish the averaging.


#### Symbol selector

Displays the active symbol, and opens the symbol selection screen on short press.

A long press of the symbol selector opens a popup menu which allows to read the symbol name and description, and to toggle the visibility and the protection state of the symbol.
