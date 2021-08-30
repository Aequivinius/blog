---
layout: post
title: You're up and running!
---
# Aufgabenstellung und Ziele #
Wir mussten ein Pokemon Avatar Creator programmieren. 
Dafür mussten wir folgenden Facelets erstellen damit man verschiedene Sachen
(Hautfarbe, Augenfarbe, Haarenfarbe) auswählen konnte.
Da zeige ich wie man mit einem `RadioButton` und`SelectOneMenu` in `jsf` 
die Haut- und Augenfarbe eingeben kann.
# Ziele #
1. `RadioButton` implementieren und ändern
2. `SelectOneMenu`implementieren und ändern

# Produkt #
Das musste zuerst importiert werden:
```
<html xmlns="http://www.w3.org/1999/xhtml"
      xmlns:h="http://xmlns.jcp.org/jsf/html"
       xmlns:f = "http://java.sun.com/jsf/core" >
```
So habe ich das `RadioButton` importiert und umgeändert.      
```
<h:form id="eyecolor-form">
      <h:selectOneRadio value = "#{userData.data}"> 
   <f:selectItem itemValue = "Green" itemLabel = "Green" /> 
   <f:selectItem itemValue = "Blue" itemLabel = "Blue" />
</h:selectOneRadio>    
</h:form>
```
So habe ich das `SelectOneMenu` importiert und umgeändert.  
```
<h:form id="skincolor-form">
      <h:outputLabel for="skinColor"></h:outputLabel>
         <h:selectOneMenu value = "#{CharacterBean.eyecolor}"> 
   <f:selectItem itemValue = "light" itemLabel = "Light" /> 
   <f:selectItem itemValue = "dark" itemLabel = "Dark" /> 
</h:selectOneMenu> 
            <h:commandButton id="submit-button" value="Submit" action="eyecolorselector.xhtml"></h:commandButton>
</h:form>
```
# Verifizierung #
1. `RadioButton` wurde richtig implementiert und man kann die Augenfarbe ändern.
2. `SelectOneMenu` wurde richtig implementiert und man kann die Hautfarbe ändern.

# Reflexion #
Diese Aufgabe war für mich ziemlich erfolgreich und ich hatte keine grossen Probleme. 
Ich brauchte etwas lange bis ich die richtige Lösung fand und es tatsächlich funktionierte.
Ein Verbesserungsvorschlag für mich wäre, nicht sofort aufzugeben auch wenn es mehrmals hintereinander nicht funktioniert, sondern weiter versuchen.
