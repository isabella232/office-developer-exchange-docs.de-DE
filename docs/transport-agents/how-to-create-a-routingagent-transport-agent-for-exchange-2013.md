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
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463699"
---
# <a name="create-a-routingagent-transport-agent-for-exchange-2013"></a><span data-ttu-id="3e296-103">Erstellen eines Routing Agent-Transport-Agents für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="3e296-103">Create a RoutingAgent transport agent for Exchange 2013</span></span>

<span data-ttu-id="3e296-104">Erfahren Sie, wie Sie einen benutzerdefinierten Routing Agent-Transport-Agent für die Verwendung mit Exchange 2013 erstellen.</span><span class="sxs-lookup"><span data-stu-id="3e296-104">Find out how to create a custom RoutingAgent transport agent to use with Exchange 2013.</span></span>
  
<span data-ttu-id="3e296-105">**Gilt für:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="3e296-105">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="3e296-106">Zugehörige Codeausschnitte und Beispiel-apps:</span><span class="sxs-lookup"><span data-stu-id="3e296-106">Related code snippets and sample apps:</span></span>

- [<span data-ttu-id="3e296-107">Exchange 2013: Erstellen eines Transport-Agents für die Bandbreiten Protokollierung</span><span class="sxs-lookup"><span data-stu-id="3e296-107">Exchange 2013: Build a bandwidth logging transport agent</span></span>](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa)
  
<span data-ttu-id="3e296-108">Die [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) -und [Routing Agent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) -Klassen sind die Basisklassen für Transport-Agents, die für die Ausführung auf dem Transportdienst auf einem Exchange Server 2013 Post Fach Server ausgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="3e296-108">The [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) and [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) classes are the base classes for transport agents that are designed to run on the transport service on an Exchange Server 2013 Mailbox server.</span></span> <span data-ttu-id="3e296-109">Die [Routing Agent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) -Klasse stellt die in der folgenden Tabelle aufgeführten Ereignisse bereit, für die Sie Handler in Ihrem Routing Agent-Transport-Agent implementieren können.</span><span class="sxs-lookup"><span data-stu-id="3e296-109">The [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) class provides the events listed in the following table for which you might implement handlers in your RoutingAgent transport agent.</span></span> 
  
<span data-ttu-id="3e296-110">**Tabelle 1. Ereignisse der Routing Agent-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3e296-110">**Table 1. RoutingAgent class events**</span></span>

|<span data-ttu-id="3e296-111">**Event**</span><span class="sxs-lookup"><span data-stu-id="3e296-111">**Event**</span></span>|<span data-ttu-id="3e296-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3e296-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3e296-113">OnCategorizedMessage</span><span class="sxs-lookup"><span data-stu-id="3e296-113">OnCategorizedMessage</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnCategorizedMessage.aspx) <br/> |<span data-ttu-id="3e296-114">Tritt auf, nachdem der Server die Inhaltskonvertierung ausgeführt hat, sofern erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3e296-114">Occurs after the server performs content conversion, if it is required.</span></span>  <br/> |
|[<span data-ttu-id="3e296-115">OnResolvedMessage</span><span class="sxs-lookup"><span data-stu-id="3e296-115">OnResolvedMessage</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnResolvedMessage.aspx) <br/> |<span data-ttu-id="3e296-116">Tritt auf, nachdem alle Empfänger der Nachricht aufgelöst wurden und bevor das Routing bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="3e296-116">Occurs after all the recipients of the message have been resolved and before routing is determined.</span></span>  <br/> |
|[<span data-ttu-id="3e296-117">OnRoutedMessage</span><span class="sxs-lookup"><span data-stu-id="3e296-117">OnRoutedMessage</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) <br/> |<span data-ttu-id="3e296-118">Tritt auf, nachdem der Server die Nachricht an den nächsten Hop weitergeleitet und bei Bedarf die Inhaltskonvertierung durchführt.</span><span class="sxs-lookup"><span data-stu-id="3e296-118">Occurs after the server routes the message to the next hop and performs content conversion, if required.</span></span> <span data-ttu-id="3e296-119">Der Server verwendet möglicherweise mehr Ressourcen zum Verarbeiten der einzelnen Nachrichten im [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) -Ereignis als das [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) -Ereignis, da der Server alle erforderlichen Inhaltskonvertierungen durchführt und den nächsten Hop in der Route für die Nachricht bestimmt, bevor der Code im [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) -Ereignishandler ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3e296-119">The server might use more resources to process each message in the [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) event than the [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) event because the server will perform any necessary content conversion and determine the next hop in the route for the message before it executes the code in the [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) event handler.</span></span>  <br/> |
|[<span data-ttu-id="3e296-120">OnSubmittedMessage</span><span class="sxs-lookup"><span data-stu-id="3e296-120">OnSubmittedMessage</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) <br/> |<span data-ttu-id="3e296-121">Tritt auf, nachdem die Nachricht aus der Sendewarteschlange entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="3e296-121">Occurs after the message is taken off the submit queue.</span></span> <span data-ttu-id="3e296-122">Verwenden Sie das [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) -Ereignis, wenn Ihr Routing Agent-Transport-Agent keine Inhaltskonvertierung, aufgelöste Empfänger oder Routingdaten erfordert.</span><span class="sxs-lookup"><span data-stu-id="3e296-122">Use the [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) event if your RoutingAgent transport agent does not require content conversion, resolved recipients, or routing data.</span></span>  <br/> |
   
