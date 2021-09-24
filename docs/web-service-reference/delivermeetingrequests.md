---
title: DeliverMeetingRequests
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DeliverMeetingRequests
api_type:
- schema
ms.assetid: 04b999af-0b27-4e6d-a8b1-400955a1afaa
description: Das DeliverMeetingRequests-Element definiert, wie Besprechungsanfragen zwischen dem Stellvertreter und dem Prinzipal verarbeitet werden. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 8e61af87337cb1fc8936b4de7753fca2d6c1161e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519828"
---
# <a name="delivermeetingrequests"></a>DeliverMeetingRequests

Das **DeliverMeetingRequests-Element** definiert, wie Besprechungsanfragen zwischen dem Stellvertreter und dem Prinzipal verarbeitet werden. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
```XML
<DeliverMeetingRequests>DelegatesOnly or DelegatesAndMe or DelegatesAndSendInformationToMe or NoForward</DeliverMeetingRequests>
```

 **DeliverMeetingRequestsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AddDelegate](adddelegate.md) <br/> |Definiert eine Anforderung zum Hinzufügen von Stellvertretern für ein Postfach. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[UpdateDelegate](updatedelegate.md) <br/> |Definiert eine Anforderung zum Aktualisieren von Stellvertretern in einem Postfach. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[GetDelegateResponse](getdelegateresponse.md) <br/> |Enthält den Status und das Ergebnis einer GetDelegate-Anforderung. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
## <a name="text-value"></a>Textwert

In der folgenden Tabelle sind die möglichen Werte für das **DeliverMeetingRequests-Element** aufgeführt. 
  
**DeliverMeetingRequests-Elementwerte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|DelegatesOnly  <br/> |Besprechungsanfragen werden an die Stellvertretung weitergeleitet und in den Ordner "Gelöschte Elemente" im Postfach des Prinzipals verschoben.  <br/> |
|DelegatesAndMe  <br/> |Besprechungsanfragen werden an den Stellvertreter weitergeleitet und verbleiben im Posteingangsordner im Postfach des Prinzipals.  <br/> |
|DelegatesAndSendInformationToMe  <br/> |Besprechungsanfragen werden an die Stellvertretung weitergeleitet und verbleiben im Posteingangsordner im Postfach des Prinzipals, aber die Schaltflächen "Annehmen", "Mit Vorbehalt" und "Ablehnen" werden nicht im Microsoft Office Outlook Lesebereich angezeigt.  <br/> |
|NoForward  <br/> |Besprechungsanfragen werden nicht an die Stellvertretung weitergeleitet.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die **DeliverMeetingRequests-Einstellung** wirkt sich auf alle Delegaten im Postfach eines Prinzipals aus. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [AddDelegate-Vorgang](adddelegate-operation.md)  
- [UpdateDelegate-Vorgang](updatedelegate-operation.md)  
- [GetDelegate-Vorgang](getdelegate-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
- [Hinzufügen von Delegaten](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

