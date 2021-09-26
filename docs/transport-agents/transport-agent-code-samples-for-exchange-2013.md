---
title: Codebeispiele für Transport-Agent für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 626345ec-918f-4d91-932f-e6ce92553ccb
description: Hier finden Sie Informationen zu den Beispiel-Transport-Agents, die für Exchange 2013 verfügbar sind.
ms.openlocfilehash: 56334f661947cffceaf18eb257feeb6504a71ecb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545712"
---
# <a name="transport-agent-code-samples-for-exchange-2013"></a>Codebeispiele für Transport-Agent für Exchange 2013

Hier finden Sie Informationen zu den Beispiel-Transport-Agents, die für Exchange 2013 verfügbar sind.
  
**Gilt für:** Exchange Server 2013
  
Sie können die in Exchange Server 2013 enthaltenen APIs verwenden, um Agents zu entwickeln, die die Transportfunktionalität erweitern. Dieser Artikel enthält Informationen zu den Verfügbaren Beispiel-Agents, mit denen Sie erfahren können, wie Sie das Transportverhalten programmgesteuert erweitern können. Die Beispiel-Agents enthalten den Quellcode für jede Komponente. 
  
In der folgenden Tabelle sind die Beispiel-Agents für Exchange 2013 aufgeführt.
  
**Tabelle 1. Transport-Agent-Beispiele**

|**Beispielname**|**Beschreibung**|
|:-----|:-----|
|[Exchange 2013: Erstellen eines Antivirus-Transport-Agents](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-an-6e544269) <br/> |Dieser Agent antwortet auf die [OnEndOfData-](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) und [OnSubmittedMessage-Ereignisse](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) und sendet die eingehende Nachricht an einen Out-of-Process-Server, der die Nachricht asynchron überprüft und eine geänderte Version zurückgibt.  <br/> |
|[Exchange 2013: Erstellen eines Transport-Agents für die Bandbreitenprotokollierung](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa) <br/> |Dieser Agent reagiert auf die [OnSubmittedMessage-](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) und [OnRoutedMessage-Ereignisse,](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) erfasst die Bandbreitennutzung für angegebene Empfänger und protokolliert die Bandbreitennutzungsinformationen in einer Textdatei.  <br/> |
|[Exchange 2013: Erstellen eines Transport-Agents für die Textkonvertierung](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0) <br/> |Dieser Agent filtert Skripts aus E-Mail-Nachrichten, indem er das Format der eingehenden Nachricht bestimmt und entscheidet, ob eine Filterung erfolgen muss. Wenn eine Filterung erforderlich ist, wird der Inhalt in HTML konvertiert, gefiltert und dann wieder in das Quellformat konvertiert.  <br/> |
|[Exchange 2013: Erstellen eines SMTP-Protokollierungs-Transport-Agents](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-an-fc23dc33) <br/> |Dieser Agent antwortet auf das [OnEndOfData-Ereignis](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) und protokolliert die Nachricht asynchron in einer Datei auf der lokalen Festplatte.  <br/> |
|[Exchange 2013: Erstellen eines Transport-Agents, der Absender vorübergehend blockiert](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-52a767d8) <br/> |Dieser Agent antwortet auf die [OnEndOfHeaders-](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) und [OnRcptCommand-Ereignisse](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnRcptCommand.aspx) und bestimmt, ob der Absender der Nachricht zuvor Nachrichten an den Front-End-Transportdienst gesendet hat. Wenn der Absender zuvor keine Nachricht an den Front-End-Transportdienst gesendet hat, wird der Absender einer Liste von Absendern hinzugefügt, und die Nachricht wird mit einer Antwort abgelehnt, die den Client anweist, den Vorgang später erneut auszuführen (auch als Grauliste bezeichnet). Wenn sich der Absender in der Liste der vorherigen Absender befindet, lehnt der Agent die Nachricht nicht ab.  <br/> |
|[Exchange 2013: Erstellen eines Postfachserverprotokollierungs-Transport-Agents](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-fc8632e5) <br/> |Dieser Agent antwortet auf das [OnRoutedMessage-Transportpipelineereignis](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) und protokolliert die Nachricht synchron in einer Datei auf der lokalen Festplatte.  <br/> |
|[Exchange 2013: Erstellen eines X-Header-Transport-Agents](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-an-32f62f5a) <br/> |Dieser Agent reagiert auf das [OnEndOfHeaders-Ereignis](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) und liest und ändert X-Header in Nachrichten.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Transport-Agent-Konzepte in Exchange 2013](transport-agent-concepts-in-exchange-2013.md)    
- [Transport-Agent-Referenz für Exchange 2013](transport-agent-reference-for-exchange-2013.md)    
- [Erstellen eines RoutingAgent-Transport-Agents für Exchange 2013](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md)   
- [Erstellen eines SmtpReceiveAgent-Transport-Agents für Exchange 2013](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)    
- [Erstellen eines DeliveryAgent-Transport-Agents für Exchange 2013](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)
    

