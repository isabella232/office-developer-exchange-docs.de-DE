---
title: Erstellen eines Routing Agent-Transport-Agents für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f0e745f-9289-4f31-8877-926692a8c133
description: Erfahren Sie, wie Sie einen benutzerdefinierten Routing Agent-Transport-Agent für die Verwendung mit Exchange 2013 erstellen.
ms.openlocfilehash: 9acf30be0dd795098f757effaa34b2e72183b000
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463699"
---
# <a name="create-a-routingagent-transport-agent-for-exchange-2013"></a>Erstellen eines Routing Agent-Transport-Agents für Exchange 2013

Erfahren Sie, wie Sie einen benutzerdefinierten Routing Agent-Transport-Agent für die Verwendung mit Exchange 2013 erstellen.
  
**Gilt für:** Exchange Server 2013
  
Zugehörige Codeausschnitte und Beispiel-apps:

- [Exchange 2013: Erstellen eines Transport-Agents für die Bandbreiten Protokollierung](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa)
  
Die [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) -und [Routing Agent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) -Klassen sind die Basisklassen für Transport-Agents, die für die Ausführung auf dem Transportdienst auf einem Exchange Server 2013 Post Fach Server ausgelegt sind. Die [Routing Agent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) -Klasse stellt die in der folgenden Tabelle aufgeführten Ereignisse bereit, für die Sie Handler in Ihrem Routing Agent-Transport-Agent implementieren können. 
  
**Tabelle 1. Ereignisse der Routing Agent-Klasse**

|**Event**|**Beschreibung**|
|:-----|:-----|
|[OnCategorizedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnCategorizedMessage.aspx) <br/> |Tritt auf, nachdem der Server die Inhaltskonvertierung ausgeführt hat, sofern erforderlich.  <br/> |
|[OnResolvedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnResolvedMessage.aspx) <br/> |Tritt auf, nachdem alle Empfänger der Nachricht aufgelöst wurden und bevor das Routing bestimmt wird.  <br/> |
|[OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) <br/> |Tritt auf, nachdem der Server die Nachricht an den nächsten Hop weitergeleitet und bei Bedarf die Inhaltskonvertierung durchführt. Der Server verwendet möglicherweise mehr Ressourcen zum Verarbeiten der einzelnen Nachrichten im [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) -Ereignis als das [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) -Ereignis, da der Server alle erforderlichen Inhaltskonvertierungen durchführt und den nächsten Hop in der Route für die Nachricht bestimmt, bevor der Code im [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) -Ereignishandler ausgeführt wird.  <br/> |
|[OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) <br/> |Tritt auf, nachdem die Nachricht aus der Sendewarteschlange entfernt wurde. Verwenden Sie das [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) -Ereignis, wenn Ihr Routing Agent-Transport-Agent keine Inhaltskonvertierung, aufgelöste Empfänger oder Routingdaten erfordert.  <br/> |
   
## <a name="creating-a-custom-routingagent-transport-agent"></a>Erstellen eines benutzerdefinierten Routing Agent-Transport-Agents

Im folgenden Verfahren wird beschrieben, wie ein benutzerdefinierter Routing Agent-Transport-Agent erstellt wird. 
  
### <a name="to-create-the-transport-agent"></a>So erstellen Sie den Transport-Agent

1. Fügen Sie Verweise auf die Namespaces hinzu.
    
   ```cs
      using Microsoft.Exchange.Data.Mime;
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Routing;
  
   ```

   Sie können diese Namespaces auf Ihrem Exchange-Server finden. Durch Hinzufügen eines Verweises auf diese Namespaces haben Sie Zugriff auf die [Routing Agent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) -Member sowie auf andere Klassen, die im [Exchange 2013: Erstellen eines Transport-Agent](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa) -Beispiels für die Bandbreiten Protokollierung verwendet werden. 
    
2. Implementieren Sie die abgeleitete Klasse für die [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) -Klasse. 
    
   ```cs
      public class BandwidthLoggerFactory : RoutingAgentFactory
      {
          public override RoutingAgent CreateAgent(SmtpServer server)
          {
              return new BandwidthLogger(server);
          }
      }
  
   ```

   Mit diesem Code wird die abgeleitete Klasse instanziiert und die **createagent** -Methode überschrieben, um eine Instanz des neuen benutzerdefinierten Agents zu erstellen. Zusätzliche Methoden wie **Close**können in dieser Klasse auch zum Ausführen von benutzerdefiniertem Code überschrieben werden. 
    
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

   Nachdem Sie Ihre Agent-Klasse definiert haben, können Sie benutzerdefinierte Funktionen hinzufügen. In diesem Beispiel werden die beiden Ereignisse [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) und [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)zu Ihren benutzerdefinierten Ereignishandlern umgeleitet. 
    
## <a name="see-also"></a>Siehe auch

- [Transport-Agent-Konzepte in Exchange 2013](transport-agent-concepts-in-exchange-2013.md)    
- [Transport-Agent-Referenz für Exchange 2013](transport-agent-reference-for-exchange-2013.md)    
- [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx)    
- [Routing Agent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)
    

