# TTL-Gatter-Binaer-Sieben-Segment-Wandler

In diesem Projekt habe ich einen Wandler gebaut, der die Eingabe von Zahlen binär mit 4 Bit ins dezimale System umwandelt und sie auf einer Sieben-Segment Anzeige ausgibt.

Stückliste:

- 1x LM74LS04 / NOT-Gate
- 5x LM74LS08 / AND-Gate
- 6x LM74LS032 / OR-Gate
- 1x Sieben-Segment Anzeige (common-Cathode)
- 4x Button
- 4x Widerstand (hier 560Ohm)
- 2x 4er Dekadenwiderstand (1kOhm) oder 7 Widerstände (1kOhm)
- Steckbrett/er
- Jumper-Cables
- 5V Spannungsversorgung


Angefangen habe ich erstmal mit der Erstellung der Logik-Schaltung in Logisim.
Hier habe ich zuerst die Wahrheitstabelle erstellt:
Die Eingänge sind ABCD und die Ausgänge sind jeweils die Segmente der Sieben-Segment Anzeige.

![](https://github.com/FabianSchieder/TTL-Gatter-Binaer-Sieben-Segment-Wandler/blob/main/Wahrheitstabelle.png "Wahrheitstabelle")

Danach habe ich daraus die Logik-Schaltung aufgebaut:

![](https://github.com/FabianSchieder/TTL-Gatter-Binaer-Sieben-Segment-Wandler/blob/main/LogikSchaltung.png "Logik-Schaltung")

Um den Aufbau zu erleichtern habe ich sie dann in eine Art Schaltplan umgewandelt:

![](https://github.com/FabianSchieder/TTL-Gatter-Binaer-Sieben-Segment-Wandler/blob/main/Schaltplan.png "Schaltplan")


Nach der ganzen Theorie gings dann ans Eingemachte, und zwar die Schaltung aufzubauen:

![](https://github.com/FabianSchieder/TTL-Gatter-Binaer-Sieben-Segment-Wandler/blob/main/GesamteSchaltung.jpg "Gesamte Schaltung")

Den ersten Schritt den ich gemacht habe war das Aufbauen der Eingabe.
Diese besteht aus 4 Knöpfen, und die Ausgänge der Knöpfe sind jeweils mit einem pull-down-Widerstand verbunden.

![](https://github.com/FabianSchieder/TTL-Gatter-Binaer-Sieben-Segment-Wandler/blob/main/Eingabe.jpg "Eingabe")

Nach der Eingabe kommt der kniffligste Teil der Schaltung - die Logik.
Einen Schönheitspreis gewinnt mein Aufbau auf jeden Fall nicht, aber das schöner aufzubauen wäre zu zeitaufwändig.
Ich musste den Schaltplan ein wenig abändern, da ich nicht genügend ICs hatte. Das Gatter ganz unten rechts ist z.B. ein CMOS-AND-Gatter.
Alle anderen ICs sind trotzdem TTL Gatter.

![](https://github.com/FabianSchieder/TTL-Gatter-Binaer-Sieben-Segment-Wandler/blob/main/ICs.jpg "Logik")

Für die Sieben-Segment Anzeige habe ich Dekadenwiderstände benutzt, weil diese viel platzspahrender sind.
Natürlich funktionieren da auch "normale" Widerstände nehmen. In diesem Fall 1kOhm.
Viel mehr brauche ich dazu nicht sagen.

![](https://github.com/FabianSchieder/TTL-Gatter-Binaer-Sieben-Segment-Wandler/blob/main/SiebenSegment.jpg "Sieben-Segment")

Als Spannungsversorgung habe ich einen Arduino-UNO benutzt, aber natürlich funktioniert hier jede beliebige 5V DC Spannungsquelle.



Link, zur Logisim Projekt Datei:

![](https://github.com/FabianSchieder/TTL-Gatter-Binaer-Sieben-Segment-Wandler/blob/main/BinaerZuSiebenSegmentWandler.circ)






