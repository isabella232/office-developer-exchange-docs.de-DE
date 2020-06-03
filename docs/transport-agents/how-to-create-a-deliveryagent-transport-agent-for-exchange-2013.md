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
# <a name="create-a-deliveryagent-transport-agent-for-exchange-2013"></a>Erstellen eines DeliveryAgent-Transport-Agents für Exchange 2013

Erfahren Sie, wie Sie einen benutzerdefinierten DeliveryAgent-Transport-Agent für die Verwendung mit Exchange 2013 erstellen.
  
**Gilt für:** Exchange Server 2013
  
Die [DeliveryAgentFactory \<Manager\> ](https://msdn.microsoft.com/library/dd877550(v=exchg.150).aspx) -und [DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) -Klassen sind die Basisklassen für Transport-Agents, die für die Ausführung auf dem Transportdienst auf einem Exchange Server 2013 Post Fach Server ausgelegt sind. Sie können Handler in Ihrem DeliveryAgent-Transport-Agent für die von der [DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) -Klasse bereitgestellten Ereignisse implementieren, die in der folgenden Tabelle aufgeführt sind. 
  
**Tabelle 1. Ereignisse der DeliveryAgent-Klasse**

|**Event**|**Beschreibung**|
|:-----|:-----|
|[OnCloseConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.oncloseconnection(v=exchg.150).aspx) <br/> |Tritt ein, nachdem das letzte e-Mail-Element zugestellt wurde und die Verbindung geschlossen wurde.  <br/> |
|[OnDeliverMailItem](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.ondelivermailitem(v=exchg.150).aspx) <br/> |Tritt ein, wenn ein e-Mail-Element bereit zur Zustellung ist.  <br/> |
|[OnOpenConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.onopenconnection(v=exchg.150).aspx) <br/> |Tritt auf, wenn der Zustellungs-Agent zur e-Mail-Zustellung geöffnet wird.  <br/> |
   
## <a name="creating-a-custom-deliveryagent-transport-agent"></a>Erstellen eines benutzerdefinierten DeliveryAgent-Transport-Agents

Im folgenden Verfahren wird beschrieben, wie ein benutzerdefinierter DeliveryAgent-Transport-Agent erstellt wird. 
  
### <a name="to-create-the-transport-agent"></a>So erstellen Sie den Transport-Agent

1. Fügen Sie Verweise auf die Namespaces hinzu.
    
   ```cs
        using Microsoft.Exchange.Data.Transport;
        using Microsoft.Exchange.Data.Transport.Delivery;
    
   ```

   Sie können diese Namespaces auf Ihrem Exchange-Server finden. Durch Hinzufügen eines Verweises auf diese Namespaces haben Sie Zugriff auf die [DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) -Mitglieder. 
    
2. Implementieren Sie die abgeleitete Klasse für [die \<Manager\> DeliveryAgentFactory](https://msdn.microsoft.com/library/dd877550(v=exchg.150).aspx) -Klasse. 
    
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

   Mit diesem Code wird die abgeleitete Klasse instanziiert und die **createagent** -Methode überschrieben, um eine Instanz des neuen benutzerdefinierten Agents zu erstellen. Zusätzliche Methoden wie **Close**können in dieser Klasse auch zum Ausführen von benutzerdefiniertem Code überschrieben werden. Eine [DeliveryAgentManager](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.aspx) -Klasse wird erstellt, um die [SupportedDeliveryProtocol](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.SupportedDeliveryProtocol.aspx) -Eigenschaft außer Kraft zu setzen und das Protokoll festzulegen, das Ihr Agent verwenden wird. 
    
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

   Nachdem Sie Ihre Agent-Klasse definiert haben, können Sie benutzerdefinierte Funktionen hinzufügen. In diesem Beispiel werden die drei Ereignisse [OnCloseConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.oncloseconnection(v=exchg.150).aspx), [OnDeliverMailItem](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.ondelivermailitem(v=exchg.150).aspx)und [OnOpenConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.onopenconnection(v=exchg.150).aspx)zu Ihren benutzerdefinierten Ereignishandlern umgeleitet. 
    
## <a name="see-also"></a>Siehe auch

- [Transport-Agent-Konzepte in Exchange 2013](transport-agent-concepts-in-exchange-2013.md)
- [Transport-Agent-Referenz für Exchange 2013](transport-agent-reference-for-exchange-2013.md)          

 