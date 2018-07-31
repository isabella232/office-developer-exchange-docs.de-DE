---
title: Transport-Agent Konzepte in Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c700af8-2792-4d3f-8571-8860e0550d8e
description: Hier finden Sie Informationen darüber, wie die Transport-Agent Pipeline und Rolle Serverarchitektur in Exchange 2013 beeinflussen Transport-Agent-Entwicklung und die Klassen, die Sie verwenden können, um Transport-Agents zu entwickeln.
ms.openlocfilehash: 6f7a03e16b260117c6ee27b86ec0e55b5346e301
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353707"
---
# <a name="transport-agent-concepts-in-exchange-2013"></a>Transport-Agent Konzepte in Exchange 2013

Hier finden Sie Informationen darüber, wie die Transport-Agent Pipeline und Rolle Serverarchitektur in Exchange 2013 beeinflussen Transport-Agent-Entwicklung und die Klassen, die Sie verwenden können, um Transport-Agents zu entwickeln. 
  
**Gilt für:** Exchange Server 2013 
  
Sie können die Klassenbibliothek in Exchange Server 2013 bereitgestellter Transport-Agents zu implementieren, die registrieren für Ereignisse und Aktionen für Nachrichten, wenn sie über die Transportpipeline übergeben. Sie können auch Transport-Agents zum Ändern von Nachrichten und Konvertieren von Inhalten verwenden. 
  
Dieser Artikel enthält Informationen zu Transport-Agents und der Transport Pipeline-Architektur. Es ist wichtig, die Architektur von der Transportpipeline zu verstehen, damit Sie Transport Verhalten zum Erfüllen der Anforderungen Ihrer Organisation ändern können. Dieser Artikel enthält auch Informationen zu Änderungen in die Exchange 2013-Architektur, die Einfluss auf Transport-Agents und die Klassen, die Sie verwenden können, um Transport-Agents zu entwickeln. 
  
## <a name="transport-agents-in-the-transport-pipeline"></a>Transport-Agents in der Transportpipeline
<a name="Pipeline"> </a>

Transport-Agents werden von einer der folgenden drei Klassen abgeleitet werden:
  
- [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)
- [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)
- [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.aspx)
    
Die Transportpipeline bezieht sich auf den Ablauf des Meldungsdaten innerhalb der Grenzen der Exchange 2013-Organisation. Die Pipeline besteht in der folgenden Tabelle aufgeführten Dienste aus.
  
**In Tabelle 1. Pipeline-Transport-Dienste**

