---
title: Erstellen eines DeliveryAgent-Transport-Agents für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4af904d7-b315-4849-92b1-66018f76ffdf
description: Erfahren Sie, wie Sie einen benutzerdefinierten DeliveryAgent-Transport-Agent für die Verwendung mit Exchange 2013 erstellen.
ms.openlocfilehash: b349f0b6d835ba3d6195b43e80d1dcd21750bf82
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527572"
---
# <a name="create-a-deliveryagent-transport-agent-for-exchange-2013"></a><span data-ttu-id="7652d-103">Erstellen eines DeliveryAgent-Transport-Agents für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="7652d-103">Create a DeliveryAgent transport agent for Exchange 2013</span></span>

<span data-ttu-id="7652d-104">Erfahren Sie, wie Sie einen benutzerdefinierten DeliveryAgent-Transport-Agent für die Verwendung mit Exchange 2013 erstellen.</span><span class="sxs-lookup"><span data-stu-id="7652d-104">Find out how to create a custom DeliveryAgent transport agent to use with Exchange 2013.</span></span>
  
<span data-ttu-id="7652d-105">**Gilt für:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="7652d-105">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="7652d-106">Die [DeliveryAgentFactory \<Manager\> ](https://msdn.microsoft.com/library/dd877550(v=exchg.150).aspx) -und [DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) -Klassen sind die Basisklassen für Transport-Agents, die für die Ausführung auf dem Transportdienst auf einem Exchange Server 2013 Post Fach Server ausgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="7652d-106">The [DeliveryAgentFactory\<Manager\>](https://msdn.microsoft.com/library/dd877550(v=exchg.150).aspx) and [DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) classes are the base classes for transport agents that are designed to run on the Transport service on an Exchange Server 2013 Mailbox server.</span></span> <span data-ttu-id="7652d-107">Sie können Handler in Ihrem DeliveryAgent-Transport-Agent für die von der [DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) -Klasse bereitgestellten Ereignisse implementieren, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="7652d-107">You might implement handlers in your DeliveryAgent transport agent for the events provided by the [DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) class that are listed in the following table.</span></span> 
  
<span data-ttu-id="7652d-108">**Tabelle 1. Ereignisse der DeliveryAgent-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7652d-108">**Table 1. DeliveryAgent class events**</span></span>

|<span data-ttu-id="7652d-109">**Event**</span><span class="sxs-lookup"><span data-stu-id="7652d-109">**Event**</span></span>|<span data-ttu-id="7652d-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7652d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7652d-111">[OnCloseConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.oncloseconnection(v=exchg.150).aspx)</span><span class="sxs-lookup"><span data-stu-id="7652d-111">[OnCloseConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.oncloseconnection(v=exchg.150).aspx)</span></span> <br/> |<span data-ttu-id="7652d-112">Tritt ein, nachdem das letzte e-Mail-Element zugestellt wurde und die Verbindung geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="7652d-112">Occurs after the last mail item has been delivered and the connection is closed.</span></span>  <br/> |
|<span data-ttu-id="7652d-113">[OnDeliverMailItem](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.ondelivermailitem(v=exchg.150).aspx)</span><span class="sxs-lookup"><span data-stu-id="7652d-113">[OnDeliverMailItem](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.ondelivermailitem(v=exchg.150).aspx)</span></span> <br/> |<span data-ttu-id="7652d-114">Tritt ein, wenn ein e-Mail-Element bereit zur Zustellung ist.</span><span class="sxs-lookup"><span data-stu-id="7652d-114">Occurs when a mail item is ready to be delivered.</span></span>  <br/> |
|<span data-ttu-id="7652d-115">[OnOpenConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.onopenconnection(v=exchg.150).aspx)</span><span class="sxs-lookup"><span data-stu-id="7652d-115">[OnOpenConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.onopenconnection(v=exchg.150).aspx)</span></span> <br/> |<span data-ttu-id="7652d-116">Tritt auf, wenn der Zustellungs-Agent zur e-Mail-Zustellung geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="7652d-116">Occurs when the delivery agent is opened for mail delivery.</span></span>  <br/> |
   
## <a name="creating-a-custom-deliveryagent-transport-agent"></a><span data-ttu-id="7652d-117">Erstellen eines benutzerdefinierten DeliveryAgent-Transport-Agents</span><span class="sxs-lookup"><span data-stu-id="7652d-117">Creating a custom DeliveryAgent transport agent</span></span>

<span data-ttu-id="7652d-118">Im folgenden Verfahren wird beschrieben, wie ein benutzerdefinierter DeliveryAgent-Transport-Agent erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7652d-118">The following procedure describes how to create a custom DeliveryAgent transport agent.</span></span> 
  
### <a name="to-create-the-transport-agent"></a><span data-ttu-id="7652d-119">So erstellen Sie den Transport-Agent</span><span class="sxs-lookup"><span data-stu-id="7652d-119">To create the transport agent</span></span>

1. <span data-ttu-id="7652d-120">Fügen Sie Verweise auf die Namespaces hinzu.</span><span class="sxs-lookup"><span data-stu-id="7652d-120">Add references to the namespaces.</span></span>
    
   ```cs
        using Microsoft.Exchange.Data.Transport;
        using Microsoft.Exchange.Data.Transport.Delivery;
    
   ```

   <span data-ttu-id="7652d-121">Sie können diese Namespaces auf Ihrem Exchange-Server finden.</span><span class="sxs-lookup"><span data-stu-id="7652d-121">You can find these namespaces on your Exchange server.</span></span> <span data-ttu-id="7652d-122">Durch Hinzufügen eines Verweises auf diese Namespaces haben Sie Zugriff auf die [DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) -Mitglieder.</span><span class="sxs-lookup"><span data-stu-id="7652d-122">By adding a reference to these namespaces, you will have access to the [DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) members.</span></span> 
    
2. <span data-ttu-id="7652d-123">Implementieren Sie die abgeleitete Klasse für [die \<Manager\> DeliveryAgentFactory](https://msdn.microsoft.com/library/dd877550(v=exchg.150).aspx) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="7652d-123">Implement the derived class for the [DeliveryAgentFactory\<Manager\>](https://msdn.microsoft.com/library/dd877550(v=exchg.150).aspx) class.</span></span> 
    
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

   <span data-ttu-id="7652d-124">Mit diesem Code wird die abgeleitete Klasse instanziiert und die **createagent** -Methode überschrieben, um eine Instanz des neuen benutzerdefinierten Agents zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7652d-124">This code will instantiate the derived class and override the **CreateAgent** method to create an instance of your new custom agent.</span></span> <span data-ttu-id="7652d-125">Zusätzliche Methoden wie **Close**können in dieser Klasse auch zum Ausführen von benutzerdefiniertem Code überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="7652d-125">Additional methods, such as **Close**, can also be overridden in this class to execute custom code.</span></span> <span data-ttu-id="7652d-126">Eine [DeliveryAgentManager](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.aspx) -Klasse wird erstellt, um die [SupportedDeliveryProtocol](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.SupportedDeliveryProtocol.aspx) -Eigenschaft außer Kraft zu setzen und das Protokoll festzulegen, das Ihr Agent verwenden wird.</span><span class="sxs-lookup"><span data-stu-id="7652d-126">A [DeliveryAgentManager](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.aspx) class is created to override the [SupportedDeliveryProtocol](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.SupportedDeliveryProtocol.aspx) property and set the protocol your agent will use.</span></span> 
    
3. <span data-ttu-id="7652d-127">Definieren Sie Ihren Agent.</span><span class="sxs-lookup"><span data-stu-id="7652d-127">Define your agent.</span></span>
    
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

   <span data-ttu-id="7652d-128">Nachdem Sie Ihre Agent-Klasse definiert haben, können Sie benutzerdefinierte Funktionen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7652d-128">After you define your agent class, you can add you custom functionality.</span></span> <span data-ttu-id="7652d-129">In diesem Beispiel werden die drei Ereignisse [OnCloseConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.oncloseconnection(v=exchg.150).aspx), [OnDeliverMailItem](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.ondelivermailitem(v=exchg.150).aspx)und [OnOpenConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.onopenconnection(v=exchg.150).aspx)zu Ihren benutzerdefinierten Ereignishandlern umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="7652d-129">In this example, the three events, [OnCloseConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.oncloseconnection(v=exchg.150).aspx), [OnDeliverMailItem](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.ondelivermailitem(v=exchg.150).aspx), and [OnOpenConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.onopenconnection(v=exchg.150).aspx), are redirected to your custom event handlers.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="7652d-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7652d-130">See also</span></span>

- [<span data-ttu-id="7652d-131">Transport-Agent-Konzepte in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="7652d-131">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)
- [<span data-ttu-id="7652d-132">Transport-Agent-Referenz für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="7652d-132">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)          

 