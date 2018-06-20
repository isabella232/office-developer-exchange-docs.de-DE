---
title: Erstellen eines DeliveryAgent-Transport-Agents für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4af904d7-b315-4849-92b1-66018f76ffdf
description: Erfahren Sie, wie Sie einen benutzerdefinierten DeliveryAgent Transport-Agent für die Verwendung mit Exchange 2013 erstellen.
ms.openlocfilehash: 44ee5dc465f4435f0b835d264331cb719fe875c1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757173"
---
# <a name="create-a-deliveryagent-transport-agent-for-exchange-2013"></a><span data-ttu-id="8a950-103">Erstellen eines DeliveryAgent-Transport-Agents für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8a950-103">Create a DeliveryAgent transport agent for Exchange 2013</span></span>

<span data-ttu-id="8a950-104">Erfahren Sie, wie Sie einen benutzerdefinierten DeliveryAgent Transport-Agent für die Verwendung mit Exchange 2013 erstellen.</span><span class="sxs-lookup"><span data-stu-id="8a950-104">Find out how to create a custom DeliveryAgent transport agent to use with Exchange 2013.</span></span>
  
<span data-ttu-id="8a950-105">**Gilt für:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="8a950-105">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="8a950-106">Die [DeliveryAgentFactory\<Manager\> ](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentFactory`1.aspx) und [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.DeliveryType.DeliveryAgent.aspx) Klassen sind die Basisklassen für Transport-Agents, die auf den Transportdienst auf einem Exchange Server 2013-Postfachserver ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8a950-106">The [DeliveryAgentFactory\<Manager\>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentFactory`1.aspx) and [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.DeliveryType.DeliveryAgent.aspx) classes are the base classes for transport agents that are designed to run on the Transport service on an Exchange Server 2013 Mailbox server.</span></span> <span data-ttu-id="8a950-107">Sie möglicherweise Handler in Ihrer DeliveryAgent Transport-Agent für die Ereignisse bereitgestellt, die von der [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.DeliveryType.DeliveryAgent.aspx) -Klasse implementieren, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="8a950-107">You might implement handlers in your DeliveryAgent transport agent for the events provided by the [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.DeliveryType.DeliveryAgent.aspx) class that are listed in the following table.</span></span> 
  
<span data-ttu-id="8a950-108">**In Tabelle 1. DeliveryAgent-Klassenereignisse**</span><span class="sxs-lookup"><span data-stu-id="8a950-108">**Table 1. DeliveryAgent class events**</span></span>

|<span data-ttu-id="8a950-109">Document.SelectionChanged **-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="8a950-109">**Event**</span></span>|<span data-ttu-id="8a950-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8a950-110">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8a950-111">OnCloseConnection</span><span class="sxs-lookup"><span data-stu-id="8a950-111">OnCloseConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.OnCloseConnection.aspx) <br/> |<span data-ttu-id="8a950-112">Tritt auf, nachdem das letzte e-Mail-Element übermittelt wurde und die Verbindung wird geschlossen.</span><span class="sxs-lookup"><span data-stu-id="8a950-112">Occurs after the last mail item has been delivered and the connection is closed.</span></span>  <br/> |
|[<span data-ttu-id="8a950-113">OnDeliverMailItem</span><span class="sxs-lookup"><span data-stu-id="8a950-113">OnDeliverMailItem</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.OnDeliverMailItem.aspx) <br/> |<span data-ttu-id="8a950-114">Tritt auf, wenn ein e-Mail-Element übermittelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8a950-114">Occurs when a mail item is ready to be delivered.</span></span>  <br/> |
|[<span data-ttu-id="8a950-115">OnOpenConnection</span><span class="sxs-lookup"><span data-stu-id="8a950-115">OnOpenConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.OnOpenConnection.aspx) <br/> |<span data-ttu-id="8a950-116">Tritt auf, wenn der zustellungs-Agent für e-Mail-Übermittlung geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="8a950-116">Occurs when the delivery agent is opened for mail delivery.</span></span>  <br/> |
   
## <a name="creating-a-custom-deliveryagent-transport-agent"></a><span data-ttu-id="8a950-117">Erstellen eines benutzerdefinierten DeliveryAgent Transport-Agents</span><span class="sxs-lookup"><span data-stu-id="8a950-117">Creating a custom DeliveryAgent transport agent</span></span>

<span data-ttu-id="8a950-118">Das folgende Verfahren beschreibt, wie Sie einen benutzerdefinierten DeliveryAgent Transport-Agent zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8a950-118">The following procedure describes how to create a custom DeliveryAgent transport agent.</span></span> 
  
### <a name="to-create-the-transport-agent"></a><span data-ttu-id="8a950-119">So erstellen Sie den Transport-agent</span><span class="sxs-lookup"><span data-stu-id="8a950-119">To create the transport agent</span></span>

