---
title: Transport-Agent-Konzepte in Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c700af8-2792-4d3f-8571-8860e0550d8e
description: Hier finden Sie Informationen dazu, wie sich die Transport-Agent-Pipeline und die Serverrollen Architektur in Exchange 2013 auf die Entwicklung von Transport-Agents auswirken, sowie die Klassen, mit denen Sie Transport-Agents entwickeln können.
ms.openlocfilehash: b9552ea4398ac8135a11b48eb7e7bdf5ec81985e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527558"
---
# <a name="transport-agent-concepts-in-exchange-2013"></a>Transport-Agent-Konzepte in Exchange 2013

Hier finden Sie Informationen dazu, wie sich die Transport-Agent-Pipeline und die Serverrollen Architektur in Exchange 2013 auf die Entwicklung von Transport-Agents auswirken, sowie die Klassen, mit denen Sie Transport-Agents entwickeln können. 
  
**Gilt für:** Exchange Server 2013 
  
Sie können die in Exchange Server 2013 bereitgestellte Klassenbibliothek verwenden, um Transport-Agents zu implementieren, die sich für Ereignisse registrieren und Aktionen für Nachrichten ausführen, während Sie die Transportpipeline durchlaufen. Sie können auch Transport-Agents verwenden, um Nachrichten zu ändern und Inhalte zu konvertieren. 
  
Dieser Artikel enthält Informationen zu Transport-Agents und zur Transportpipeline Architektur. Es ist wichtig, dass Sie die Architektur der Transportpipeline kennen, damit Sie das Transportverhalten so ändern können, dass es den Anforderungen Ihrer Organisation entspricht. Dieser Artikel enthält auch Informationen zu Änderungen in der Exchange 2013 Architektur, die Transport-Agents und die Klassen betreffen, die Sie zum Entwickeln von Transport-Agents verwenden können. 
  
## <a name="transport-agents-in-the-transport-pipeline"></a>Transport-Agents in der Transportpipeline
<a name="Pipeline"> </a>

Transport-Agents werden von einer der folgenden drei Klassen abgeleitet:
  
- [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)
- [Routing Agent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)
- [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.aspx)
    
Die Transportpipeline bezieht sich auf den Fluss von Nachrichtendaten innerhalb der Grenzen einer Exchange 2013 Organisation. Die Pipeline besteht aus den in der folgenden Tabelle aufgeführten Diensten.
  
**Tabelle 1. Transport Pipeline Dienste**

