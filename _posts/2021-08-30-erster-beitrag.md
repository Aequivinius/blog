# Bilder Java JSF einbinden
## _Aufgabenstellung und Ziele_ ##

Im Modul 133 Der Berufsschule beschäftigen wir uns mit Web-Applikationen und speziell mit JSF (Java Server Faces). 
Ich möchte in meiner JSF-Applikation Bild/Grafiken einbinden.

Ich verfolge folgende Ziele:
1. Ich möchte Grafiken mit JSF anzeigen
2. Ich möchte den Lösungsweg nachvollziehbar darstellen.

## _Produkt_ ##

In JSF zeigt der Tag `<h:graphicImage` dem Benutzer eine nicht manipulierbare Grafik an. 
Das Bild, das ich einbinden möchte muss im resources Ordner der Applikation sein. Der Ordner resources wird nach Ressourcen durchsucht während dem durchlaufen der Applikation.
Aufgrund dessen kann das Bild auch über das Attribut "name" geladen werden.
Weil sich mein Bild *bd.png* in dem Unterordner /resources/img befindet ist es notwendig den Unterordner anzugeben. 
Mit dem Attribut "library" kann ich auf mein Bild greifen.

**Ordnerstruktur**

<img width="300" alt="Ordnerstruktur" src="https://user-images.githubusercontent.com/89779667/131359470-85262486-5a21-4897-9b25-9ffefa30bc1f.PNG">


**web.xml**
Diesen Textabschnitt brauche ich in meiner `web.xml` Datei.
``` 
  <context-param>
        <param-name>javax.faces.WABAPP_RESOURCES_DIRECTORY</param-name>
        <param-value>/WEB-INF/resources/css</param-value>
    </context-param>
``` 
**xhtml**
Diesen Textabschnitt brauche ich in meiner `.xhtml` Datei.
```

<h:graphicImage library="img" name="bd.png"/>
```
## _Reflektion und Verifikation_ ##

Mit Hilfe einer, von der Lehrperson zur Verfügung gestellten Präsentation, habe ich einen Weg gefunden um Grafiken und Bilder in meiner JSF-Applikation einzubinden. 
Mit Diesem Weg werden die Grafiken in meiner Web-Applikation, wie in Zel 1. gewünscht, angezeigt.
Der Lösungsweg ist beschrieben und begründet. Folgend wird das 2. Ziel erfüllt.
Ich habe durch die Präsentation rasch eine Lösung für mein Problem gefunden. Ich war einen Moment verwirrt über den Lösungsweg. Ich habe mich in der Zeit ein wenig verloren. 
Beim nächsten mal, wenn ich in so eine Situation gerate, werde ich bei anderen Quellen nach einer Lösung suchen oder die Lehrperson frühzeitig hinzuziehen.
