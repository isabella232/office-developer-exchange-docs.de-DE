---
title: FindPeopleResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 95f016a9-002f-4be3-abd6-f5e3528afd44
description: Das FindPeopleResponse-Element gibt die Antwort auf eine FindPeople an.
ms.openlocfilehash: 4f2c2f6069a515d5153ea488b35182d8b35f029f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758475"
---
# <a name="findpeopleresponse"></a>FindPeopleResponse

Das **FindPeopleResponse** -Element gibt die Antwort auf eine **FindPeople** an. 
  
```XML
<FindPeopleResponse ResponseClass=" Success | Warning | Error ">
    <People/>
    <TotalNumberOfPeopleInView/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</FindPeopleResponse>
```

 **FindPeopleResponseMessageType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|ResponseClass  <br/> |Gibt die Antwort-Klasse.  <br/> |
   
#### <a name="responseclass"></a>ResponseClass

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Erfolg  <br/> |Gibt Erfolg an.  <br/> |
|Warning  <br/> |Gibt eine Warnung an.  <br/> |
|Fehler  <br/> |Gibt einen Fehler an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Personen](people.md) <br/> |Gibt ein Array von Persona Daten als Ergebnis einer Anforderung **FindPeople** zurückgegeben.  <br/> |
|[TotalNumberOfPeopleInView](totalnumberofpeopleinview.md) <br/> |Gibt die Gesamtzahl der Rollen auf einem Server gespeichert, die durch eine **FindPeople** Anforderung zurückgegeben werden.  <br/> |
|[MessageText](messagetext.md) <br/> |Enthält einen beschreibenden Text für den Status der Antwort.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Enthält Statusinformationen über die Anforderung.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.  <br/> |
|[MessageXml](messagexml.md) <br/> |Bietet zusätzliche Fehlerantwortinformationen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Gibt ein Array von Antwortnachrichten.  <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

