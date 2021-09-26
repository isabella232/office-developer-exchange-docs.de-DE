---
title: SubscriptionStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SubscriptionStatus
api_type:
- schema
ms.assetid: 2d64ebb7-f26a-4d02-b7ef-d9d7da75f0c3
description: Das SubscriptionStatus-Element beschreibt den Status eines Pushabonnements.
ms.openlocfilehash: 6918a4965da2c075341c99581c3bd06c93da35fa
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546931"
---
# <a name="subscriptionstatus"></a>SubscriptionStatus

Das **SubscriptionStatus-Element** beschreibt den Status eines Pushabonnements. 
  
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
|[SendNotificationResult](sendnotificationresult.md) <br/> |Enthält die Antwort der Clientanwendung auf eine Pushbenachrichtigung.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Es folgen die möglichen Textwerte für dieses Element:
  
- OK
    
- Abonnement kündigen
    
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element beschreibt den Status des Abonnements. Die Clientanwendung für das Pushabonnement sendet den Status zurück an den Computer, auf dem Exchange 2007 ausgeführt wird, auf dem die Clientzugriffsserverrolle nach jeder Pushbenachrichtigung installiert ist. Wenn der **SubscriptionStatus-Wert** **"Unsubscribe"** entspricht, beendet der Clientzugriffsserver das Senden von Benachrichtigungen und beendet das Abonnement. Wenn der **SubscriptionStatus-Wert** **"OK"** entspricht, sendet der Clientzugriffsserver weiterhin Benachrichtigungen.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

