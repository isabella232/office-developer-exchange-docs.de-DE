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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757183"
---
# <a name="create-a-routingagent-transport-agent-for-exchange-2013"></a><span data-ttu-id="24390-103">Erstellen eines RoutingAgent-Transport-Agents für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="24390-103">Create a RoutingAgent transport agent for Exchange 2013</span></span>

<span data-ttu-id="24390-104">Erfahren Sie, wie Sie einen benutzerdefinierten RoutingAgent Transport-Agent für die Verwendung mit Exchange 2013 erstellen.</span><span class="sxs-lookup"><span data-stu-id="24390-104">Find out how to create a custom RoutingAgent transport agent to use with Exchange 2013.</span></span>
  
<span data-ttu-id="24390-105">**Gilt für:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="24390-105">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="24390-106">Verwandte Codeabschnitte und Beispiel-apps:</span><span class="sxs-lookup"><span data-stu-id="24390-106">Related code snippets and sample apps:</span></span>

- [<span data-ttu-id="24390-107">Exchange 2013: Erstellen eines Bandbreite Protokollierung Transport-Agents</span><span class="sxs-lookup"><span data-stu-id="24390-107">Exchange 2013: Build a bandwidth logging transport agent</span></span>](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa)
  
<span data-ttu-id="24390-108">Die [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) und [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) Klassen sind die Basisklassen für Transport-Agents, die auf den Transportdienst auf einem Exchange Server 2013-Postfachserver ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="24390-108">The [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) and [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) classes are the base classes for transport agents that are designed to run on the transport service on an Exchange Server 2013 Mailbox server.</span></span> <span data-ttu-id="24390-109">Die [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) -Klasse stellt die Ereignisse aufgelistet, die in der folgenden Tabelle für die Handler in Ihrer RoutingAgent Transport-Agent implementiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="24390-109">The [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) class provides the events listed in the following table for which you might implement handlers in your RoutingAgent transport agent.</span></span> 
  
<span data-ttu-id="24390-110">**In Tabelle 1. RoutingAgent-Klassenereignisse**</span><span class="sxs-lookup"><span data-stu-id="24390-110">**Table 1. RoutingAgent class events**</span></span>

