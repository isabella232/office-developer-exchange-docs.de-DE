---
title: Codebeispiele für Transport-Agent für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 626345ec-918f-4d91-932f-e6ce92553ccb
description: Hier finden Sie Informationen zu den Beispiel-Transport-Agents, die für Exchange 2013 verfügbar sind.
ms.openlocfilehash: c14a4e34102b55014cc6507e375929c186f5f6e9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461800"
---
# <a name="transport-agent-code-samples-for-exchange-2013"></a>Codebeispiele für Transport-Agent für Exchange 2013

Hier finden Sie Informationen zu den Beispiel-Transport-Agents, die für Exchange 2013 verfügbar sind.
  
**Gilt für:** Exchange Server 2013
  
Sie können die in Exchange Server 2013 enthaltenen APIs verwenden, um Agents zu entwickeln, die die Transport Funktionalität erweitern. Dieser Artikel enthält Informationen zu den Beispiel-Agents, die Ihnen bei der programmgesteuerten Erweiterung des Transportverhaltens behilflich sind. Die Beispiel-Agents enthalten den Quellcode für jede Komponente. 
  
In der folgenden Tabelle sind die Beispiel-Agents für Exchange 2013 aufgeführt.
  
**Tabelle 1. Beispiele für Transport-Agents**

|**Beispiel Name**|**Beschreibung**|
|:-----|:-----|
|[Exchange 2013: Erstellen eines Antivirus-Transport-Agents](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-an-6e544269) <br/> |Dieser Agent antwortet auf die [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) -und [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) -Ereignisse und sendet die eingehende Nachricht an einen prozessübergreifenden Server, der die Nachricht asynchron überprüft und eine geänderte Version zurückgibt.  <br/> |
|[Exchange 2013: Erstellen eines Transport-Agents für die Bandbreiten Protokollierung](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa) <br/> |Dieser Agent antwortet auf die [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) -und [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) -Ereignisse, erfasst die Bandbreitennutzung für bestimmte Empfänger und protokolliert die Informationen zur Bandbreitennutzung in einer Textdatei.  <br/> |
|[Exchange 2013: Erstellen eines Transport-Agents für die Text Konvertierung](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0) <br/> |Dieser Agent filtert Skripts aus e-Mail-Nachrichten, indem er das Format der eingehenden Nachricht ermittelt und entscheidet, ob eine Filterung erfolgen muss. Wenn eine Filterung erforderlich ist, wird der Inhalt in HTML konvertiert, gefiltert und anschließend wieder in das Quellformat konvertiert.  <br/> |
|[Exchange 2013: Erstellen eines Transport-Agents für die SMTP-Protokollierung](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-an-fc23dc33) <br/> |Dieser Agent antwortet auf das [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) -Ereignis und protokolliert die Nachricht asynchron in einer Datei auf der lokalen Festplatte.  <br/> |
|[Exchange 2013: Erstellen eines Transport-Agents, der Absender vorübergehend blockiert](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-52a767d8) <br/> |Dieser Agent antwortet auf die [OnEndOfHeaders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) -und [OnRcptCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnRcptCommand.aspx) -Ereignisse und bestimmt, ob der Absender der Nachricht zuvor Nachrichten an den Front-End-Transport-Dienst gesendet hat. Wenn der Absender zuvor keine Nachricht an den Front-End-Transport-Dienst gesendet hat, wird der Absender zu einer Liste von Absendern hinzugefügt, und die Nachricht wird mit einer Antwort zurückgewiesen, die den Client anweist, später erneut zu versuchen (auch bekannt als Greylisting). Wenn sich der Absender in der Liste der vorherigen Absender befindet, lehnt der Agent die Nachricht nicht ab.  <br/> |
|[Exchange 2013: Erstellen eines Postfachserver-Protokollierungs Transport-Agents](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-fc8632e5) <br/> |Dieser Agent antwortet auf das [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) -Transportpipeline Ereignis und protokolliert die Nachricht synchron in einer Datei auf der lokalen Festplatte.  <br/> |
|[Exchange 2013: Erstellen eines X-Header-Transport-Agents](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-an-32f62f5a) <br/> |Dieser Agent reagiert auf das [OnEndOfHeaders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) -Ereignis und liest und ändert X-Kopfzeilen in Nachrichten.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Transport-Agent-Konzepte in Exchange 2013](transport-agent-concepts-in-exchange-2013.md)    
- [Transport-Agent-Referenz für Exchange 2013](transport-agent-reference-for-exchange-2013.md)    
- [Erstellen eines Routing Agent-Transport-Agents für Exchange 2013](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md)   
- [Erstellen eines SmtpReceiveAgent-Transport-Agents für Exchange 2013](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)    
- [Erstellen eines DeliveryAgent-Transport-Agents für Exchange 2013](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)
    

