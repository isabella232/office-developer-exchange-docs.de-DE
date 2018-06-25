---
title: Transport-Agent-Namespaces in Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5c40788e-c182-4502-9202-206e6aaa53f8
description: Informationen Sie zu den .NET Framework-Klassen und Member, die Sie zum Erstellen von benutzerdefinierten Transport-Agents für Exchange 2013 verwenden können.
ms.openlocfilehash: a8189ca9915312b64fefda3091f8f81e51271ad6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757204"
---
# <a name="transport-agent-namespaces-in-exchange-2013"></a>Transport-Agent-Namespaces in Exchange 2013

Informationen Sie zu den .NET Framework-Klassen und Member, die Sie zum Erstellen von benutzerdefinierten Transport-Agents für Exchange 2013 verwenden können.
  
**Gilt für:** Exchange Server 2013 
  
Dieser Artikel enthält Informationen zu den Namespaces, die Informationen enthalten, die Sie zum Erstellen von Transport-Agents für Exchange Server 2013 verwenden können. Außerdem werden die Klassen, mit denen Transport-Agents können lesen und Ändern von e-Mail-Nachrichten, die über die Transportpipeline übergeben beschrieben.
  
## <a name="transport-agent-class-library"></a>Transport-Agent-Klassenbibliothek

Die folgenden Namespaces enthalten Typen, die Sie zum Erstellen und Erweitern von Transport-Agents verwenden können.

**In Tabelle 1. .NET Framework-namespaces**

|**Namespace**|**Beschreibung**|
|:-----|:-----|
|[Microsoft.Exchange.Data](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.aspx) <br/> |Enthält Typen, die Daten und Konfigurationsinformationen Ausnahmen angeben.  <br/> |
|[Microsoft.Exchange.Data.Common](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Common.aspx) <br/> |Enthält Typen, die Lokalisierung und Fehlerbehandlung zu unterstützen.  <br/> |
|[Microsoft.Exchange.Data.ContentTypes.iCalendar](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.aspx) <br/> |Enthält Typen, mit denen Sie iCalendar-Daten gelesen und geschrieben.  <br/> |
|[Microsoft.Exchange.Data.ContentTypes.Tnef](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.aspx) <br/> |Enthält Typen, mit denen Sie zum Lesen und Schreiben von TNEF-Daten.  <br/> |
|[Microsoft.Exchange.Data.ContentTypes.vCard](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.vCard.aspx) <br/> |Enthält Typen, mit denen Sie das Lesen und Schreiben von vCard-Daten.  <br/> |
|[Microsoft.Exchange.Data.Globalization](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Globalization.aspx) <br/> |Enthält Typen, mit denen Sie arbeiten mit Kulturen und Zeichensätze um lokalisierten Inhalte zu erstellen.  <br/> |
|[Microsoft.Exchange.Data.Mime](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.aspx) <br/> |Enthält Typen, mit denen Sie das Lesen und Schreiben von MIME-Daten.  <br/> |
|[Microsoft.Exchange.Data.Mime.Encoders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.aspx) <br/> |Enthält Typen, mit denen Sie zum Codieren und Decodieren MIME-Daten.  <br/> |
|[Microsoft.Exchange.Data.TextConverters](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.aspx) <br/> |Enthält Typen, mit denen Sie zum Lesen und Schreiben von Daten mit unterschiedlichen Textformaten und Daten zu und von diese Formate konvertieren.  <br/> |
|[Microsoft.Exchange.Data.Transport](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.aspx) <br/> |Enthält Typen, mit die Sie routing, Host und Informationen über die Transportpipeline Domäne zugreifen können.  <br/> |
|[Microsoft.Exchange.Data.Transport.Delivery](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.aspx) <br/> |Enthält Typen, die die Erweiterung von Exchange 2013 zustellungs-Agents zu unterstützen.  <br/> |
|[Microsoft.Exchange.Data.Transport.Email](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Email.aspx) <br/> |Enthält Typen, die erstellen, lesen, schreiben und Ändern von e-Mail-Nachrichten unterstützen.  <br/> |
|[Microsoft.Exchange.Data.Transport.Routing](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.aspx) <br/> |Enthält Typen, die die Erweiterung für das Exchange 2013 Transport Routingverhalten unterstützen.  <br/> |
|[Microsoft.Exchange.Data.Transport.Smtp](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.aspx) <br/> |Enthält Typen, die die Erweiterung des Exchange 2013 Transports SMTP-Verhalten zu unterstützen.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Transport-Agents in Exchange](transport-agents-in-exchange-2013.md)   
- [Transport-Agent Konzepte in Exchange 2013](transport-agent-concepts-in-exchange-2013.md) 
- [Für Exchange Server-API-Referenz](http://msdn.microsoft.com/library/6eddd052-f59f-45b4-b846-7e53d4d7eb16%28Office.15%29.aspx)
- [Agents Datei Konfigurationselemente für Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)
    