|**Dienst**|**Beschreibung**|**Unterstützte Klassen**|
|:-----|:-----|:-----|
|Front-End-Transport  <br/> |Wird auf allen [Client Zugriffsservern](https://technet.microsoft.com/library/dd298114%28v=exchg.150%29.aspx) ausgeführt und fungiert als statusfreier Proxy für den gesamten eingehenden und ausgehenden externen SMTP-Datenverkehr für die Exchange 2013 Organisation. Der Front-End-Transport-Dienst überprüft Nachrichteninhalte nicht lokal oder keine Nachrichten in der Warteschlange. Er kommuniziert mit dem Transport Dienst auf einem [Postfachserver](https://technet.microsoft.com/library/jj150491%28v=exchg.150%29.aspx).  <br/> |[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) <br/> |
|Transport  <br/> |Wird auf allen Postfachservern ausgeführt und ähnelt der [Hub-Transport-Server](https://technet.microsoft.com/library/bb123494%28v=exchg.141%29.aspx) Rolle in Exchange Server 2010. Der Transport Dienst leitet Nachrichten zwischen sich selbst und den postfachtransport-und Front-End-Transportdiensten weiter. Dieser Dienst kommuniziert nicht direkt mit Postfachdatenbanken.  <br/> |[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) <br/> [Routing Agent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) <br/> [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.aspx) <br/> |
|Postfachtransportdienst  <br/> |Wird auf allen Postfachservern ausgeführt und besteht aus zwei getrennten Diensten: postfachtransportübermittlung und postfachtransportzustellung. Die postfachtransportzustellung empfängt SMTP-Nachrichten vom Transport Dienst und stellt mithilfe eines Exchange-Remoteprozeduraufrufs (RPC) eine Verbindung mit der Postfachdatenbank her, um die Nachricht zuzustellen. Die Post Fach Transport Übermittlung stellt mithilfe von RPC eine Verbindung mit der Postfachdatenbank her, um Nachrichten abzurufen, und sendet die Nachrichten über SMTP an den Transport Dienst.  <br/> |Keine.  <br/> |
   
### <a name="transport-events"></a>Transport Ereignisse
<a name="Events"> </a>

Sie implementieren Transport-Agents, indem Sie sich zunächst für ein Ereignis registrieren und dann eine Aktion ausführen, wenn dieses Ereignis ausgelöst wird. Jeder der drei Agenttypen kann für eine andere Gruppe von Ereignissen registriert werden.
  
In der folgenden Abbildung wird gezeigt, wo sich Transport-Agents in Transport-Pipelines für Ereignisse registrieren können.
  
**Abbildung 1. Transport Ereignisse**

![Abbildung des Nachrichtenflusses durch die Transportpipeline und Ereignisse, für die sich jeder Agent registrieren kann beginnend mit Smtp-Ereignissen für den SmtpReceivedAgent, dann für Categorizor-Ereignisse für den RoutingAgent und schließlich für Übermittlungsereignisse für den DeliveryAgent.](media/TAConceptsFig1.png)
  
Wenn eine Nachricht in die Transportpipeline eingeht, kann ein Transport-Agent, der von der [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) -Klasse abgeleitet wurde, in der Nachricht während der SMTP-Ereignisse fungieren, für die der Agent registriert ist. Ein von der [Routing Agent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) -Klasse abgeleiteter Agent kann für jedes der vier Kategorisierungs Ereignisse fungieren, für die es registriert ist. Ein Agent, der von der [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.aspx) -Klasse abgeleitet wurde, kann während eines der Zustellungs Ereignisse, für die es registriert ist, auf eine Nachricht reagieren. 
  
## <a name="transport-agents-and-server-roles"></a>Transport-Agents und Serverrollen
<a name="ServerRoles"> </a>

Änderungen an der Architektur der Serverrolle in Exchange 2013 wirken sich auf Transport-Agents und ihre Aktionen für Transport-Agents aus. Exchange 2013 umfasst die folgenden Serverrollen:
  
- Postfachserver: enthält Client Zugriffsprotokolle, den Transport Dienst, Postfachdatenbanken und Unified Messaging-Komponenten. Der Postfachserver kommuniziert direkt mit Active Directory-Domänendienste (AD DS), Client Zugriffsservern und e-Mail-Clients wie Outlook.
    
- Clientzugriffsserver – Bereitstellung von Authentifizierung, begrenzten Umleitungen, Proxy Diensten und Clientzugriffsprotokollen wie http, Pop, IMAP und SMTP.
    
- Edge-Transport-Server – leitet e-Mails in eine und aus einer Organisation weiter. Edge-Transport-Server sitzen normalerweise am Umfang einer Exchange-Topologie.
    
Diese konsolidierte Struktur reduziert die Anzahl der Server, die in einer Exchange 2013 Umgebung bereitgestellt werden müssen. Administratoren müssen Hub-Transport-und Client Zugriffsserver nicht mehr an allen Active Directory-Standorten bereitstellen, die einen Postfachserver enthalten, und Sie müssen nicht mehr alle Serverrollen aktualisieren, um die Vorteile der neuen Funktionalität nutzen zu können.
  
Diese Änderungen an der Serverrollen Architektur können sich möglicherweise darauf auswirken, wo in der Pipeline Ihr Agent auf Ereignisse reagieren kann. Wenn Sie Transport-Agents für Exchange-Versionen vor Exchange 2013 erstellt haben, müssen Sie unbedingt die architektonischen Änderungen überprüfen, um zu bestimmen, ob Sie an Ihren Agents Änderungen vornehmen müssen.
  
In der folgenden Abbildung wird gezeigt, wie die architektonischen Änderungen in Exchange 2013 zu einer optimierten, konsolidierten Transportpipeline führen. In dieser Abbildung werden Client Zugriffsserver mit der Bezeichnung CAS bezeichnet. Und Postfachserver mit der Bezeichnung mbx.
  
**Abbildung 2. Exchange 2013 Serverrollen Architektur**

![Abbildung des Clientdatenverkehrs durch eine externe Firewall und den Edge-Transport-Server auf der linken Seite, der Datenverkehr über einen Lastenausgleich der Ebene 4 an ein konsolidiertes Clientzugriffsserver-Array und eine Gruppe von Postfachservern in einer Database Availability Group auf der rechten Seite übergibt.](media/Transport_Agent_Concepts_Fig_3.png)
  
In der folgenden Abbildung sind die Interaktionen zwischen den Exchange 2013-Serverrollen dargestellt.
  
**Abbildung 3. Interaktion mit dem Postfach und dem Client Zugriffsserver**

![Abbildung von Interaktionen beginnen mit Pfeilen vom Clientdatenverkehr, der einen Lastenausgleich der Ebene 4 durchläuft, der 4 Ziele auf dem Clientzugriffsserver hat: IIS/HTTP Proxy, POP/IMAP, SMTP und UM. Die Pfeile werden an ihre dazugehörigen Ziele im Postfachspeicher übergeben.](media/Transport_Agent_Concepts_Fig_4.png)
  
Weitere Informationen zu Änderungen an der Architektur der Exchange 2013 Serverrolle finden Sie unter [Exchange 2013 Architecture](https://technet.microsoft.com/library/jj150540%28v=exchg.150%29.aspx#BKMK_Arch) in [What es New in Exchange 2013](https://technet.microsoft.com/library/jj150540%28v=exchg.150%29.aspx). 
  
## <a name="transport-agent-classes"></a>Transport-Agent-Klassen
<a name="Create"> </a>

Die von Ihrem Transport-Agent abgeleitete Klasse bestimmt die Ereignisse, für die sich Ihr Agent registrieren kann. Ihr Agent enthält normalerweise eine Agent-Klasse, eine Agent-Factory, einen oder mehrere Ereignishandler und den Code, der die Aktionen ausführt, die der Agent ausführen soll.
  
In der folgenden Tabelle sind die Klassen aufgeführt, aus denen die einzelnen Agenttypen abgeleitet werden sollen.
  
**Tabelle 2. Agent-Klassen**

||||
|:-----|:-----|:-----|
|Agent-Typ  <br/> |Factory-Basisklasse  <br/> |Agent-Basisklasse  <br/> |
|SMTP-Empfang  <br/> |[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) <br/> |[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) <br/> |
|Routing  <br/> |[RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) <br/> |[Routing Agent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) <br/> |
|Übermittlung  <br/> |[DeliveryAgentFactory\<Manager\>](https://msdn.microsoft.com/library/dd877550(v=exchg.150).aspx) <br/> |[DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) <br/> |
   
Diese Factory-und Agent-Basisklassen stellen Eigenschaften und Methoden bereit, die Sie für den Zugriff auf Transportereignisse und-Nachrichten verwenden können. Implementieren Sie Klassen in Ihrem Agent, die von diesen Klassen erben. Überschreiben Sie in der von Agent Factory abgeleiteten Klasse die **createagent** -Methode, sodass eine neue Instanz Ihrer Agent-Klasse zurückgegeben wird. 
  
An die Ereignisse übergebene Argumente können eine Instanz der [Email Message](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Email.EmailMessage.aspx) -Klasse enthalten, die Sie verwenden können, um die Eigenschaften und den Inhalt der zugrunde liegenden Nachricht zu ändern. Nicht alle Nachrichten Informationen sind in jedem Ereignis verfügbar. Sie müssen bestimmen, welcher Agent und welches Ereignis am besten für die Aufgabe geeignet ist, die Sie ausführen möchten. 
  
Die folgenden Namespaces enthalten Typen, die Sie zum Lesen, schreiben und Ändern von Nachrichten in der Transportpipeline verwenden können:
  
- [Microsoft. Exchange. Data. MIME. Encoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.aspx)
    
- [Microsoft. Exchange. Data. ContentTypes. iCalendar](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.aspx)
    
- [Microsoft. Exchange. Data. MIME](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.aspx)
    
- [Microsoft. Exchange. Data. ContentTypes. TNEF](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.aspx)
    
- [Microsoft. Exchange. Data. ContentTypes. vCard](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.vCard.aspx)
    
Nachdem Sie Ihren Transport-Agent geschrieben haben, [Installieren und verwalten](https://technet.microsoft.com/library/bb125175%28v=exchg.150%29.aspx) Sie den Agent mithilfe der Exchange-Verwaltungsshell. Weitere Informationen finden Sie unter [Creating Transport Agents for Exchange 2013](creating-transport-agents-for-exchange-2013.md). 
  
## <a name="see-also"></a>Siehe auch

- [Transport-Agents in Exchange](transport-agents-in-exchange-2013.md)    
- [Transport-Agent-Referenz für Exchange 2013](transport-agent-reference-for-exchange-2013.md)   
- [Lesen und Ändern von Nachrichten in der Exchange 2013 Transportpipeline](reading-and-modifying-messages-in-the-exchange-2013-transport-pipeline.md)    
- [Neuerungen in Exchange 2013](https://technet.microsoft.com/library/jj150540%28v=exchg.150%29.aspx)   
- [Exchange 2013 Server Rollen Architektur](https://blogs.technet.com/b/exchange/archive/2013/01/23/exchange-2013-server-role-architecture.aspx)    
- [Postfach-und Client Zugriffsserver](https://technet.microsoft.com/library/jj150519%28v=exchg.150%29.aspx)   
- [Exchange Server 2013 Nachrichtenfluss](https://technet.microsoft.com/library/aa996349.aspx)
- [Exchange Server 2013 e-Mail-Routing](https://technet.microsoft.com/library/aa998825%28v=exchg.150%29.aspx)   
- [Exchange Server-PowerShell (Exchange-Verwaltungsshell)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)
    