1. <span data-ttu-id="8a950-120">Fügen Sie Verweise auf die Namespaces hinzu.</span><span class="sxs-lookup"><span data-stu-id="8a950-120">Add references to the namespaces.</span></span>
    
   ```cs
        using Microsoft.Exchange.Data.Transport;
        using Microsoft.Exchange.Data.Transport.Delivery;
    
   ```

   <span data-ttu-id="8a950-121">Diese Namespaces finden Sie auf Ihrem Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8a950-121">You can find these namespaces on your Exchange server.</span></span> <span data-ttu-id="8a950-122">Hinzufügen eines Verweises auf die Namespaces, haben Sie Zugriff auf die Member [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.DeliveryType.DeliveryAgent.aspx) haben.</span><span class="sxs-lookup"><span data-stu-id="8a950-122">By adding a reference to these namespaces, you will have access to the [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.DeliveryType.DeliveryAgent.aspx) members.</span></span> 
    
2. <span data-ttu-id="8a950-123">Implementieren die abgeleitete Klasse für die [DeliveryAgentFactory\<Manager\> ](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentFactory`1.aspx) Klasse.</span><span class="sxs-lookup"><span data-stu-id="8a950-123">Implement the derived class for the [DeliveryAgentFactory\<Manager\>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentFactory`1.aspx) class.</span></span> 
    
   ```cs
      public class MyDeliveryAgentFactory : DeliveryAgentFactory<MyDeliveryAgentFactory.MyDeliveryAgentManager>
      {
          static MyDeliveryAgentFactory()
          {
          }
          public override DeliveryAgent CreateAgent(SmtpServer server)
          {
              return new MyDeliveryAgent(server);
          }
          public sealed class MyDeliveryAgentManager : DeliveryAgentManager
          {
              /// <summary>
              /// Gets the supported delivery protocol.
              /// </summary>
              public override string SupportedDeliveryProtocol
              {
                  get { return "MyProtocol"; }
              }
          }
      }
  
   ```

   <span data-ttu-id="8a950-124">Dieser Code abgeleitete Klasse instanziieren und überschreiben Sie die **Hilfe von CreateAgent** -Methode zum Erstellen einer Instanz des neuen benutzerdefinierten Agents.</span><span class="sxs-lookup"><span data-stu-id="8a950-124">This code will instantiate the derived class and override the **CreateAgent** method to create an instance of your new custom agent.</span></span> <span data-ttu-id="8a950-125">Zusätzliche Methoden, z. B. **Schließen**, können auch in dieser Klasse, um benutzerdefinierten Code auszuführen, außer Kraft gesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="8a950-125">Additional methods, such as **Close**, can also be overridden in this class to execute custom code.</span></span> <span data-ttu-id="8a950-126">Eine [DeliveryAgentManager](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.aspx) -Klasse wird erstellt, um Überschreiben der [SupportedDeliveryProtocol](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.SupportedDeliveryProtocol.aspx) -Eigenschaft, und legen das Protokoll aus, das der Agent verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8a950-126">A [DeliveryAgentManager](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.aspx) class is created to override the [SupportedDeliveryProtocol](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.SupportedDeliveryProtocol.aspx) property and set the protocol your agent will use.</span></span> 
    
3. <span data-ttu-id="8a950-127">Definieren des Agents.</span><span class="sxs-lookup"><span data-stu-id="8a950-127">Define your agent.</span></span>
    
   ```cs
      public class MyDeliveryAgent : DeliveryAgent
      {
          public MyDeliveryAgent(SmtpServer server)
          {
              this.OnCloseConnection += CloseConnection;
              this.OnDeliverMailItem += DeliverMailItem;
              this.OnOpenConnection += OpenConnection;
          }
      }
  
   ```

   <span data-ttu-id="8a950-128">Nachdem Sie Ihre Agent-Klasse definiert haben, können Sie Sie benutzerdefinierten Funktionalität hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8a950-128">After you define your agent class, you can add you custom functionality.</span></span> <span data-ttu-id="8a950-129">In diesem Beispiel werden die drei folgenden Ereignisse, [OnCloseConnection](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.OnCloseConnection.aspx) , [OnDeliverMailItem](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.OnDeliverMailItem.aspx) und [OnOpenConnection](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.OnOpenConnection.aspx) , an die benutzerdefinierte Ereignishandler umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8a950-129">In this example, the three events, [OnCloseConnection](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.OnCloseConnection.aspx) , [OnDeliverMailItem](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.OnDeliverMailItem.aspx) and [OnOpenConnection](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.OnOpenConnection.aspx) , are redirected to your custom event handlers.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="8a950-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a950-130">See also</span></span>

- [<span data-ttu-id="8a950-131">Transport-Agent Konzepte in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8a950-131">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)
- [<span data-ttu-id="8a950-132">Transport-Agent-Referenz für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8a950-132">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)    
- [<span data-ttu-id="8a950-133">DeliveryAgentFactory\<Manager\></span><span class="sxs-lookup"><span data-stu-id="8a950-133">DeliveryAgentFactory\<Manager\></span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentFactory`1.aspx)   
- [<span data-ttu-id="8a950-134">DeliveryAgent</span><span class="sxs-lookup"><span data-stu-id="8a950-134">DeliveryAgent</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.DeliveryType.DeliveryAgent.aspx)    
- [<span data-ttu-id="8a950-135">DeliveryAgentManager</span><span class="sxs-lookup"><span data-stu-id="8a950-135">DeliveryAgentManager</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.aspx)
    

