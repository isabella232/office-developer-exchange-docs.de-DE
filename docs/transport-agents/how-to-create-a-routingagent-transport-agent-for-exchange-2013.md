---
title: Erstellen eines RoutingAgent-Transport-Agents für Exchange 2013
manager: sethgros
ms.date: 09/21/2021
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3f0e745f-9289-4f31-8877-926692a8c133
description: Erfahren Sie, wie Sie einen benutzerdefinierten RoutingAgent-Transport-Agent für die Verwendung mit Exchange 2013 erstellen.
ms.openlocfilehash: 89c70e7d021b9b2cc46f65ee3bbff334430fecc7
ms.sourcegitcommit: f13a3a4a61fa23ca6414b7c96ddf087adbe3dc9e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/11/2021
ms.locfileid: "60262211"
---
# <a name="create-a-routingagent-transport-agent-for-exchange-2013"></a>Erstellen eines RoutingAgent-Transport-Agents für Exchange 2013

Erfahren Sie, wie Sie einen benutzerdefinierten RoutingAgent-Transport-Agent für die Verwendung mit Exchange 2013 erstellen.
  
**Gilt für:** Exchange Server 2013
  
Verwandte Codeausschnitte und Beispiel-Apps:

- [Exchange 2013: Erstellen eines Transport-Agents für die Bandbreitenprotokollierung](/exchange/client-developer/transport-agents/transport-agent-code-samples-for-exchange-2013.md)
  
Die [RoutingAgentFactory-](https://docs.microsoft.com/previous-versions/office/exchange-server-api/aa564164(v=exchg.150)) und [RoutingAgent-Klassen](https://docs.microsoft.com/previous-versions/office/exchange-server-api/aa564421(v=exchg.150)) sind die Basisklassen für Transport-Agents, die für die Ausführung auf dem Transportdienst auf einem Exchange Server 2013-Postfachserver entwickelt wurden. Die [RoutingAgent-Klasse](https://docs.microsoft.com/previous-versions/office/exchange-server-api/aa564421(v=exchg.150)) stellt die in der folgenden Tabelle aufgeführten Ereignisse bereit, für die Sie Handler in Ihrem RoutingAgent-Transport-Agent implementieren können. 
  
**Tabelle 1. RoutingAgent-Klassenereignisse**

|Document.SelectionChanged **-Ereignis**|**Beschreibung**|
|:-----|:-----|
|[OnCategorizedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnCategorizedMessage.aspx) <br/> |Tritt auf, nachdem der Server die Inhaltskonvertierung ausgeführt hat, falls erforderlich.  <br/> |
|[OnResolvedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnResolvedMessage.aspx) <br/> |Tritt auf, nachdem alle Empfänger der Nachricht aufgelöst wurden und bevor das Routing bestimmt wird.  <br/> |
|[OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) <br/> |Tritt auf, nachdem der Server die Nachricht an den nächsten Hop weitergibt und bei Bedarf eine Inhaltskonvertierung durchführt. Der Server verwendet möglicherweise mehr Ressourcen zum Verarbeiten jeder Nachricht im [OnRoutedMessage-Ereignis](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) als das [OnSubmittedMessage-Ereignis,](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) da der Server alle erforderlichen Inhaltskonvertierungen durchführt und den nächsten Hop in der Route für die Nachricht bestimmt, bevor der Code im [OnRoutedMessage-Ereignishandler](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) ausgeführt wird.  <br/> |
|[OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) <br/> |Tritt auf, nachdem die Nachricht aus der Sendewarteschlange entfernt wurde. Verwenden Sie das [OnSubmittedMessage-Ereignis,](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) wenn ihr RoutingAgent-Transport-Agent keine Inhaltskonvertierung, aufgelöste Empfänger oder Routingdaten erfordert.  <br/> |
   
## <a name="creating-a-custom-routingagent-transport-agent"></a>Erstellen eines benutzerdefinierten RoutingAgent-Transport-Agents

Im folgenden Verfahren wird beschrieben, wie Sie einen benutzerdefinierten RoutingAgent-Transport-Agent erstellen. 
  
### <a name="to-create-the-transport-agent"></a>So erstellen Sie den Transport-Agent

1. Fügen Sie Verweise auf die Namespaces hinzu.
    
   ```cs
      using Microsoft.Exchange.Data.Mime;
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Routing;
  
   ```

   Sie finden diese Namespaces auf Ihrem Exchange Server. Durch Hinzufügen eines Verweises auf diese Namespaces haben Sie Zugriff auf die [RoutingAgent-Member](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) sowie auf andere Klassen, die im [Exchange 2013: Erstellen eines Transport-Agent-Beispiels](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa) für die Bandbreitenprotokollierung verwendet werden. 
    
2. Implementieren Sie die abgeleitete Klasse für die [RoutingAgentFactory-Klasse.](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) 
    
   ```cs
      public class BandwidthLoggerFactory : RoutingAgentFactory
      {
          public override RoutingAgent CreateAgent(SmtpServer server)
          {
              return new BandwidthLogger(server);
          }
      }
  
   ```

   Dieser Code instanziiert die abgeleitete Klasse und überschreibt die **CreateAgent-Methode,** um eine Instanz des neuen benutzerdefinierten Agents zu erstellen. Zusätzliche Methoden, z. **B. Close**, können in dieser Klasse auch überschrieben werden, um benutzerdefinierten Code auszuführen. 
    
3. Definieren Sie Ihren Agent.
    
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

   Nachdem Sie die Agentklasse definiert haben, können Sie benutzerdefinierte Funktionen hinzufügen. In diesem Beispiel werden die beiden Ereignisse [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) und [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)an ihre benutzerdefinierten Ereignishandler umgeleitet. 
    
## <a name="see-also"></a>Weitere Artikel

- [Transport-Agent-Konzepte in Exchange 2013](transport-agent-concepts-in-exchange-2013.md)    
- [Transport-Agent-Referenz für Exchange 2013](transport-agent-reference-for-exchange-2013.md)    
- [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx)    
- [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)
    

