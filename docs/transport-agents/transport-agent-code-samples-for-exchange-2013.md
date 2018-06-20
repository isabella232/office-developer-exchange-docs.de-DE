---
title: Transport-Agent-Codebeispiele für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 626345ec-918f-4d91-932f-e6ce92553ccb
description: Hier finden Sie Informationen zu den Beispiel-Transport-Agents, die für Exchange 2013 verfügbar sind.
ms.openlocfilehash: 122a3351748fa6ffd823a51ce65ffb913332cb2c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757200"
---
# <a name="transport-agent-code-samples-for-exchange-2013"></a>Transport-Agent-Codebeispiele für Exchange 2013

Hier finden Sie Informationen zu den Beispiel-Transport-Agents, die für Exchange 2013 verfügbar sind.
  
**Gilt für:** Exchange Server 2013
  
Sie können die APIs, die in Exchange Server 2013 Agents zu entwickeln, die Erweiterung der Funktionalität Transport enthalten sind. Dieser Artikel enthält Informationen über die Beispiel-Agents, die zur einfacheren erfahren, wie zur programmgesteuerten Erweiterung von Transport Verhalten verfügbar sind. Die Beispiel-Agenten enthalten den Quellcode für die einzelnen Komponenten. 
  
Die folgende Tabelle enthält die Beispiel-Agents für Exchange 2013.
  
**In Tabelle 1. Transport-Agent-Beispiele**

|**Name des Beispiels**|**Beschreibung**|
|:-----|:-----|
|[Exchange 2013: Erstellen eines antivirus Transport-Agents](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-an-6e544269) <br/> |Dieser Agent reagiert auf die Ereignisse ["OnEndofData"](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) und ["OnSubmittedMessage"](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) und sendet die eingehende Nachricht an einen Out-of-Process-Server, der asynchron untersucht die Meldung und gibt eine geänderte Version zurück.  <br/> |
|[Exchange 2013: Erstellen eines Bandbreite Protokollierung Transport-Agents](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa) <br/> |Dieser Agent reagiert auf die Ereignisse ["OnSubmittedMessage"](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) und ["OnRoutedMessage"](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) , zeichnet Auslastung der Bandbreite zur angegebenen Empfänger und die Informationen zur Verwendung von Bandbreite in eine Textdatei protokolliert.  <br/> |
|[Exchange 2013: Erstellen eines Stelle Konvertierung Transport-Agents](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0) <br/> |Dieser Agent filtert Skripts aus e-Mail-Nachrichten nach bestimmen das Format der eingehenden Nachricht und die Entscheidung, ob Filtern ausgeführt werden muss. Falls Filtern erforderlich ist, wird der Inhalt in HTML konvertiert, gefiltert und dann wieder in das Format der Quelle konvertiert.  <br/> |
|[Exchange 2013: Erstellen eines SMTP-Protokollierung Transport-Agents](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-an-fc23dc33) <br/> |Dieser Agent reagiert auf das Ereignis [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) und asynchron protokolliert die Nachricht in einer Datei auf der lokalen Festplatte.  <br/> |
|[Exchange 2013: Erstellen Sie einen Transport-Agent, der Absender vorübergehend blockiert](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-52a767d8) <br/> |Dieser Agent reagiert auf die Ereignisse ["OnEndOfHeaders"](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) und [OnRcptCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnRcptCommand.aspx) und bestimmt, ob der Absender der Nachricht an den Front-End-Transport-Dienst zuvor Nachrichten gesendet hat. Wenn der Absender nicht zuvor eine Nachricht an den Front-End-Transport-Dienst gesendet, der Absender eine Liste der Absender hinzugefügt wird und die Nachricht, eine Antwort, die den Client zurückgewiesen wird zu einem späteren Zeitpunkt erneut versuchen weist (auch bekannt als graue Liste). Wenn der Absender in der Liste der vorherigen Absender ist, lehnt der Agent die Nachricht nicht.  <br/> |
|[Exchange 2013: Erstellen Sie einen Transport-Agent Mailbox-Server-Protokollierung](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-fc8632e5) <br/> |Dieser Agent reagiert auf die Pipeline [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) Transportereignis und synchron protokolliert die Nachricht in einer Datei auf der lokalen Festplatte.  <br/> |
|[Exchange 2013: Erstellen eines X-Header-Transport-Agents](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-an-32f62f5a) <br/> |Dieser Agent reagiert auf das Ereignis ["OnEndOfHeaders"](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) und lesen und Ändern von X-Header in Nachrichten.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Transport-Agent Konzepte in Exchange 2013](transport-agent-concepts-in-exchange-2013.md)    
- [Transport-Agent-Referenz für Exchange 2013](transport-agent-reference-for-exchange-2013.md)    
- [Erstellen eines RoutingAgent-Transport-Agents für Exchange 2013](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md)   
- [Erstellen eines SmtpReceiveAgent Transport-Agents für Exchange 2013](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)    
- [Erstellen eines DeliveryAgent-Transport-Agents für Exchange 2013](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)
    

