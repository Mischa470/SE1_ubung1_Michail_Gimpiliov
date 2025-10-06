Aufgabe 1: 
1) 
Antwort auf Frage 1:
Die zwei Packages „View“ und „Control“ repräsentieren die zwei unterschiedlichen Schichten der Software, die wir bauen wollen. View mit der Klasse Client dient praktisch nur als Präsentationsschicht, während Control, also die Kontrollschicht mit der Klasse GermanTranslator und dem Interface Translator das Gerüst der Software bilden. Da wir nun eine Factory-Klasse, welche für die Objekterzeugung zuständig ist, erstellen wollen, muss diese im Control-Package liegen. In dieser Klasse wird dann laut Aufgabenstellung mithilfe einer Methode ein Objekt der Klasse GermanTranslator erstellt, welches mit der Klasse LocalDate das Datum system-intern setzt. Anschließend wird in der Klasse Client der Translator streng (also mithilfe der zuvor erstellten Methode) implementiert und dieser kann dann die Methode translateNumber() mit dem Übergabeparameter der Methode aNumber aufrufen und das Ergebnis zurückgeben. 

Antwort auf Frage 2:
Für die hier gegebene Problematik könnte man das Factory Pattern verwenden. Anstatt ein neues Objekt mit new in der Client-Klasse zu erstellen wird in der Factory-Klasse eine create()-Methode implementiert, welches ein Objekt vom Typ des Interfaces zurückgibt. So ist es für die Client-Klasse unwichtig, welcher genaue Translator in der Factory-Klasse erstellt wird, da immer der Obertyp (in dem Fall Translator) zurückgegeben wird. Der software-technische Nutzen in diesem Beispiel wäre, dass man anstatt eines GermanTranslator auch einen beliebig anderen Translator in der Factory-Klasse erstellen könnte, um diesen dann in der Client Klasse aufrufen zu können. 

Antwort auf Frage 3: 
Man muss das Interface auf public stellen, da der Translator sonst nicht von dem package „view“ benutzt werden kann, da der Modifier public erst die package-privatheit aufhebt.  

2) 
Antwort auf Frage 1:
Eine separate Testklasse ermöglicht eine klare Trennung zwischen Produktionscode und Testlogik, was die Wartbarkeit verbessert und Kollisionen vermeidet.

Antwort auf Frage 2:
Der Sinn von Äquivalenzklassen bei einem Blackbox-Test liegt darin, dass sie die unendliche Menge möglicher Eingaben auf eine handhabbare Auswahl reduzieren. Werte die ein gleiches oder ähnliches Verhalten haben, werden in eine Äquivalenzklasse zusammengefasst, welche dann durch einen oder ein paar wenige Tests überprüft werden kann, anstatt umständlich viele Tests für jeden einzelnen Wert durchzuführen. 

Antwort auf Frage 3: 
Der Client implentiert keine eigene Logik, die man testen kann, sondern nutzt nur ein Translator-Objekt über die Factory-Klasse. 


