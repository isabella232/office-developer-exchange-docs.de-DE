---
title: Transport-Agent-Konzepte in Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 0c700af8-2792-4d3f-8571-8860e0550d8e
description: Hier finden Sie Informationen dazu, wie sich die Transport-Agent-Pipeline und die Serverrollenarchitektur in Exchange 2013 auf die Transport-Agent-Entwicklung auswirken und welche Klassen Sie zum Entwickeln von Transport-Agents verwenden können.
ms.openlocfilehash: 9116c9b7811958a2479421a642052df3cee24e34
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59537161"
---
# <a name="transport-agent-concepts-in-exchange-2013"></a>Transport-Agent-Konzepte in Exchange 2013

Hier finden Sie Informationen dazu, wie sich die Transport-Agent-Pipeline und die Serverrollenarchitektur in Exchange 2013 auf die Transport-Agent-Entwicklung auswirken und welche Klassen Sie zum Entwickeln von Transport-Agents verwenden können. 
  
**Gilt für:** Exchange Server 2013 
  
Sie können die in Exchange Server 2013 bereitgestellte Klassenbibliothek verwenden, um Transport-Agents zu implementieren, die sich für Ereignisse registrieren und Aktionen für Nachrichten ausführen, während sie die Transportpipeline passieren. Sie können auch Transport-Agents verwenden, um Nachrichten zu ändern und Inhalte zu konvertieren. 
  
Dieser Artikel enthält Informationen zu Transport-Agents und der Transportpipelinearchitektur. Es ist wichtig, die Architektur der Transportpipeline zu verstehen, damit Sie das Transportverhalten an die Anforderungen Ihrer Organisation anpassen können. Dieser Artikel enthält auch Informationen zu Änderungen in der Exchange 2013-Architektur, die sich auf Transport-Agents auswirken, und zu den Klassen, die Sie zum Entwickeln von Transport-Agents verwenden können. 
  
## <a name="transport-agents-in-the-transport-pipeline"></a>Transport-Agents in der Transportpipeline
<a name="Pipeline"> </a>

Transport-Agents werden von einer der folgenden drei Klassen abgeleitet:
  
- [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)
- [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)
- [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.aspx)
    
Die Transportpipeline bezieht sich auf den Nachrichtendatenfluss innerhalb der Grenzen einer Exchange 2013-Organisation. Die Pipeline besteht aus den in der folgenden Tabelle aufgeführten Diensten.
  
**Tabelle 1. Transportpipelinedienste**

