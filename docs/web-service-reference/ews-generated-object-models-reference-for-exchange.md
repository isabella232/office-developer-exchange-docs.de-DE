---
title: Für Exchange-Webdienste genierte Objektmodelle
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 67d7d831-9c53-46da-80e4-18f562e71284
description: Wenn Sie die für Exchange-Webdienste generierte Objektmodellreferenz für die Entwicklung von Anwendungen für Exchange verwenden, informieren Sie sich über weitere Optionen für die Entwicklung für Exchange-Webdienste.
ms.openlocfilehash: 6c97ca7973da84d96d102287b9c260409a0f57ef
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541434"
---
# <a name="ews-generated-object-models-for-exchange"></a>Für Exchange-Webdienste genierte Objektmodelle für Exchange

**Gilt für**: Exchange Online | Exchange Server 2013 | Office 365

Das für Exchange-Webdienste von wsdl.exe generierte Objektmodell stellte ursprünglich ein einfaches Objektmodell für die Verwendung mit Exchange 2007 bereit. Als die von Exchange-Webdiensten verwaltete API verfügbar wurde, brachte Sie einige Vorteile für Entwickler mit sich, die mit verwaltetem Code arbeiten. 

Die von Exchange-Webdiensten verwaltete API:

- Bietet ein intuitives Objektmodell

- Enthält clientseitige Geschäftslogik und Datenvalidierung

- Wird vollständig unterstützt und wird regelmäßig aktualisiert

- Enthält einen AutoErmittlung-Client.

- Implementiert Clientfunktionen wie Protokollierung, Cookieverwaltung und Diagnoseberichte zu Exchange

Die wsdl.exe-basierte, von Exchange-Webdiensten verwaltete Referenzdokumentation ist veraltet, da die von Exchange-Webdiensten verwaltete API die meisten Funktionen ersetzt, die von generierten Objektmodellen bereitgestellt wurden. Gleichzeitig wissen wir, dass die von Exchange-Webdiensten verwaltete API nicht für alle geeignet ist. In den meisten Fällen ist dies die beste Möglichkeit zum Erstellen von Exchange-Webdienstclients für .NET, es gibt jedoch einige Ausnahmen; Zum Beispiel:

- Wenn Funktionen, die Sie verwenden möchten, [nicht in der von Exchange-Webdiensten verwalteten API nicht implementiert sind](../exchange-web-services/web-service-api-feature-availability-in-exchange-and-the-ews-managed-api.md#bk_apifeatures).

- Wenn Sie eine andere Entwicklungsplattform als .NET verwenden.

Wenn Sie die von Exchange-Webdiensten verwaltete API nicht zum Entwickeln Ihrer Anwendung verwenden können, können Sie stattdessen Folgendes:

- Eine Exchange-Webdienstclient-API eines Drittanbieters verwenden.

- Ein eigenes Exchange-Webdienst-Clientobjektmodell erstellen.

- Einen Objektmodellgenerator verwenden. Erwartungsgemäß finden Sie Objektmodellgeneratoren für die meisten gängigen Plattformen und Sprachen.

Wenn Sie einen Objektmodellgenerator verwenden möchten, können Sie die XML-Referenz verwenden, um sich über die Grundlagen des generierten Objektmodells zu informieren. Das Objektmodell wird aus XML-Strukturen generiert, die im Schema beschrieben sind. In der Regel werden die von Objektmodellgeneratoren erstellten Klassen mit den komplexen Typen im Schema verknüpft. Eigenschaften werden in der Regel mit den XML-Elemente verknüpft.

Lesen Sie [ExchangeWebServices-Namespace](https://docs.microsoft.com/dotnet/api/exchangewebservices?view=exchange-ews-proxy).

## <a name="see-also"></a>Siehe auch

- [Webdienstreferenz für Exchange](web-services-reference-for-exchange.md)
- [Erkunden von verwalteter EWS-API, EWS und Webdiensten in Exchange](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)
- [Neuerungen in EWS und anderen Webdiensten in Exchange](../exchange-web-services/whats-new-in-ews-and-other-web-services-in-exchange.md)