|**Dienst**|**Beschreibung**|**Unterstützte Klassen**|
|:-----|:-----|:-----|
|Front-End-Transport  <br/> |Führt auf allen [Clientzugriffsservern](http://technet.microsoft.com/en-us/library/dd298114%28v=exchg.150%29.aspx) und fungiert als statusfreie Proxy für alle eingehenden und ausgehenden externen SMTP-Datenverkehr für die Exchange 2013-Organisation. Der Front-End-Transport-Dienst nicht überprüfen Nachrichteninhalt oder lokal alle Nachrichten in die Warteschlange. Es kommuniziert mit dem Transportdienst auf einem [Postfachserver](http://technet.microsoft.com/en-us/library/jj150491%28v=exchg.150%29.aspx).  <br/> |[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) <br/> |
|Transport  <br/> |Führt auf allen Postfachservern und ähnelt dem [Hub-Transport-Server](http://technet.microsoft.com/en-us/library/bb123494%28v=exchg.141%29.aspx) -Role in Exchange Server 2010. Der Transportdienst leitet Nachrichten zwischen sich selbst und die Postfach-Transport und Front-End-Transport-Dienste. Dieser Dienst kommuniziert nicht direkt mit Postfachdatenbanken.  <br/> |[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) <br/> [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) <br/> [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.aspx) <br/> |
|Postfach-Transport  <br/> |Führt auf allen Postfachservern und besteht aus zwei separaten Diensten: Postfachtransportübermittlung und Postfach-Transport-Bereitstellung. Postfach Transport Übermittlung empfängt SMTP-Nachrichten von den Transportdienst und stellt eine Verbindung mit der Postfachdatenbank mithilfe einer Exchange-Remoteprozeduraufruf (RPC), um die Nachricht zu übermitteln. Postfachtransportübermittlung eine Verbindung mit der Postfachdatenbank mithilfe von RPC zum Abrufen von Nachrichten und sendet die Nachrichten über den SMTP-Transport-Dienst.  <br/> |Keine.  <br/> |
   
### <a name="transport-events"></a>Transport-Ereignisse
<a name="Events"> </a>

Implementieren Sie Transport-Agents, indem Sie zuerst registrieren für ein Ereignis, und klicken Sie dann eine Aktion durchzuführen, wenn das Ereignis ausgelöst wird. Jede der drei Agent kann für einen anderen Satz von Ereignissen registrieren.
  
Die folgende Abbildung zeigt, wo in der Transport Pipeline Transport, den Agents für die Ereignisse registrieren können.
  
**Abbildung 1. Transport-Ereignisse**

![Abbildung des Nachrichtenflusses durch die Transportpipeline und Ereignisse, für die sich jeder Agent registrieren kann beginnend mit Smtp-Ereignissen für den SmtpReceivedAgent, dann für Categorizor-Ereignisse für den RoutingAgent und schließlich für Übermittlungsereignisse für den DeliveryAgent.](media/TAConceptsFig1.png)
  
Wenn eine Meldung über die Transportpipeline eingibt, kann ein Transport-Agent, der von der [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) -Klasse abgeleitet während eines der SMTP-Ereignisse für die Nachricht fungieren, die für der Agent registriert. Ein Agent, der von der [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) -Klasse abgeleitet kann auf einen der vier Kategorisierungsmodul Ereignisse fungieren, die sie für registriert hat. Ein Agent, der von der [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.aspx) -Klasse abgeleitet kann auf eine Nachricht während eines der Übermittlung Ereignisse fungieren, die sie für registriert hat. 
  
## <a name="transport-agents-and-server-roles"></a>Transport-Agents und Serverrollen
<a name="ServerRoles"> </a>

Änderungen an die Server-Role-Architektur wirken sich auf Exchange 2013 Transport-Agents und was Transport-Agents möglich ist. Exchange 2013 umfasst die folgenden Serverrollen:
  
- Postfachserver – Protokolle Clientzugriff enthält, der Transportdienst, Postfachdatenbanken und Unified Messaging-Komponenten. Mailbox-Server kommuniziert direkt mit Active Directory-Domänendienste (AD DS), Clientzugriffs-Servern und e-Mail-Clients wie Outlook.
    
- Clientzugriffsserver – bietet Authentifizierung, beschränkt Umleitung, Proxy-Dienste und Protokolle für den Clientzugriff wie HTTP, POP, IMAP und SMTP.
    
- Edge-Transport-Server – leitet e-Mail-an- und wieder abmelden einer Organisation. Edge-Transport-Servern befinden sich in der Regel am Perimeter des Exchange-Topologie.
    
Diese Struktur konsolidierten verringert die Anzahl von Servern, die in einer Exchange 2013-Umgebung bereitgestellt werden müssen. Administratoren haben nicht mehr zum Bereitstellen von Hub-Transport- und Clientzugriffs-Servern an jedem Active Directory-Standort, der einen Postfachserver enthält, und sie nicht mehr benötigen, um alle Serverrollen zu aktualisieren, um neue Funktionen nutzen.
  
Diese Änderungen an die Server-Role-Architektur können beeinträchtigen, in dem in der Pipeline Agents auf Ereignisse reagieren kann. Wenn Sie Transport-Agents für Exchange-Versionen vor Exchange 2013 erstellt haben, müssen Sie überprüfen Sie die architekturänderungen, um zu bestimmen, ob Änderungen an der Agents vorgenommen werden müssen.
  
Die folgende Abbildung zeigt, wie die architektonischen Änderungen in Exchange 2013 in eine optimierte, konsolidierte Transportpipeline bewirken. In dieser Abbildung sind die Clientzugriffs-Servern CAS gekennzeichnet. Und Postfachservern werden MBX gekennzeichnet.
  
**Abbildung 2. Exchange 2013-Server-Role-Architektur**

![Abbildung des Clientdatenverkehrs durch eine externe Firewall und den Edge-Transport-Server auf der linken Seite, der Datenverkehr über einen Lastenausgleich der Ebene 4 an ein konsolidiertes Clientzugriffsserver-Array und eine Gruppe von Postfachservern in einer Database Availability Group auf der rechten Seite übergibt.](media/Transport_Agent_Concepts_Fig_3.png)
  
Die folgende Abbildung zeigt die Interaktionen zwischen den Exchange 2013-Serverrollen.
  
**Abbildung 3. Postfach- und Clientzugriffs-Server-Aktivitäten**

![Abbildung von Interaktionen beginnen mit Pfeilen vom Clientdatenverkehr, der einen Lastenausgleich der Ebene 4 durchläuft, der 4 Ziele auf dem Clientzugriffsserver hat: IIS/HTTP Proxy, POP/IMAP, SMTP und UM. Die Pfeile werden an ihre dazugehörigen Ziele im Postfachspeicher übergeben.](media/Transport_Agent_Concepts_Fig_4.png)
  
Weitere Informationen zu Änderungen in der Exchange 2013-Server-Role-Architektur finden Sie unter [Architektur von Exchange 2013](http://technet.microsoft.com/en-us/library/jj150540%28v=exchg.150%29.aspx#BKMK_Arch) unter [What's New in Exchange 2013](http://technet.microsoft.com/en-us/library/jj150540%28v=exchg.150%29.aspx). 
  
## <a name="transport-agent-classes"></a>Transport-Agent-Klassen
<a name="Create"> </a>

Die Klasse, der Ihre Transport-Agent abgeleitet bestimmt die Ereignisse, die für die Agents registrieren kann. Agents in der Regel enthält ein Agent-Klasse, ein Agentfactory, einen oder mehrere Ereignishandler und den Code, der die Aktionen, die Sie den Agent ausführt übernehmen möchten.
  
Die folgende Tabelle enthält die Klassen, von denen für jeden Agent abgeleitet werden.
  
**In Tabelle 2. Agent-Klassen**

||||
|:-----|:-----|:-----|
|Agenttyp  <br/> |Factory-Basisklasse  <br/> |Agent-Basisklasse  <br/> |
|SMTP-Empfang  <br/> |[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) <br/> |[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) <br/> |
|Routing  <br/> |[RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) <br/> |[RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) <br/> |
|Übermittlung  <br/> |[DeliveryAgentFactory\<Manager\>](https://msdn.microsoft.com/en-us/library/dd877550(v=exchg.150).aspx) <br/> |[DeliveryAgent](https://msdn.microsoft.com/en-us/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) <br/> |
   
Diese Factory und Agent Basisklassen stellen Eigenschaften und Methoden, mit denen Sie Zugriff auf Transport-Ereignisse und Nachrichten. Implementieren Sie Klassen in der Agents, die von diesen Klassen erben. Überschreiben Sie die **Hilfe von CreateAgent** -Methode in der Agent-Klasse abgeleitet Zuordnungsinstanz, damit eine neue Instanz des Agent-Klasse zurückgegeben. 
  
Argumente an die Ereignisse übergeben können es sich um eine Instanz der Klasse ["EmailMessage"](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Email.EmailMessage.aspx) enthalten, die Sie verwenden können, um die Eigenschaften und den Inhalt der zugrunde liegenden Nachricht zu ändern. Nicht alle Nachrichteninformationen ist in jedem Ereignis verfügbar. Sie müssen ermitteln, welche Agent und welche Ereignis ist am besten für die Aufgabe, die Sie ausführen möchten. 
  
Die folgenden Namespaces enthalten Typen, die Sie verwenden können, lesen, schreiben und Nachrichten in der Transportpipeline zu ändern:
  
- [Microsoft.Exchange.Data.Mime.Encoders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.aspx)
    
- [Microsoft.Exchange.Data.ContentTypes.iCalendar](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.aspx)
    
- [Microsoft.Exchange.Data.Mime](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.aspx)
    
- [Microsoft.Exchange.Data.ContentTypes.Tnef](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.aspx)
    
- [Microsoft.Exchange.Data.ContentTypes.vCard](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.vCard.aspx)
    
Nachdem Sie Ihre Transport-Agent, Sie [Installieren und Verwalten von Agents](http://technet.microsoft.com/en-us/library/bb125175%28v=exchg.150%29.aspx) mithilfe der Exchange-Verwaltungsshell geschrieben. Weitere Informationen finden Sie unter [Creating Transport-Agents für Exchange 2013](creating-transport-agents-for-exchange-2013.md). 
  
## <a name="see-also"></a>Siehe auch

- [Transport-Agents in Exchange](transport-agents-in-exchange-2013.md)    
- [Transport-Agent-Referenz für Exchange 2013](transport-agent-reference-for-exchange-2013.md)   
- [Lesen und Ändern von Nachrichten in der Transportpipeline Exchange 2013](reading-and-modifying-messages-in-the-exchange-2013-transport-pipeline.md)    
- [Was ist neu in Exchange 2013](http://technet.microsoft.com/en-us/library/jj150540%28v=exchg.150%29.aspx)   
- [Exchange 2013-Server-Role-Architektur](http://blogs.technet.com/b/exchange/archive/2013/01/23/exchange-2013-server-role-architecture.aspx)    
- [Postfach- und Clientzugriffsservern](http://technet.microsoft.com/en-us/library/jj150519%28v=exchg.150%29.aspx)   
- [Exchange Server 2013-Nachrichtenübermittlung](http://technet.microsoft.com/en-us/library/aa996349.aspx)
- [Exchange Server 2013 E-Mail-Routing](http://technet.microsoft.com/en-us/library/aa998825%28v=exchg.150%29.aspx)   
- [Exchange Server-PowerShell (Exchange-Verwaltungsshell)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)
    

