---
title: SubscriptionStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SubscriptionStatus
api_type:
- schema
ms.assetid: 2d64ebb7-f26a-4d02-b7ef-d9d7da75f0c3
description: Das Element SubscriptionStatus beschreibt den Status eines Push-Abonnements.
ms.openlocfilehash: 1f6de15f7a3b07714899aef2ff74a8d556f8ca1d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839131"
---
# <a name="subscriptionstatus"></a>SubscriptionStatus

Das Element **SubscriptionStatus** beschreibt den Status eines Push-Abonnements. 
  
```xml
<SubscriptionStatus>OK or Unsubscribe</SubscriptionStatus>
```

 **SubscriptionStatusType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SendNotificationResult](sendnotificationresult.md) <br/> |Enthält die Antwort der Clientanwendung ' auf einer Push-Benachrichtigung.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Es folgen die möglichen Textwerte für dieses Element:
  
- OK
    
- Kündigen eines Abonnements
    
## <a name="remarks"></a>Hinweise

Dieses Element beschreibt den Status des Abonnements. Die Push-Abonnement-Clientanwendung gesendet, der den Status wieder auf dem Computer, auf dem Exchange 2007 ausgeführt werden, die Clientzugriffsserverrolle nach einzelnen Push Notification installiert hat. Wenn der Wert **SubscriptionStatus** **kündigen**gleich ist, wird der Clientzugriffsserver Senden von Benachrichtigungen beenden und beenden Sie das Abonnement. Wenn der Wert **SubscriptionStatus** **OK**gleich ist, wird der Clientzugriffsserver weiterhin Benachrichtigungen senden.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

