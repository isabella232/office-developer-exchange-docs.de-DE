---
title: Erstellen eines DeliveryAgent-Transport-Agents für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 4af904d7-b315-4849-92b1-66018f76ffdf
description: Erfahren Sie, wie Sie einen benutzerdefinierten DeliveryAgent-Transport-Agent für die Verwendung mit Exchange 2013 erstellen.
ms.openlocfilehash: b465c3bbd4658bea700d5be9f4eb16ae81693717
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59526933"
---
# <a name="create-a-deliveryagent-transport-agent-for-exchange-2013"></a>Erstellen eines DeliveryAgent-Transport-Agents für Exchange 2013

Erfahren Sie, wie Sie einen benutzerdefinierten DeliveryAgent-Transport-Agent für die Verwendung mit Exchange 2013 erstellen.
  
**Gilt für:** Exchange Server 2013
  
Die [Klassen \<Manager\> DeliveryAgentFactory](https://msdn.microsoft.com/library/dd877550(v=exchg.150).aspx) und [DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) sind die Basisklassen für Transport-Agents, die für die Ausführung auf dem Transportdienst auf einem Exchange Server 2013-Postfachserver entwickelt wurden. Sie können Handler in Ihrem DeliveryAgent-Transport-Agent für die Ereignisse implementieren, die von der [DeliveryAgent-Klasse](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) bereitgestellt werden, die in der folgenden Tabelle aufgeführt sind. 
  
**Tabelle 1. DeliveryAgent-Klassenereignisse**

|Document.SelectionChanged **-Ereignis**|**Beschreibung**|
|:-----|:-----|
|[OnCloseConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.oncloseconnection(v=exchg.150).aspx) <br/> |Tritt ein, nachdem das letzte E-Mail-Element zugestellt wurde und die Verbindung geschlossen wurde.  <br/> |
|[OnDeliverMailItem](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.ondelivermailitem(v=exchg.150).aspx) <br/> |Tritt auf, wenn ein E-Mail-Element für die Zustellung bereit ist.  <br/> |
|[OnOpenConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.onopenconnection(v=exchg.150).aspx) <br/> |Tritt auf, wenn der Zustellungs-Agent für die E-Mail-Zustellung geöffnet wird.  <br/> |
   
## <a name="creating-a-custom-deliveryagent-transport-agent"></a>Erstellen eines benutzerdefinierten DeliveryAgent-Transport-Agents

Im folgenden Verfahren wird beschrieben, wie Sie einen benutzerdefinierten DeliveryAgent-Transport-Agent erstellen. 
  
### <a name="to-create-the-transport-agent"></a>So erstellen Sie den Transport-Agent

1. Fügen Sie Verweise auf die Namespaces hinzu.
    
   ```cs
        using Microsoft.Exchange.Data.Transport;
        using Microsoft.Exchange.Data.Transport.Delivery;
    
   ```

   Sie finden diese Namespaces auf Ihrem Exchange Server. Durch Hinzufügen eines Verweises auf diese Namespaces haben Sie Zugriff auf die [DeliveryAgent-Elemente.](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) 
    
2. Implementieren Sie die abgeleitete Klasse für die [ \<Manager\> DeliveryAgentFactory-Klasse.](https://msdn.microsoft.com/library/dd877550(v=exchg.150).aspx) 
    
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

   Dieser Code instanziiert die abgeleitete Klasse und überschreibt die **CreateAgent-Methode,** um eine Instanz des neuen benutzerdefinierten Agents zu erstellen. Zusätzliche Methoden, z. **B. Close**, können in dieser Klasse auch überschrieben werden, um benutzerdefinierten Code auszuführen. Eine [DeliveryAgentManager-Klasse](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.aspx) wird erstellt, um die [SupportedDeliveryProtocol-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.SupportedDeliveryProtocol.aspx) zu überschreiben und das Protokoll festzulegen, das der Agent verwendet. 
    
3. Definieren Sie Ihren Agent.
    
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

   Nachdem Sie die Agentklasse definiert haben, können Sie benutzerdefinierte Funktionen hinzufügen. In diesem Beispiel werden die drei Ereignisse ["OnCloseConnection",](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.oncloseconnection(v=exchg.150).aspx) ["OnDeliverMailItem"](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.ondelivermailitem(v=exchg.150).aspx)und ["OnOpenConnection"](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.onopenconnection(v=exchg.150).aspx)an die benutzerdefinierten Ereignishandler umgeleitet. 
    
## <a name="see-also"></a>Siehe auch

- [Transport-Agent-Konzepte in Exchange 2013](transport-agent-concepts-in-exchange-2013.md)
- [Transport-Agent-Referenz für Exchange 2013](transport-agent-reference-for-exchange-2013.md)          

 