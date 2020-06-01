---
title: Referenz zur verwalteten API der Exchange-Webdienste (Exchange Web Services, EWS)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
api_type:
- schema
ms.assetid: c6ca36f4-a67c-4e3c-aae7-9ead7b704e15
description: Erfahren Sie mehr über die Namespaces, die in der verwaltete EWS-API enthalten sind.
localization_priority: Priority
ms.openlocfilehash: aa5dd71bf1e9962611a8ea8471aca0c60aa232e8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466752"
---
# <a name="ews-managed-api-reference"></a>Referenz zur verwalteten EWS-API

**Bezieht sich auf**: verwaltete EWS-API | Exchange Online | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013 | Office 365

Die verwaltete API der Exchange-Webdienste (EWS) umfasst zwei APIs: Microsoft.Exchange.WebServices.dll und Microsoft.Exchange.WebServices.Auth.dll.

## <a name="ews-managed-api-namespaces"></a>Namespaces der verwalteten EWS-API

|Namespace |Beschreibung |
|:---------|:-----------|
|[Microsoft.Exchange.WebServices.Auth.Validation](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.auth.validation?view=exchange-ews-api) |Enthält Typen und Methoden, die verwendet werden, um Benutzeridentitätstoken zu überprüfen, die von einem Exchange-Server gesendet wurden. Der Namespace „Microsoft.Exchange.WebServices.Auth.Validation“ gilt für Clients, die für Exchange Online und Versionen von Exchange ab Exchange Server 2013 bestimmt sind. Dieser Namespace ist in der Microsoft.Exchange.WebServices.Auth.dll-API enthalten.|
|[Microsoft.Exchange.WebServices.Autodiscover](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.autodiscover?view=exchange-ews-api)|Enthält Typen, die zur Kommunikation mit dem AutoErmittlungsdienst verwendet werden, der von einem Exchange-Server gehostet wird. Dieser Namespace dient auch der Suche nach Dienstverbindungspunkten in Active Directory Domain Services (AD DS). Die AutoErmittlungsdienste stellen Konfigurationsinformationen für EWS-Clients bereit. Dadurch können die Clients die entsprechende Dienst-URL als Ziel anpeilen.<br/><br/>Die Namespace-Funktionalität kann verwendet werden, um den POX-AutoErmittlungsdienst als Ziel anzupeilen, der in Microsoft Exchange Server 2007 eingeführt wurde, die Dienstverbindungspunkt-Objektsuche (wenn der Client Teil der Domäne ist) oder den SOAP-AutoErmittlungsendpunkt, der in Exchange Server 2010 eingeführt wurde. Der wichtigste Typ in diesem Namespace ist die [AutodiscoverService-Klasse](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.autodiscover.autodiscoverservice?view=exchange-ews-api). Dieser Namespace ist in der Microsoft.Exchange.WebServices.dll-API enthalten.|
|[Microsoft.Exchange.WebServices.Data](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.data?view=exchange-ews-api)| Enthält Typen, die für die Kommunikation mit einem Exchange-Server über EWS verwendet werden. Dieser Namespace stellt die wichtigsten Funktionen der verwalteten EWS-API bereit. Der wichtigste Typ in diesem Namespace ist die [ExchangeService-Klasse](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.data.exchangeservice?view=exchange-ews-api).|

## <a name="see-also"></a>Siehe auch

- [Webdienstreferenz für Exchange](web-services-reference-for-exchange.md)
- [Erkunden von verwalteter EWS-API, EWS und Webdiensten in Exchange](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)
- [Neuerungen in EWS und anderen Webdiensten in Exchange](../exchange-web-services/whats-new-in-ews-and-other-web-services-in-exchange.md)
- [Erste Schritte mit Webdiensten in Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
- [Entwickeln von Webdienstclients für Exchange](../exchange-web-services/develop-web-service-clients-for-exchange.md)

