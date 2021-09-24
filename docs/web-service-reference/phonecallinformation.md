---
title: PhoneCallInformation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PhoneCallInformation
api_type:
- schema
ms.assetid: a0363c42-6d35-4074-bc17-946eb12736ff
description: Das PhoneCallInformation-Element gibt die Statusinformationen für einen Telefonanruf an.
ms.openlocfilehash: 815e0ffac761b12969483752f5022f8580f6cc62
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59528326"
---
# <a name="phonecallinformation"></a>PhoneCallInformation

Das **PhoneCallInformation-Element** gibt die Statusinformationen für einen Telefonanruf an. 
  
```XML
<PhoneCallInformation>
   <PhoneCallState/>
   <ConnectionFailureCause/>
   <SIPResponseText/>
   <SIPResponseCode/>
</PhoneCallInformation>
```

 **PhoneCallInformationType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[PhoneCallState](phonecallstate.md) <br/> |Gibt den Status für einen Telefonanruf an. Dieses Element ist erforderlich.  <br/> |
|[ConnectionFailureCause](connectionfailurecause.md) <br/> |Gibt die Ursache für einen Verbindungsfehler an. Dieses Element ist erforderlich.  <br/> |
|[SIPResponseText](sipresponsetext.md) <br/> |Gibt den SIP-Antworttext an. Dieses Element ist optional.  <br/> |
|[SIPResponseCode](sipresponsecode.md) <br/> |Gibt den SIP-Antwortcode an. Dieses Element ist optional.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetPhoneCallInformationResponse](getphonecallinformationresponse.md) <br/> |Definiert eine Antwort auf eine [GetPhoneCallInformation-Vorgangsanforderung.](getphonecallinformation-operation.md)  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

