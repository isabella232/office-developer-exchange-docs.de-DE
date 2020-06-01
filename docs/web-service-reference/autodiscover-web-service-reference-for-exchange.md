---
title: AutoErmittlung Webdienstverweis für Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a01124a8-a8cf-4b80-8625-d7ee05690bca
description: Hier finden Sie Referenzinhalte für den AutoErmittlungsdienst in Exchange.
ms.openlocfilehash: ce7f2bbd662a5e61959c7e3c6748f0cf40cc4fb3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466871"
---
# <a name="autodiscover-web-service-reference-for-exchange"></a>AutoErmittlung Webdienstverweis für Exchange

Hier finden Sie Referenzinhalte für den AutoErmittlungsdienst in Exchange.
  
Der AutoErmittlungsdienst stellt die Konfigurationsinformationen bereit, die Ihre Anwendung zum Erstellen einer Verbindung mit einem Exchange-Server verwendet. Sie können eine der folgenden Optionen verwenden, um eine Verbindung mit der AutoErmittlung herzustellen:
  
- SOAP-AutoErmittlungsdienst – verfügbar für Clients, die mit Exchange 2010, einschließlich Exchange Online, eine Verbindung mit Exchange-Versionen herstellen.
    
- "Plain Old XML" (POX) AutoErmittlungsdienst – verfügbar für Clients, die eine Verbindung mit Exchange-Versionen herstellen, beginnend mit Exchange 2007, einschließlich Exchange Online. 
    
Sowohl der SOAP-als auch der POX-AutoErmittlungsdienst können die Konfigurationsinformationen bereitstellen, die vom Client zum Erstellen einer Verbindung mit einem Exchange-Server verwendet werden.
  
> [!NOTE]
> Für Exchange-Versionen, die mit Exchange 2010 beginnen, wird empfohlen, den SOAP-AutoErmittlungsdienst anstelle des POX-AutoErmittlungsdiensts zu verwenden. Der SOAP-AutoErmittlungsdienst bietet Batched AutoErmittlungs-Einstellungsanforderungen und eine präzisere Kontrolle darüber, welche Einstellungen in der Antwort zurückgegeben werden. 
  
Dieser Abschnitt enthält Referenzinformationen für den SOAP-AutoErmittlungsdienst und den POX-AutoErmittlungsdienst.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_InThisSection"> </a>

- [Referenz zum SOAP-AutoErmittlungwebdienst für Exchange](soap-autodiscover-web-service-reference-for-exchange.md)
    
- [Referenz zum POX-AutoErmittlungwebdienst für Exchange](pox-autodiscover-web-service-reference-for-exchange.md)
    
## <a name="see-also"></a>Siehe auch

- [Webdienstreferenz für Exchange](web-services-reference-for-exchange.md)
- [AutoErmittlungsdienst (SOAP)](https://msdn.microsoft.com/library/e24d1a1f-0d20-4bd9-ae4c-9112ecacea78%28Office.15%29.aspx)
- [AutoErmittlungsdienst (POX)](https://msdn.microsoft.com/library/13c54de3-a91c-4424-8732-99dd8f2162ec%28Office.15%29.aspx)
    

