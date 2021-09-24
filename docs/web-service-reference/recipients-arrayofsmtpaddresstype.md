---
title: Empfänger (ArrayOfSmtpAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Recipients
api_type:
- schema
ms.assetid: cf68417d-85cf-49e0-857a-f987d3675344
description: Das Recipients-Element gibt ein Array von Empfängern einer Nachricht an.
ms.openlocfilehash: 20083c001df5097ded2033bed881ec3a39f98789
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59534494"
---
# <a name="recipients-arrayofsmtpaddresstype"></a>Empfänger (ArrayOfSmtpAddressType)

Das **Recipients-Element** gibt ein Array von Empfängern einer Nachricht an. 
  
```xml
<Recipients>   <SmtpAddress/></Recipients>
```

 **ArrayOfSmtpAddressType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SmtpAddress](smtpaddress.md) <br/> |Stellt die SMTP-Empfängeradresse (Simple Mail Transfer Protocol) einer Kalender- oder Kontaktfreigabeanfrage dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetSharingMetadata](getsharingmetadata.md) <br/> |Definiert eine Anforderung zum Abrufen eines undurchsichtigen Authentifizierungstokens, das die Freigabe-Einladung identifiziert.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange Webdienste des Computers hostet, auf dem Microsoft Exchange Server ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetSharingMetadata-Vorgang](getsharingmetadata-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

