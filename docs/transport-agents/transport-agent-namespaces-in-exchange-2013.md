---
title: Transport-Agent-Namespaces in Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 5c40788e-c182-4502-9202-206e6aaa53f8
description: Erfahren Sie mehr über die .NET Framework Klassen und Member, mit denen Sie benutzerdefinierte Transport-Agents für Exchange 2013 erstellen können.
ms.openlocfilehash: 076ddb8e2ccbdfa195a68aca6b296337a2876b55
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59537130"
---
# <a name="transport-agent-namespaces-in-exchange-2013"></a>Transport-Agent-Namespaces in Exchange 2013

Erfahren Sie mehr über die .NET Framework Klassen und Member, mit denen Sie benutzerdefinierte Transport-Agents für Exchange 2013 erstellen können.
  
**Gilt für:** Exchange Server 2013 
  
Dieser Artikel enthält Informationen zu den Namespaces, die Referenzinformationen enthalten, die Sie zum Erstellen von Transport-Agents für Exchange Server 2013 verwenden können. Außerdem werden die Klassen beschrieben, die Ihre Transport-Agents verwenden können, um E-Mail-Nachrichten zu lesen und zu ändern, die die Transportpipeline durchlaufen.
  
## <a name="transport-agent-class-library"></a>Transport-Agent-Klassenbibliothek

Die folgenden Namespaces enthalten Typen, die Sie zum Erstellen und Erweitern von Transport-Agents verwenden können.

**Tabelle 1. .NET Framework Namespaces**

|**Namespace**|**Beschreibung**|
|:-----|:-----|
|[Microsoft. Exchange. Daten](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.aspx) <br/> |Enthält Typen, die Daten- und Konfigurations ausnahmen angeben.  <br/> |
|[Microsoft. Exchange.Data.Common](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Common.aspx) <br/> |Enthält Typen, die Lokalisierung und Fehlerbehandlung unterstützen.  <br/> |
|[Microsoft. Exchange. Data.ContentTypes.iCalendar](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.aspx) <br/> |Enthält Typen, mit denen Sie iCalendar-Daten lesen und schreiben können.  <br/> |
|[Microsoft. Exchange. Data.ContentTypes.Tnef](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.aspx) <br/> |Enthält Typen, mit denen Sie TNEF-Daten lesen und schreiben können.  <br/> |
|[Microsoft. Exchange. Data.ContentTypes.vCard](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.vCard.aspx) <br/> |Enthält Typen, mit denen Sie vCard-Daten lesen und schreiben können.  <br/> |
|[Microsoft. Exchange. Data.Globalization](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Globalization.aspx) <br/> |Enthält Typen, mit denen Sie mit Kulturen und Zeichensätzen arbeiten können, um lokalisierte Inhalte zu erzeugen.  <br/> |
|[Microsoft. Exchange. Data.Mime](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.aspx) <br/> |Enthält Typen, mit denen Sie MIME-Daten lesen und schreiben können.  <br/> |
|[Microsoft. Exchange. Data.Mime.Encoders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.aspx) <br/> |Enthält Typen, mit denen Sie MIME-Daten codieren und decodieren können.  <br/> |
|[Microsoft. Exchange. Data.TextConverters](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.aspx) <br/> |Enthält Typen, mit denen Sie Daten mit unterschiedlichen Textformaten lesen und schreiben und Daten in und aus diesen Formaten konvertieren können.  <br/> |
|[Microsoft. Exchange. Data.Transport](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.aspx) <br/> |Enthält Typen, mit denen Sie auf Routing-, Host- und Domäneninformationen zur Transportpipeline zugreifen können.  <br/> |
|[Microsoft. Exchange. Data.Transport.Delivery](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.aspx) <br/> |Enthält Typen, die die Erweiterung von Exchange 2013-Übermittlungs-Agents unterstützen.  <br/> |
|[Microsoft. Exchange. Data.Transport.Email](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Email.aspx) <br/> |Enthält Typen, die das Erstellen, Lesen, Schreiben und Ändern von E-Mail-Nachrichten unterstützen.  <br/> |
|[Microsoft. Exchange. Data.Transport.Routing](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.aspx) <br/> |Enthält Typen, die die Erweiterung des Transportroutingverhaltens Exchange 2013 unterstützen.  <br/> |
|[Microsoft. Exchange. Data.Transport.Smtp](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.aspx) <br/> |Enthält Typen, die die Erweiterung des smtp-Transportverhaltens Exchange 2013 unterstützen.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Transport-Agents in Exchange](transport-agents-in-exchange-2013.md)   
- [Transport-Agent-Konzepte in Exchange 2013](transport-agent-concepts-in-exchange-2013.md) 
- 
  [Server-API-Referenz für Exchange](https://msdn.microsoft.com/library/6eddd052-f59f-45b4-b846-7e53d4d7eb16%28Office.15%29.aspx)
- [Agents-Konfigurationsdateielemente für Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)
    

