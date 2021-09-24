---
title: ContactsView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ContactsView
api_type:
- schema
ms.assetid: 8534f44b-a5af-4a9f-9621-23a3eff5f9d8
description: Das ContactsView-Element definiert eine Suche nach Kontaktelementen basierend auf alphabetischen Anzeigenamen.
ms.openlocfilehash: a96da6270d2396e5e82851dcc200f818cec5a7ed
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531099"
---
# <a name="contactsview"></a>ContactsView

Das **ContactsView-Element** definiert eine Suche nach Kontaktelementen basierend auf alphabetischen Anzeigenamen. 
  
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
|**MaxEntriesReturned** <br/> |Beschreibt die maximale Anzahl von Ergebnissen, die in der [FindItem-Antwort](finditem.md) zurückgegeben werden sollen.  <br/> |
|**InitialName** <br/> |Definiert den Vornamen in der Kontaktliste, der in der Antwort zurückgegeben werden soll. Wenn der angegebene Anfängliche Name nicht in der Kontaktliste enthalten ist, wird der nächste alphabetische Name gemäß definition durch den kulturellen Kontext zurückgegeben, außer wenn der nächste Name nach **FinalName** kommt. Wenn das **InitialName-Attribut** ausgelassen wird, enthält die Antwort eine Liste von Kontakten, die mit dem Vornamen in der Kontaktliste beginnt. Dieses Attribut ist optional.  <br/> |
|**FinalName** <br/> |Definiert den Nachnamen in der Kontaktliste, der in der Antwort zurückgegeben werden soll. Wenn das **FinalName-Attribut** ausgelassen wird, enthält die Antwort alle nachfolgenden Kontakte in der angegebenen Sortierreihenfolge. Wenn der angegebene endgültige Name nicht in der Kontaktliste enthalten ist, wird der nächste alphabetische Name gemäß der Definition durch den kulturellen Kontext ausgeschlossen.  <br/><br/>Wenn z. B. FinalName="Name", aber Name nicht in der Kontaktliste enthalten ist, werden Kontakte mit anzeigenamen namens Name1 oder NAME nicht eingeschlossen.  <br/><br/>Dieses Attribut ist optional.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Definiert eine Anforderung zum Suchen von Elementen in einem Postfach.<br/><br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel einer Anforderung wird veranschaulicht, wie sie die ersten drei Kontakte finden, beginnend mit dem Kontakt, der den Anzeigenamen "Kelly Rollin" aufweist.
  
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
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [FindItem-Vorgang](finditem-operation.md)
- [Suchen von Elementen](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

