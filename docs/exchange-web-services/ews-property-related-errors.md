---
title: EWS-Eigenschaft-bezogene Fehler
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 1c4c5969-7bdd-4021-be0e-cae99e86cf2c
description: Hier finden Sie Informationen zur Behandlung von Fehlern in der Anwendung EWS-Eigenschaft im Zusammenhang.
ms.openlocfilehash: 019a13116ae9a08c19381b78e1fd38c26f50c0d1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512268"
---
# <a name="ews-property-related-errors"></a>EWS-Eigenschaft-bezogene Fehler

Hier finden Sie Informationen zur Behandlung von Fehlern in der Anwendung EWS-Eigenschaft im Zusammenhang.
  
Die meisten EWS-Clientanwendungen werden Eigenschaften verwenden, d. h., dass Sie behandeln von Fehlern im Zusammenhang-Eigenschaft hat. Sie können diese Fehler zur Laufzeit oder während Sie die EWS-Anwendung entwickeln behandeln.
  
**Tabelle 1:-Eigenschaft-bezogene Fehler und deren Behandlung**

|**Fehler**|**Ein Versuch verursacht...**|**Behandeln von...**|
|:-----|:-----|:-----|
|ErrorDataSizeLimitExceeded  <br/> |Festlegen einer Eigenschaft mit einem Wert, der die maximale Größe für die Eigenschaft überschreitet, oder die Eigenschaft wird nicht unterstützt, wie etwa Ordnereigenschaften streaming.  <br/> |Einschränken der Größe von Daten, legen Sie für die Eigenschaft.  <br/> |
|ErrorFolderPropertRequestFailed  <br/> |Rufen Sie eine Eigenschaft, die konnten nicht abgerufen werden.  <br/> |Gibt an, dass die Eigenschaft kann nicht abgerufen werden.  <br/> |
|ErrorInvalidExtendedProperty  <br/> |Legen Sie eine ungültige Kombination der Werte der erweiterten Eigenschaft oder die Ergebnisse in einer erweiterten Eigenschaft Uniform Resource Identifier (URI) ist ungültig.  <br/> |Der Wert der erweiterten Eigenschaft überprüfen.  <br/> |
|ErrorInvalidExtendedPropertyValue  <br/> |Festlegen der Wert einer erweiterten Eigenschaft, der den angegebenen Typ nicht entsprechen  <br/> |Aktualisieren von Code, um zu prüfen, ob matching-Typen.  <br/> |
|ErrorInvalidFolderId  <br/> |Legen Sie die Struktur der Ordner-ID auf einem ungültigen Formular.  <br/> |Verwenden von Bezeichnern nur zurückgegeben von EWS.  <br/> |
|ErrorInvalidId  <br/> |Legen Sie die Struktur der einen Bezeichner und/oder ändern Sie Schlüssel in einem ungültigen Formular.  <br/> |Verwenden von Bezeichnern nur zurückgegeben von EWS.  <br/> |
|ErrorInvalidIdEmpty  <br/> |Legen Sie einer leere einen Bezeichner.  <br/> |Durch Festlegen des Bezeichners mit einem gültigen Bezeichner Elements oder Ordners.  <br/> |
|ErrorInvalidIdMalformed  <br/> |Legen Sie die Struktur der einen Bezeichner und/oder ändern Sie Schlüssel in einem ungültigen Formular.  <br/> |Verwenden von Bezeichnern nur zurückgegeben von EWS.  <br/> |
|ErrorInvalidPropertyAppend  <br/> |Fügen Sie eine Eigenschaft, die anhängen nicht unterstützt.  <br/> |Aktualisieren des Codes, damit nur versucht wird, fügen Sie der empfängerauflistung-Eigenschaften (an, Cc und Bcc), Attendee-Auflistung: Eigenschaften Werte (erforderlich, Optional, Ressourcen), Body-Eigenschaft und die ReplyTo-Eigenschaft.  <br/> |
|ErrorInvalidPropertyDelete  <br/> |Löschen einer Eigenschaft, die Löschen nicht unterstützt.  <br/> |Aktualisieren den Code, um nicht versuchen, die Eigenschaft zu löschen. Der Ordner und Element-IDs können beispielsweise können nicht gelöscht werden.  <br/> |
|ErrorInvalidPropertyForExists  <br/> |Legen Sie eine Einschränkung diese existenzielle je Suche für eine Flag-basierte-Eigenschaft.  <br/> |Aktualisieren den Code, um das Flag-basierte Eigenschaften nicht in eine Einschränkung diese existenzielle je Suche verwenden. Flag-basierte Eigenschaften sind IsDraft, IsSubmitted, IsUnmodified, IsResend und IsFromMe.  <br/> |
|ErrorInvalidPropertyForOperation  <br/> |Bearbeiten einer Eigenschaft eines Elements oder Ordners, der von der Operation nicht unterstützt wird.  <br/> |Aktualisieren den Code, um die Eigenschaft mit dem Vorgang nicht zugegriffen werden, die den Fehler verursacht hat.  <br/> |
|ErrorInvalidPropertyRequest  <br/> |Geben Sie eine Eigenschaft in der Anforderung, die für den jeweiligen Elementtyp nicht unterstützt wird.  <br/> |Aktualisieren den Code, um nicht auf die Eigenschaft mit dem Vorgang zuzugreifen versuchen.  <br/> |
|ErrorInvalidPropertySet  <br/> |Festlegen Sie eine nur-Lese-Eigenschaft.  <br/> |Aktualisieren den Code, um nicht versuchen, die Eigenschaft festzulegen.  <br/> |
|ErrorInvalidValueForProperty  <br/> |Vergleichen Sie den Wert einer Eigenschaft in einer Suche Einschränkung, bei denen der Vergleichswert nicht den Eigenschaftentyp übereinstimmen.  <br/> |Aktualisieren von Code, um zu prüfen, ob Typenkonflikt Eigenschaft.  <br/> |
|ErrorItemSavePropertyError  <br/> |Speichern eines Elements oder Ordners mit ungültigen Werten.  <br/> |Überprüfen die Eigenschaftswerte und Typen vor dem Senden in einer Anforderung an.  <br/> |
|ErrorNoFolderClassOverride  <br/> |Legen Sie die Ordner-Klasse auf einen neuen Ordner, der nicht den Basisordner-Typ ist.  <br/> |Verwenden eine generische Ordnertyp, um die Klasse Ordner festzulegen.  <br/> |
|ErrorNoPropertyTagForCustomProperties  <br/> |Eine benutzerdefinierte erweiterte Eigenschaft zu verweisen, indem dessen Eigenschafts-Tag.  <br/> |Aktualisieren den Code, um die benutzerdefinierten verweisen extended-Eigenschaft von Eigenschaftensatz-ID und den Eigenschaftennamen oder Versendung Eigenschaftenbezeichner.  <br/> |
|ErrorObjectTypeChanged  <br/> |Festlegen Sie oder aktualisieren Sie die Item-Klasse für ein Element, das übereinstimmt mit dieses Schematyps.  <br/> |Aktualisieren von Code, der Item-Klasse den Elementtyp Schema übereinstimmt.  <br/> |
|ErrorPropertyUpdate  <br/> |Aktualisieren Sie eine Eigenschaft mit einer Ungültiger Eigenschaftswert.  <br/> |Überprüfen vor dem Absenden in einer Anforderung [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) Wert der Eigenschaft.  <br/> |
|ErrorRequiredPropertyMissing  <br/> |Senden Sie eine CreateAttachment-Anforderung, die eine erforderliche Eigenschaft fehlt.  <br/> |Aktualisieren den Code, um die fehlenden Eigenschaftensatz gemäß der Eigenschaftenpfad in der Antwort zurückgegeben.  <br/> |
|ErrorUnsupportedMapiPropertyType  <br/> |Verwenden Sie erweiterte Eigenschaftentypen-Objekt vom Typ, Objektarray, Fehler oder Null.  <br/> |Aktualisieren den Code, um die eingeschränkte erweiterte Eigenschaftentypen nicht verwendet werden.  <br/> |
|ErrorUnsupportedPathForQuery  <br/> |Verwenden Sie einen Pfad nicht unterstützte Eigenschaft in einer Einschränkung für die Suche.  <br/> |Ändern die Einschränkung suchen, um den Eigenschaftentyp Pfad ausschließen.  <br/> |
|ErrorUnsupportedPathForSortGroup  <br/> |Verwenden Sie einen Pfad nicht unterstützte Eigenschaft in einer sortierten oder gruppierten Suchanfrage an.  <br/> |Ändern die Einschränkung suchen, um den Eigenschaftentyp Pfad ausschließen.  <br/> |
|ErrorUnsupportedTypeForConversion  <br/> |Fordern Sie einen Eigenschaftentyp, der XML-Code für EWS in eine Antwort zurückgegeben konvertiert werden kann.  <br/> |Aktualisieren den Code, um den Eigenschaftentyp nicht anfordern.  <br/> |
|ErrorUpdatePropertyMismatch  <br/> |Aktualisieren eines Elements oder Ordners, der die Beschreibung ändern, für die nicht die-Eigenschaft entspricht, die zu aktualisierenden angegeben ist.  <br/> |Ändern den Code, damit die Beschreibung der Änderung des Elements oder Ordners-Typ entspricht, der aktualisiert wird.  <br/> |
   
## <a name="see-also"></a>Siehe auch


- [Eigenschaften und erweiterte Eigenschaften in EWS in Exchange](properties-and-extended-properties-in-ews-in-exchange.md)
    
- [Erste Schritte mit Webdiensten in Exchange](start-using-web-services-in-exchange.md)
    
- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    

