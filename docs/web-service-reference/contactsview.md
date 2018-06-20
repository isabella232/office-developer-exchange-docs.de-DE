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
description: Das ContactsView-Element definiert eine Suche für Kontaktelemente basierend auf alphabetische Anzeigenamen.
ms.openlocfilehash: e578eb4dd0042b8c478e883c7fa54d7f2e984229
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757636"
---
# <a name="contactsview"></a>ContactsView

Das **ContactsView** -Element definiert eine Suche für Kontaktelemente basierend auf alphabetische Anzeigenamen. 
  
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
|**"MaxEntriesReturned"** <br/> |Beschreibt die maximale Anzahl der in der Antwort [FindItem](finditem.md) zurückzugebender Ergebnisse an.  <br/> |
|**InitialName** <br/> |Definiert den ersten Namen in der Kontaktliste in der Antwort zurückgegeben. Wenn der angegebene anfänglichen Name nicht in der Kontaktliste auf den Namen des nächsten alphabetische ist, wie durch die kulturellen Kontext definiert werden zurückgegeben außer, wenn der nächste Name nach **FinalName wird**. Wenn das Attribut **InitialName** ausgelassen wird, enthält die Antwort eine Liste von Kontakten, die mit der erste Name in der Kontaktliste beginnt. Dieses Attribut ist optional.  <br/> |
|**FinalName** <br/> |Definiert den Nachnamen in der Kontaktliste in der Antwort zurückgegeben. Wenn das Attribut **FinalName** ausgelassen wird, enthält die Antwort alle nachfolgenden Kontakte in der angegebenen Sortierreihenfolge. Ist der angegebene endgültige Name nicht in der Kontaktliste, wird der Name des nächsten alphabetische gemäß Definition durch die kulturellen Kontext ausgeschlossen werden.  <br/><br/>Beispielsweise wenn FinalName = "Name", aber Name ist nicht in der Kontaktliste, Kontakte, die Anzeigenamen der Name1 oder NAME nicht enthalten sein.  <br/><br/>Dieses Attribut ist optional.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Definiert eine Anforderung zum Suchen von Elementen in einem Postfach an.<br/><br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird eine Anforderung veranschaulicht, wie die ersten drei Kontakte, beginnend mit der Kontakt den Anzeigenamen des Kelly Rollin auf Suchen.
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [FindItem-Vorgang](finditem-operation.md)
- [Finding Items](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

