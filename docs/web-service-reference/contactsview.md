---
title: ContactsView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContactsView
api_type:
- schema
ms.assetid: 8534f44b-a5af-4a9f-9621-23a3eff5f9d8
description: Das ContactsView-Element definiert eine Suche nach Kontaktelementen basierend auf alphabetischen Anzeigenamen.
ms.openlocfilehash: 23c3fe13c44cdd0e5a054ecb3378bc3d633e55aa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463818"
---
# <a name="contactsview"></a>ContactsView

Das **ContactsView** -Element definiert eine Suche nach Kontaktelementen basierend auf alphabetischen Anzeigenamen. 
  
[FindItem](finditem.md)
  
[ContactsView](contactsview.md)
  
```xml
<ContactsView MaxEntriesReturned="" InitialName="" FinalName="" />
```

**ContactsViewType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |Beschreibt die maximale Anzahl von Ergebnissen, die in der [FindItem](finditem.md) -Antwort zurückgegeben werden.  <br/> |
|**Initialname** <br/> |Definiert den ersten Namen in der Kontaktliste, der in der Antwort zurückgegeben werden soll. Wenn sich der angegebene ursprüngliche Name nicht in der Kontaktliste befindet, wird der nächste alphabetische Name im Kultur Kontext zurückgegeben, außer wenn der nächste Name nach **finalname**kommt. Wenn das **Initial** Name-Attribut nicht angegeben wird, enthält die Antwort eine Liste von Kontakten, die mit dem ersten Namen in der Kontaktliste beginnt. Dieses Attribut ist optional.  <br/> |
|**Finalname** <br/> |Definiert den letzten Namen in der Kontaktliste, der in der Antwort zurückgegeben werden soll. Wenn das **finalname** -Attribut nicht angegeben wird, enthält die Antwort alle nachfolgenden Kontakte in der angegebenen Sortierreihenfolge. Wenn sich der angegebene endgültige Name nicht in der Kontaktliste befindet, wird der nächste alphabetische Name im Kultur Kontext ausgeschlossen.  <br/><br/>Wenn beispielsweise finalname = "Name", aber Name nicht in der Kontaktliste enthalten ist, werden Kontakte mit Anzeigenamen von Name1 oder Name nicht einbezogen.  <br/><br/>Dieses Attribut ist optional.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Definiert eine Anforderung zum Suchen von Elementen in einem Postfach.<br/><br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel einer Anforderung wird veranschaulicht, wie die ersten drei Kontakte, beginnend mit dem Kontakt mit dem Anzeigenamen von Kelly Rollin, gefunden werden.
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="contacts:DisplayName"/>
        </t:AdditionalProperties>
      </ItemShape>
      <ContactsView MaxEntriesReturned="3" InitialName="Kelly Rollin" />
      <SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="contacts:DisplayName"/>
        </t:FieldOrder>
        </SortOrder>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="contacts"/>
      </ParentFolderIds>
    </FindItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [FindItem-Vorgang](finditem-operation.md)
- [Finding Items](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

