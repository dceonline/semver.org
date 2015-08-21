---
layout: german
title: Semantische Versionierung 2.0.0
---

Semantische Versionierung 2.0.0
===============================

Zusammenfassung
---------------

Bei einer vorgegebenen Versionsnummer MAJOR.MINOR.PATCH, erhöht sich:

1. die MAJOR Version bei inkompatiblen Änderungen an der API,
1. die MINOR Version beim Hinzufügen von abwärtskompatibler Funktionalität und
1. die PATCH Version beim Erstellen abwärtskompatibler Bugfixes.

Es gibt zusätzliche Bezeichner für Pre-Release und Build Metadaten als 
Erweiterung zum MAJOR.MINOR.PATCH Format.

Einleitung
----------

In der Welt des Software-Management existiert ein grauenvoller Ort mit Namen 
"Abhängigkeitshölle". Desto größer Ihr System wird und je mehr Pakete Sie in 
Ihre Software integrieren, um so wahrscheinlicher ist es, dass Sie sich eines 
Tages an diesem Ort der Verzweiflung wieder finden.

In Systemen mit vielen Abhängigkeiten kann die Veröffentlichung neuer 
Paketversionen recht schnell zum Alptraum werden. Ist die Spezifikation von 
Abhängigkeiten zu eng gefasst besteht die Gefahr einer Versionssperre (die 
Unmöglichkeit ein Upgrade eines Paketes durchzuführen ohne dazu neue Versionen 
aller abhängigen Pakete herauszubringen). Sind die Abhängigkeiten zu locker 
vorgegeben, werden Sie unweigerlich von einer Vermischung der Versionen 
betroffen sein. Die Abhängigkeitshölle ist dann erreicht, wenn Versionssperre 
oder Versionsvermischung Sie daran hindern Ihr Projekt einfach und sicher voran 
zu bringen.

Als eine Lösung für dieses Problem schlage ich Ihnen einen einfachen Satz von 
Regeln und Anforderungen vor, wie man Versionsnummern zuweist und erhöht. Diese 
Regeln basieren auf weit verbreiteten und im Einsatz befindlichen Praktiken 
sowohl bei unfreier als auch freier Software, sind jedoch nicht unbedingt 
darauf begrenzt. Damit dieses System funktioniert müssen Sie zuerst eine 
öffentliche API deklarieren. Diese sollte aus Unterlagen bestehen oder 
aus dem Code selbst hervorgehen. Unabhängig davon ist es wichtig das diese API 
klar und präzise ist. Haben Sie diese API erst einmal veröffentlicht, 
kommunizieren Sie Änderungen daran durch spezielle Erhöhungen Ihrer 
Versionsnummer. Betrachten sie ein Versionsformat von X.Y.Z 
(Major.Minor.Patch). Bugfixes, die die API nicht beeinflussen, erhöhen die 
Patch-Version, abwärtskompatible Erweiterungen/Änderungen erhöhen die 
Minor-Version und nicht abwärtskompatible Änderungen erhöhen die Major-Version.

Ich nenne dieses System "Semantische Versionierung". Im Rahmen dieses Systems 
beziehen sich Versionsnummer auf den zugrundeliegenden Code und darauf was sich 
von der einen zur nächsten Version geändert hat.