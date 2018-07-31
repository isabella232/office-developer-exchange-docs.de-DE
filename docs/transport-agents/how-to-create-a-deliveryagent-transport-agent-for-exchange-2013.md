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
ms.openlocfilehash: bc36c7b5e0fb8006c5927d423d7767dcc7382ce0
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353308"
---
# <a name="create-a-deliveryagent-transport-agent-for-exchange-2013"></a>Erstellen eines DeliveryAgent-Transport-Agents für Exchange 2013

Erfahren Sie, wie Sie einen benutzerdefinierten DeliveryAgent Transport-Agent für die Verwendung mit Exchange 2013 erstellen.
  
**Gilt für:** Exchange Server 2013
  
Die [DeliveryAgentFactory\<Manager\> ](https://msdn.microsoft.com/en-us/library/dd877550(v=exchg.150).aspx) und [DeliveryAgent](https://msdn.microsoft.com/en-us/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) Klassen sind die Basisklassen für Transport-Agents, die auf den Transportdienst auf einem Exchange Server 2013-Postfachserver ausgeführt werden sollen. Sie möglicherweise Handler in Ihrer DeliveryAgent Transport-Agent für die Ereignisse bereitgestellt, die von der [DeliveryAgent](https://msdn.microsoft.com/en-us/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) -Klasse implementieren, die in der folgenden Tabelle aufgelistet sind. 
  
**In Tabelle 1. DeliveryAgent-Klassenereignisse**

|Document.SelectionChanged **-Ereignis**|**Beschreibung**|
|:-----|:-----|
|[OnCloseConnection](https://msdn.microsoft.com/en-us/library/microsoft.exchange.data.transport.delivery.deliveryagent.oncloseconnection(v=exchg.150).aspx) <br/> |Tritt auf, nachdem das letzte e-Mail-Element übermittelt wurde und die Verbindung wird geschlossen.  <br/> |
|[OnDeliverMailItem](https://msdn.microsoft.com/en-us/library/microsoft.exchange.data.transport.delivery.deliveryagent.ondelivermailitem(v=exchg.150).aspx) <br/> |Tritt auf, wenn ein e-Mail-Element übermittelt werden kann.  <br/> |
|[OnOpenConnection](https://msdn.microsoft.com/en-us/library/microsoft.exchange.data.transport.delivery.deliveryagent.onopenconnection(v=exchg.150).aspx) <br/> |Tritt auf, wenn der zustellungs-Agent für e-Mail-Übermittlung geöffnet wird.  <br/> |
   
## <a name="creating-a-custom-deliveryagent-transport-agent"></a>Erstellen eines benutzerdefinierten DeliveryAgent Transport-Agents

Das folgende Verfahren beschreibt, wie Sie einen benutzerdefinierten DeliveryAgent Transport-Agent zu erstellen. 
  
### <a name="to-create-the-transport-agent"></a>So erstellen Sie den Transport-agent

1. Fügen Sie Verweise auf die Namespaces hinzu.
    
   ```cs
        using Microsoft.Exchange.Data.Transport;
        using Microsoft.Exchange.Data.Transport.Delivery;
    
   ```

   Diese Namespaces finden Sie auf Ihrem Exchange Server. Hinzufügen eines Verweises auf die Namespaces, haben Sie Zugriff auf die Member [DeliveryAgent](https://msdn.microsoft.com/en-us/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) haben. 
    
2. Implementieren die abgeleitete Klasse für die [DeliveryAgentFactory\<Manager\> ](https://msdn.microsoft.com/en-us/library/dd877550(v=exchg.150).aspx) Klasse. 
    
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

   Dieser Code abgeleitete Klasse instanziieren und überschreiben Sie die **Hilfe von CreateAgent** -Methode zum Erstellen einer Instanz des neuen benutzerdefinierten Agents. Zusätzliche Methoden, z. B. **Schließen**, können auch in dieser Klasse, um benutzerdefinierten Code auszuführen, außer Kraft gesetzt werden. Eine [DeliveryAgentManager](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.aspx) -Klasse wird erstellt, um Überschreiben der [SupportedDeliveryProtocol](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.SupportedDeliveryProtocol.aspx) -Eigenschaft, und legen das Protokoll aus, das der Agent verwendet werden soll. 
    
3. Definieren des Agents.
    
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

   Nachdem Sie Ihre Agent-Klasse definiert haben, können Sie Sie benutzerdefinierten Funktionalität hinzufügen. In diesem werden Beispiel, das drei Ereignisse, [OnCloseConnection](https://msdn.microsoft.com/en-us/library/microsoft.exchange.data.transport.delivery.deliveryagent.oncloseconnection(v=exchg.150).aspx), [OnDeliverMailItem](https://msdn.microsoft.com/en-us/library/microsoft.exchange.data.transport.delivery.deliveryagent.ondelivermailitem(v=exchg.150).aspx)und [OnOpenConnection](https://msdn.microsoft.com/en-us/library/microsoft.exchange.data.transport.delivery.deliveryagent.onopenconnection(v=exchg.150).aspx), um Ihre benutzerdefinierte Ereignishandler umgeleitet. 
    
## <a name="see-also"></a>Siehe auch

- [Transport-Agent Konzepte in Exchange 2013](transport-agent-concepts-in-exchange-2013.md)
- [Transport-Agent-Referenz für Exchange 2013](transport-agent-reference-for-exchange-2013.md)          

 