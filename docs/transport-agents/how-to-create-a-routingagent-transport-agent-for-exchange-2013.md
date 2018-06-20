---
title: Erstellen eines RoutingAgent-Transport-Agents für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f0e745f-9289-4f31-8877-926692a8c133
description: Erfahren Sie, wie Sie einen benutzerdefinierten RoutingAgent Transport-Agent für die Verwendung mit Exchange 2013 erstellen.
ms.openlocfilehash: d07f68494acd26940a4837bbbfc7a0505114bd20
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757183"
---
# <a name="create-a-routingagent-transport-agent-for-exchange-2013"></a>Erstellen eines RoutingAgent-Transport-Agents für Exchange 2013

Erfahren Sie, wie Sie einen benutzerdefinierten RoutingAgent Transport-Agent für die Verwendung mit Exchange 2013 erstellen.
  
**Gilt für:** Exchange Server 2013
  
Verwandte Codeabschnitte und Beispiel-apps:

- [Exchange 2013: Erstellen eines Bandbreite Protokollierung Transport-Agents](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa)
  
Die [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) und [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) Klassen sind die Basisklassen für Transport-Agents, die auf den Transportdienst auf einem Exchange Server 2013-Postfachserver ausgeführt werden sollen. Die [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) -Klasse stellt die Ereignisse aufgelistet, die in der folgenden Tabelle für die Handler in Ihrer RoutingAgent Transport-Agent implementiert werden kann. 
  
**In Tabelle 1. RoutingAgent-Klassenereignisse**

|Document.SelectionChanged **-Ereignis**|**Beschreibung**|
|:-----|:-----|
|[OnCategorizedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnCategorizedMessage.aspx) <br/> |Tritt auf, nachdem der Server die Konvertierung von Inhalten, führt bei Bedarf.  <br/> |
|[OnResolvedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnResolvedMessage.aspx) <br/> |Tritt auf, nachdem alle Empfänger der Nachricht behoben wurden und bevor routing bestimmt wird.  <br/> |
|[OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) <br/> |Tritt auf, nachdem der Server die Nachricht an den nächsten Hop leitet und führt die Konvertierung von Inhalten, falls erforderlich. Der Server möglicherweise mehr Ressourcen verwenden, um jede Nachricht in das [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) -Ereignis als das [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) -Ereignis nicht verarbeiten, da der Server führen Sie alle erforderlichen inhaltskonvertierung und bestimmen den nächsten Hop in der Route für die Nachricht Bevor sie den Code im Ereignishandler [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) ausgeführt wird.  <br/> |
|["OnSubmittedMessage"](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) <br/> |Tritt auf, nachdem die Nachricht aus der Warteschlange senden stammt. Verwenden Sie das [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) -Ereignis aus, wenn Ihre RoutingAgent Transport-Agent keine Konvertierung von Inhalten, aufgelösten Empfänger oder Weiterleiten von Daten erforderlich ist.  <br/> |
   
## <a name="creating-a-custom-routingagent-transport-agent"></a>Erstellen eines benutzerdefinierten RoutingAgent Transport-Agents

Das folgende Verfahren beschreibt, wie Sie einen benutzerdefinierten RoutingAgent Transport-Agent zu erstellen. 
  
### <a name="to-create-the-transport-agent"></a>So erstellen Sie den Transport-agent

1. Fügen Sie Verweise auf die Namespaces hinzu.
    
   ```cs
      using Microsoft.Exchange.Data.Mime;
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Routing;
  
   ```

   Diese Namespaces finden Sie auf Ihrem Exchange Server. Durch Hinzufügen eines Verweises auf die Namespaces, haben Sie Zugriff auf die [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) Member sowie andere Klassen in der [Exchange 2013: Erstellen Sie einen Transport-Agent Bandbreite Protokollierung](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa) Beispiel. 
    
2. Implementieren Sie die für die [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) -Klasse abgeleitete Klasse. 
    
   ```cs
      public class BandwidthLoggerFactory : RoutingAgentFactory
      {
          public override RoutingAgent CreateAgent(SmtpServer server)
          {
              return new BandwidthLogger(server);
          }
      }
  
   ```

   Dieser Code abgeleitete Klasse instanziieren und überschreiben Sie die **Hilfe von CreateAgent** -Methode zum Erstellen einer Instanz des neuen benutzerdefinierten Agents. Zusätzliche Methoden, z. B. **Schließen**, können auch in dieser Klasse, um benutzerdefinierten Code auszuführen, außer Kraft gesetzt werden. 
    
3. Definieren des Agents.
    
   ```cs
      public class BandwidthLogger : RoutingAgent
      {
          // Your custom code goes here
          public BandwidthLogger(SmtpServer server)
          {
              Debug.WriteLine(logPrefix + "Agent constructor");
              this.server = server;
              this.OnSubmittedMessage += SubmittedMessage;
              this.OnRoutedMessage += RoutedMessage;
          }
      }
  
   ```

   Nachdem Sie Ihre Agent-Klasse definiert haben, können Sie Sie benutzerdefinierten Funktionalität hinzufügen. In diesem Beispiel werden die beiden Ereignisse ["OnSubmittedMessage"](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) und ["OnRoutedMessage"](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)an Ihre benutzerdefinierte Ereignishandler umgeleitet. 
    
## <a name="see-also"></a>Siehe auch

- [Transport-Agent Konzepte in Exchange 2013](transport-agent-concepts-in-exchange-2013.md)    
- [Transport-Agent-Referenz für Exchange 2013](transport-agent-reference-for-exchange-2013.md)    
- [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx)    
- [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)
    