## <a name="creating-a-custom-routingagent-transport-agent"></a><span data-ttu-id="3e296-123">Erstellen eines benutzerdefinierten Routing Agent-Transport-Agents</span><span class="sxs-lookup"><span data-stu-id="3e296-123">Creating a custom RoutingAgent transport agent</span></span>

<span data-ttu-id="3e296-124">Im folgenden Verfahren wird beschrieben, wie ein benutzerdefinierter Routing Agent-Transport-Agent erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3e296-124">The following procedure describes how to create a custom RoutingAgent transport agent.</span></span> 
  
### <a name="to-create-the-transport-agent"></a><span data-ttu-id="3e296-125">So erstellen Sie den Transport-Agent</span><span class="sxs-lookup"><span data-stu-id="3e296-125">To create the transport agent</span></span>

1. <span data-ttu-id="3e296-126">Fügen Sie Verweise auf die Namespaces hinzu.</span><span class="sxs-lookup"><span data-stu-id="3e296-126">Add references to the namespaces.</span></span>
    
   ```cs
      using Microsoft.Exchange.Data.Mime;
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Routing;
  
   ```

   <span data-ttu-id="3e296-127">Sie können diese Namespaces auf Ihrem Exchange-Server finden.</span><span class="sxs-lookup"><span data-stu-id="3e296-127">You can find these namespaces on your Exchange server.</span></span> <span data-ttu-id="3e296-128">Durch Hinzufügen eines Verweises auf diese Namespaces haben Sie Zugriff auf die [Routing Agent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) -Member sowie auf andere Klassen, die im [Exchange 2013: Erstellen eines Transport-Agent](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa) -Beispiels für die Bandbreiten Protokollierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3e296-128">By adding a reference to these namespaces, you will have access to the [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) members as well as other classes used in the [Exchange 2013: Build a bandwidth logging transport agent](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa) sample.</span></span> 
    
2. <span data-ttu-id="3e296-129">Implementieren Sie die abgeleitete Klasse für die [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="3e296-129">Implement the derived class for the [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) class.</span></span> 
    
   ```cs
      public class BandwidthLoggerFactory : RoutingAgentFactory
      {
          public override RoutingAgent CreateAgent(SmtpServer server)
          {
              return new BandwidthLogger(server);
          }
      }
  
   ```

   <span data-ttu-id="3e296-130">Mit diesem Code wird die abgeleitete Klasse instanziiert und die **createagent** -Methode überschrieben, um eine Instanz des neuen benutzerdefinierten Agents zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3e296-130">This code will instantiate the derived class and override the **CreateAgent** method to create an instance of your new custom agent.</span></span> <span data-ttu-id="3e296-131">Zusätzliche Methoden wie **Close**können in dieser Klasse auch zum Ausführen von benutzerdefiniertem Code überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="3e296-131">Additional methods, such as **Close**, can also be overridden in this class to execute custom code.</span></span> 
    
3. <span data-ttu-id="3e296-132">Definieren Sie Ihren Agent.</span><span class="sxs-lookup"><span data-stu-id="3e296-132">Define your agent.</span></span>
    
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

   <span data-ttu-id="3e296-133">Nachdem Sie Ihre Agent-Klasse definiert haben, können Sie benutzerdefinierte Funktionen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3e296-133">After you define your agent class, you can add you custom functionality.</span></span> <span data-ttu-id="3e296-134">In diesem Beispiel werden die beiden Ereignisse [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) und [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)zu Ihren benutzerdefinierten Ereignishandlern umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="3e296-134">In this example, the two events [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) and [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)are redirected to your custom event handlers.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="3e296-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e296-135">See also</span></span>

- [<span data-ttu-id="3e296-136">Transport-Agent-Konzepte in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="3e296-136">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)    
- [<span data-ttu-id="3e296-137">Transport-Agent-Referenz für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="3e296-137">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)    
- [<span data-ttu-id="3e296-138">RoutingAgentFactory</span><span class="sxs-lookup"><span data-stu-id="3e296-138">RoutingAgentFactory</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx)    
- [<span data-ttu-id="3e296-139">Routing Agent</span><span class="sxs-lookup"><span data-stu-id="3e296-139">RoutingAgent</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)
    

