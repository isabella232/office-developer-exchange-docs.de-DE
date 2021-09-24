---
title: EmailUser
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: dc8133ff-c34e-4921-bb56-06e79aee0a8a
description: Das EmailUser-Element gibt einen E-Mail-Empfänger an.
ms.openlocfilehash: d3c1657938f8b4b21123b2f7cb67252e31f3d7b2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538209"
---
# <a name="emailuser"></a>EmailUser

Das **EmailUser-Element** gibt einen E-Mail-Empfänger an. 
  
```XML
<EmailUser>
    <Name/>
    <UserId/>
</EmailUser>
```

 **EmailUserType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Name (Zeichenfolge)](name-string.md) <br/> |Gibt einen Namen oder Schlüssel der Sucheinschränkung oder den Namen eines E-Mail-Benutzers an.  <br/> |
|[UserId (Zeichenfolge)](userid-string.md) <br/> |Gibt den Benutzerbezeichner eines E-Mail-Benutzers an.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Teilnehmer](attendees.md) <br/> |Gibt die Empfänger einer Einladung zu einer Besprechung an.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