|<span data-ttu-id="24390-111">Document.SelectionChanged **-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="24390-111">**Event**</span></span>|<span data-ttu-id="24390-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="24390-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="24390-113">OnCategorizedMessage</span><span class="sxs-lookup"><span data-stu-id="24390-113">OnCategorizedMessage</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnCategorizedMessage.aspx) <br/> |<span data-ttu-id="24390-114">Tritt auf, nachdem der Server die Konvertierung von Inhalten, führt bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="24390-114">Occurs after the server performs content conversion, if it is required.</span></span>  <br/> |
|[<span data-ttu-id="24390-115">OnResolvedMessage</span><span class="sxs-lookup"><span data-stu-id="24390-115">OnResolvedMessage</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnResolvedMessage.aspx) <br/> |<span data-ttu-id="24390-116">Tritt auf, nachdem alle Empfänger der Nachricht behoben wurden und bevor routing bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="24390-116">Occurs after all the recipients of the message have been resolved and before routing is determined.</span></span>  <br/> |
|[<span data-ttu-id="24390-117">OnRoutedMessage</span><span class="sxs-lookup"><span data-stu-id="24390-117">OnRoutedMessage</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) <br/> |<span data-ttu-id="24390-118">Tritt auf, nachdem der Server die Nachricht an den nächsten Hop leitet und führt die Konvertierung von Inhalten, falls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="24390-118">Occurs after the server routes the message to the next hop and performs content conversion, if required.</span></span> <span data-ttu-id="24390-119">Der Server möglicherweise mehr Ressourcen verwenden, um jede Nachricht in das [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) -Ereignis als das [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) -Ereignis nicht verarbeiten, da der Server führen Sie alle erforderlichen inhaltskonvertierung und bestimmen den nächsten Hop in der Route für die Nachricht Bevor sie den Code im Ereignishandler [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="24390-119">The server might use more resources to process each message in the [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) event than the [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) event because the server will perform any necessary content conversion and determine the next hop in the route for the message before it executes the code in the [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) event handler.</span></span>  <br/> |
|[<span data-ttu-id="24390-120">"OnSubmittedMessage"</span><span class="sxs-lookup"><span data-stu-id="24390-120">OnSubmittedMessage</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) <br/> |<span data-ttu-id="24390-121">Tritt auf, nachdem die Nachricht aus der Warteschlange senden stammt.</span><span class="sxs-lookup"><span data-stu-id="24390-121">Occurs after the message is taken off the submit queue.</span></span> <span data-ttu-id="24390-122">Verwenden Sie das [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) -Ereignis aus, wenn Ihre RoutingAgent Transport-Agent keine Konvertierung von Inhalten, aufgelösten Empfänger oder Weiterleiten von Daten erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="24390-122">Use the [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) event if your RoutingAgent transport agent does not require content conversion, resolved recipients, or routing data.</span></span>  <br/> |
   
## <a name="creating-a-custom-routingagent-transport-agent"></a><span data-ttu-id="24390-123">Erstellen eines benutzerdefinierten RoutingAgent Transport-Agents</span><span class="sxs-lookup"><span data-stu-id="24390-123">Creating a custom RoutingAgent transport agent</span></span>

<span data-ttu-id="24390-124">Das folgende Verfahren beschreibt, wie Sie einen benutzerdefinierten RoutingAgent Transport-Agent zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="24390-124">The following procedure describes how to create a custom RoutingAgent transport agent.</span></span> 
  
### <a name="to-create-the-transport-agent"></a><span data-ttu-id="24390-125">So erstellen Sie den Transport-agent</span><span class="sxs-lookup"><span data-stu-id="24390-125">To create the transport agent</span></span>

1. <span data-ttu-id="24390-126">Fügen Sie Verweise auf die Namespaces hinzu.</span><span class="sxs-lookup"><span data-stu-id="24390-126">Add references to the namespaces.</span></span>
    
   ```cs
      using Microsoft.Exchange.Data.Mime;
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Routing;
  
   ```

   <span data-ttu-id="24390-127">Diese Namespaces finden Sie auf Ihrem Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="24390-127">You can find these namespaces on your Exchange server.</span></span> <span data-ttu-id="24390-128">Durch Hinzufügen eines Verweises auf die Namespaces, haben Sie Zugriff auf die [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) Member sowie andere Klassen in der [Exchange 2013: Erstellen Sie einen Transport-Agent Bandbreite Protokollierung](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa) Beispiel.</span><span class="sxs-lookup"><span data-stu-id="24390-128">By adding a reference to these namespaces, you will have access to the [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) members as well as other classes used in the [Exchange 2013: Build a bandwidth logging transport agent](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa) sample.</span></span> 
    
2. <span data-ttu-id="24390-129">Implementieren Sie die für die [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) -Klasse abgeleitete Klasse.</span><span class="sxs-lookup"><span data-stu-id="24390-129">Implement the derived class for the [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) class.</span></span> 
    
   ```cs
      public class BandwidthLoggerFactory : RoutingAgentFactory
      {
          public override RoutingAgent CreateAgent(SmtpServer server)
          {
              return new BandwidthLogger(server);
          }
      }
  
   ```

   <span data-ttu-id="24390-130">Dieser Code abgeleitete Klasse instanziieren und überschreiben Sie die **Hilfe von CreateAgent** -Methode zum Erstellen einer Instanz des neuen benutzerdefinierten Agents.</span><span class="sxs-lookup"><span data-stu-id="24390-130">This code will instantiate the derived class and override the **CreateAgent** method to create an instance of your new custom agent.</span></span> <span data-ttu-id="24390-131">Zusätzliche Methoden, z. B. **Schließen**, können auch in dieser Klasse, um benutzerdefinierten Code auszuführen, außer Kraft gesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="24390-131">Additional methods, such as **Close**, can also be overridden in this class to execute custom code.</span></span> 
    
3. <span data-ttu-id="24390-132">Definieren des Agents.</span><span class="sxs-lookup"><span data-stu-id="24390-132">Define your agent.</span></span>
    
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

   <span data-ttu-id="24390-133">Nachdem Sie Ihre Agent-Klasse definiert haben, können Sie Sie benutzerdefinierten Funktionalität hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="24390-133">After you define your agent class, you can add you custom functionality.</span></span> <span data-ttu-id="24390-134">In diesem Beispiel werden die beiden Ereignisse ["OnSubmittedMessage"](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) und ["OnRoutedMessage"](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)an Ihre benutzerdefinierte Ereignishandler umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="24390-134">In this example, the two events [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) and [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)are redirected to your custom event handlers.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="24390-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24390-135">See also</span></span>

- [<span data-ttu-id="24390-136">Transport-Agent Konzepte in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="24390-136">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)    
- [<span data-ttu-id="24390-137">Transport-Agent-Referenz für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="24390-137">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)    
- [<span data-ttu-id="24390-138">RoutingAgentFactory</span><span class="sxs-lookup"><span data-stu-id="24390-138">RoutingAgentFactory</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx)    
- [<span data-ttu-id="24390-139">RoutingAgent</span><span class="sxs-lookup"><span data-stu-id="24390-139">RoutingAgent</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)
    

