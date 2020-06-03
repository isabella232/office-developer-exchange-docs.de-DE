---
title: Namespaces des Transport-Agents in Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5c40788e-c182-4502-9202-206e6aaa53f8
description: Erfahren Sie mehr über die .NET Framework Klassen und Member, die Sie zum Erstellen von benutzerdefinierten Transport-Agents für Exchange 2013 verwenden können.
ms.openlocfilehash: fc2d9108c910a730bb48c5be028797f0f15ad4ad
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461793"
---
# <a name="transport-agent-namespaces-in-exchange-2013"></a>Namespaces des Transport-Agents in Exchange 2013

Erfahren Sie mehr über die .NET Framework Klassen und Member, die Sie zum Erstellen von benutzerdefinierten Transport-Agents für Exchange 2013 verwenden können.
  
**Gilt für:** Exchange Server 2013 
  
Dieser Artikel enthält Informationen zu den Namespaces, die Referenzinformationen enthalten, die Sie zum Erstellen von Transport-Agents für Exchange Server 2013 verwenden können. Außerdem werden die Klassen beschrieben, die Ihre Transport-Agents zum Lesen und Ändern von e-Mail-Nachrichten verwenden können, die die Transportpipeline passieren.
  
## <a name="transport-agent-class-library"></a>Transport-Agent-Klassenbibliothek

Die folgenden Namespaces enthalten Typen, die Sie zum Erstellen und Erweitern von Transport-Agents verwenden können.

**Tabelle 1. .NET Framework Namespaces**

|**Namespace**|**Beschreibung**|
|:-----|:-----|
|[Microsoft. Exchange. Data](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.aspx) <br/> |Enthält Typen, die Daten-und Konfigurations Ausnahmen angeben.  <br/> |
|[Microsoft. Exchange. Data. Common](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Common.aspx) <br/> |Enthält Typen, die die Lokalisierung und Fehlerbehandlung unterstützen.  <br/> |
|[Microsoft. Exchange. Data. ContentTypes. iCalendar](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.aspx) <br/> |Enthält Typen, mit denen Sie iCalendar-Daten lesen und schreiben können.  <br/> |
|[Microsoft. Exchange. Data. ContentTypes. TNEF](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.aspx) <br/> |Enthält Typen, mit denen Sie TNEF-Daten lesen und schreiben können.  <br/> |
|[Microsoft. Exchange. Data. ContentTypes. vCard](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.vCard.aspx) <br/> |Enthält Typen, mit denen Sie vCard-Daten lesen und schreiben können.  <br/> |
|[Microsoft. Exchange. Data. Globalization](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Globalization.aspx) <br/> |Enthält Typen, mit denen Sie mit Kulturen und Zeichensätzen zusammenarbeiten können, um lokalisierte Inhalte zu erstellen.  <br/> |
|[Microsoft. Exchange. Data. MIME](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.aspx) <br/> |Enthält Typen, mit denen Sie MIME-Daten lesen und schreiben können.  <br/> |
|[Microsoft. Exchange. Data. MIME. Encoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.aspx) <br/> |Enthält Typen, mit denen Sie MIME-Daten codieren und decodieren können.  <br/> |
|[Microsoft. Exchange. Data. TextConverters](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.aspx) <br/> |Enthält Typen, mit denen Sie Daten mit unterschiedlichen Textformaten lesen und schreiben und Daten in und aus diesen Formaten konvertieren können.  <br/> |
|[Microsoft. Exchange. Data. Transport](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.aspx) <br/> |Enthält Typen, mit denen Sie auf Routing-, Host-und Domäneninformationen zur Transportpipeline zugreifen können.  <br/> |
|[Microsoft. Exchange. Data. Transport. Delivery](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.aspx) <br/> |Enthält Typen, die die Erweiterung von Exchange 2013 Zustellungs-Agents unterstützen.  <br/> |
|[Microsoft. Exchange. Data. Transport. e-Mail](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Email.aspx) <br/> |Enthält Typen, die das Erstellen, lesen, schreiben und Ändern von e-Mail-Nachrichten unterstützen.  <br/> |
|[Microsoft. Exchange. Data. Transport. Routing](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.aspx) <br/> |Enthält Typen, die die Erweiterung des Exchange 2013 Transport Routingverhaltens unterstützen.  <br/> |
|[Microsoft. Exchange. Data. Transport. SMTP](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.aspx) <br/> |Enthält Typen, die die Erweiterung des SMTP-Verhaltens von Exchange 2013 Transport unterstützen.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Transport-Agents in Exchange](transport-agents-in-exchange-2013.md)   
- [Transport-Agent-Konzepte in Exchange 2013](transport-agent-concepts-in-exchange-2013.md) 
- 
  [Server-API-Referenz für Exchange](https://msdn.microsoft.com/library/6eddd052-f59f-45b4-b846-7e53d4d7eb16%28Office.15%29.aspx)
- [Elemente der Konfigurationsdatei der Agents für Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)
    