|**Dienst**|**Beschreibung**|**Unterstützte Klassen**|
|:-----|:-----|:-----|
|Front-End-Transport  <br/> |Wird auf allen [Clientzugriffsservern](https://technet.microsoft.com/library/dd298114%28v=exchg.150%29.aspx) ausgeführt und fungiert als statusloser Proxy für den gesamten eingehenden und ausgehenden externen SMTP-Datenverkehr für die Exchange 2013-Organisation. Der Front-End-Transport-Dienst prüft nachrichteninhalt nicht oder warteschlange nachrichten lokal. Es kommuniziert mit dem Transportdienst auf einem [Postfachserver.](https://technet.microsoft.com/library/jj150491%28v=exchg.150%29.aspx)  <br/> |[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) <br/> |
|Transport  <br/> |Wird auf allen Postfachservern ausgeführt und ähnelt der [Hub-Transport-Serverrolle](https://technet.microsoft.com/library/bb123494%28v=exchg.141%29.aspx) in Exchange Server 2010. Der Transportdienst leitet Nachrichten zwischen sich selbst und den Postfach- und Front-End-Transport-Diensten weiter. Dieser Dienst kommuniziert nicht direkt mit Postfachdatenbanken.  <br/> |[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) <br/> [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) <br/> [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.aspx) <br/> |
|Postfachtransportdienst  <br/> |Wird auf allen Postfachservern ausgeführt und besteht aus zwei separaten Diensten: Postfachtransportübermittlung und Postfachtransportübermittlung. Die Postfachtransportübermittlung empfängt SMTP-Nachrichten vom Transportdienst und stellt eine Verbindung mit der Postfachdatenbank her, indem ein Exchange Remoteprozeduraufruf (Remote Procedure Call, RPC) zum Übermitteln der Nachricht verwendet wird. Die Postfachtransportübermittlung stellt mithilfe von RPC eine Verbindung mit der Postfachdatenbank her, um Nachrichten abzurufen, und sendet die Nachrichten über SMTP an den Transportdienst.  <br/> |Keine  <br/> |
   
### <a name="transport-events"></a>Transportereignisse
<a name="Events"> </a>

Sie implementieren Transport-Agents, indem Sie sich zuerst für ein Ereignis registrieren und dann eine Aktion ausführen, wenn dieses Ereignis ausgelöst wird. Jeder der drei Agenttypen kann sich für einen anderen Satz von Ereignissen registrieren.
  
Die folgende Abbildung zeigt, wo transport-Agents in der Transportpipeline für Ereignisse registrieren können.
  
**Abbildung 1. Transportereignisse**

![Abbildung des Nachrichtenflusses durch die Transportpipeline und Ereignisse, für die sich jeder Agent registrieren kann beginnend mit Smtp-Ereignissen für den SmtpReceivedAgent, dann für Categorizor-Ereignisse für den RoutingAgent und schließlich für Übermittlungsereignisse für den DeliveryAgent.](media/TAConceptsFig1.png)
  
Wenn eine Nachricht in die Transportpipeline gelangt, kann ein von der [SmtpReceiveAgent-Klasse abgeleiteter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) Transport-Agent während eines der SMTP-Ereignisse, für die der Agent registriert wurde, auf die Nachricht reagieren. Ein von der [RoutingAgent-Klasse](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) abgeleiteter Agent kann auf jedes der vier Kategorisierungsereignisse reagieren, für die er registriert wurde. Ein von der [DeliveryAgent-Klasse](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.aspx) abgeleiteter Agent kann während eines der Übermittlungsereignisse, für die er registriert wurde, auf eine Nachricht reagieren. 
  
## <a name="transport-agents-and-server-roles"></a>Transport-Agents und Serverrollen
<a name="ServerRoles"> </a>

Änderungen an der Serverrollenarchitektur in Exchange 2013 wirken sich auf Transport-Agents und deren Möglichkeiten aus. Exchange 2013 umfasst die folgenden Serverrollen:
  
- Postfachserver – Umfasst Clientzugriffsprotokolle, den Transportdienst, Postfachdatenbanken und Unified Messaging-Komponenten. Der Postfachserver kommuniziert direkt mit Active Directory Domain Services (AD DS), Clientzugriffsservern und E-Mail-Clients wie Outlook.
    
- Clientzugriffsserver – Bietet Authentifizierung, eingeschränkte Umleitung, Proxydienste und Clientzugriffsprotokolle wie HTTP, POP, IMAP und SMTP.
    
- Edge-Transport-Server – Leitet E-Mails in eine und aus einer Organisation weiter. Edge-Transport-Server befinden sich in der Regel am Umkreis einer Exchange Topologie.
    
Diese konsolidierte Struktur reduziert die Anzahl der Server, die in einer Exchange 2013-Umgebung bereitgestellt werden müssen. Administratoren müssen keine Hub-Transport- und Clientzugriffsserver mehr an jedem Active Directory-Standort bereitstellen, der einen Postfachserver enthält, und sie müssen nicht mehr alle Serverrollen aktualisieren, um neue Funktionen nutzen zu können.
  
Diese Änderungen an der Serverrollenarchitektur können sich potenziell darauf auswirken, wo in der Pipeline Ihr Agent auf Ereignisse reagieren kann. Wenn Sie Transport-Agents für Versionen von Exchange vor Exchange 2013 erstellt haben, überprüfen Sie die Architekturänderungen, um festzustellen, ob Sie Änderungen an Ihren Agents vornehmen müssen.
  
Die folgende Abbildung zeigt, wie die Architekturänderungen in Exchange 2013 zu einer optimierten, konsolidierten Transportpipeline führen. In dieser Abbildung werden Clientzugriffsserver als CAS bezeichnet. Und Postfachserver werden als MBX bezeichnet.
  
**Abbildung 2. Serverrollenarchitektur Exchange 2013**

![Abbildung des Clientdatenverkehrs durch eine externe Firewall und den Edge-Transport-Server auf der linken Seite, der Datenverkehr über einen Lastenausgleich der Ebene 4 an ein konsolidiertes Clientzugriffsserver-Array und eine Gruppe von Postfachservern in einer Database Availability Group auf der rechten Seite übergibt.](media/Transport_Agent_Concepts_Fig_3.png)
  
Die folgende Abbildung zeigt die Interaktionen zwischen den Serverrollen Exchange 2013.
  
**Abbildung 3. Postfach- und Clientzugriffsserverinteraktionen**

![Abbildung von Interaktionen beginnen mit Pfeilen vom Clientdatenverkehr, der einen Lastenausgleich der Ebene 4 durchläuft, der 4 Ziele auf dem Clientzugriffsserver hat: IIS/HTTP Proxy, POP/IMAP, SMTP und UM. Die Pfeile werden an ihre dazugehörigen Ziele im Postfachspeicher übergeben.](media/Transport_Agent_Concepts_Fig_4.png)
  
Weitere Informationen zu Änderungen an der Serverrollenarchitektur Exchange 2013 finden Sie unter [Exchange 2013-Architektur](https://technet.microsoft.com/library/jj150540%28v=exchg.150%29.aspx#BKMK_Arch) in [What's New in Exchange 2013.](https://technet.microsoft.com/library/jj150540%28v=exchg.150%29.aspx) 
  
## <a name="transport-agent-classes"></a>Transport-Agent-Klassen
<a name="Create"> </a>

Die Klasse, von der ihr Transport-Agent abgeleitet ist, bestimmt die Ereignisse, für die sich ihr Agent registrieren kann. Ihr Agent enthält in der Regel eine Agentklasse, eine Agent-Factory, einen oder mehrere Ereignishandler und den Code, der die Aktionen ausführt, die Der Agent ausführen soll.
  
In der folgenden Tabelle sind die Klassen aufgeführt, von denen für jeden Agenttyp abgeleitet werden soll.
  
**Tabelle 2. Agentklassen**

||||
|:-----|:-----|:-----|
|Agenttyp  <br/> |Factory-Basisklasse  <br/> |Agent-Basisklasse  <br/> |
|SMTP-Empfang  <br/> |[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) <br/> |[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) <br/> |
|Routing  <br/> |[RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) <br/> |[RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) <br/> |
|Übermittlung  <br/> |[DeliveryAgentFactory\<Manager\>](https://msdn.microsoft.com/library/dd877550(v=exchg.150).aspx) <br/> |[DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) <br/> |
   
Diese Basisklassen für Factory und Agent stellen Eigenschaften und Methoden bereit, mit denen Sie auf Transportereignisse und Nachrichten zugreifen können. Implementieren Sie Klassen in Ihrem Agent, die von diesen Klassen erben. Überschreiben Sie in der von der Agent factory abgeleiteten Klasse die **CreateAgent-Methode,** sodass sie eine neue Instanz der Agentklasse zurückgibt. 
  
An die Ereignisse übergebene Argumente können eine Instanz der [EmailMessage-Klasse](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Email.EmailMessage.aspx) enthalten, mit der Sie die Eigenschaften und inhalte der zugrunde liegenden Nachricht ändern können. Nicht alle Nachrichteninformationen sind in jedem Ereignis verfügbar. Sie müssen bestimmen, welcher Agent und welches Ereignis für die Aufgabe am besten geeignet ist, die Sie ausführen möchten. 
  
Die folgenden Namespaces enthalten Typen, die Sie zum Lesen, Schreiben und Ändern von Nachrichten in der Transportpipeline verwenden können:
  
- [Microsoft. Exchange. Data.Mime.Encoders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.aspx)
    
- [Microsoft. Exchange. Data.ContentTypes.iCalendar](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.aspx)
    
- [Microsoft. Exchange. Data.Mime](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.aspx)
    
- [Microsoft. Exchange. Data.ContentTypes.Tnef](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.aspx)
    
- [Microsoft. Exchange. Data.ContentTypes.vCard](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.vCard.aspx)
    
Nachdem Sie den Transport-Agent geschrieben haben, [installieren und verwalten](https://technet.microsoft.com/library/bb125175%28v=exchg.150%29.aspx) Sie den Agent mithilfe der Exchange Verwaltungsshell. Weitere Informationen finden Sie unter [Erstellen von Transport-Agents für Exchange 2013.](creating-transport-agents-for-exchange-2013.md) 
  
## <a name="see-also"></a>Siehe auch

- [Transport-Agents in Exchange](transport-agents-in-exchange-2013.md)    
- [Transport-Agent-Referenz für Exchange 2013](transport-agent-reference-for-exchange-2013.md)   
- [Lesen und Ändern von Nachrichten in der Exchange 2013-Transportpipeline](reading-and-modifying-messages-in-the-exchange-2013-transport-pipeline.md)    
- [Neuigkeiten in Exchange 2013](https://technet.microsoft.com/library/jj150540%28v=exchg.150%29.aspx)   
- [serverrollenarchitektur Exchange 2013](https://blogs.technet.com/b/exchange/archive/2013/01/23/exchange-2013-server-role-architecture.aspx)    
- [Postfach- und Clientzugriffsserver](https://technet.microsoft.com/library/jj150519%28v=exchg.150%29.aspx)   
- [Exchange Server 2013 E-Mail-Flow](https://technet.microsoft.com/library/aa996349.aspx)
- [Exchange Server 2013 E-Mail-Routing](https://technet.microsoft.com/library/aa998825%28v=exchg.150%29.aspx)   
- [Exchange Server-PowerShell (Exchange-Verwaltungsshell)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)
    

