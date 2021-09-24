---
title: Anforderungen für die Neuverteilung für die verwaltete EWS-API
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 8b206274-eaa4-40d3-b504-af27335c8f43
description: Erfahren Sie, wie Sie die assemblys der verwalteten EWS-API mit Ihrer Anwendung verteilen können.
ms.openlocfilehash: f43156838c735cfc17106deb7860329d3da6c07a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531330"
---
# <a name="redistribution-requirements-for-the-ews-managed-api"></a>Anforderungen für die Neuverteilung für die verwaltete EWS-API

Erfahren Sie, wie Sie die assemblys der verwalteten EWS-API mit Ihrer Anwendung verteilen können.
  
Beim Entwerfen Ihrer verwalteten EWS-API-Anwendung sollten Sie auch überlegen, wie Sie sie für Ihre Benutzer freigeben. 
  
## <a name="redistributing-your-ews-managed-api-application"></a>Verteilen Ihrer verwalteten EWS-API-Anwendung

Wenn sich die Anwendung nicht auf dem Exchange Server befindet, müssen Sie die Assemblys der verwalteten EWS-API weiterverteilen. Der Download der verwalteten EWS-API enthält zwei Assemblys, die Sie verteilen können: Microsoft.Exchange.WebServices.dll und Microsoft.Exchange.WebServices.Auth.dll. Beachten Sie beim Entwerfen der Veröffentlichung Ihrer verwalteten EWS-API-Anwendung die folgenden Informationen:
  
- Die verwaltete EWS-API wurde so konzipiert, dass Sie sie herunterladen und mit Ihrer Anwendung verteilen können, die auf einen Exchange Server ausgerichtet ist. Alternativ kann Ihre Anwendung die verwaltete EWS-API herunterladen.
    
- Sie können die verwaltete EWS-API verwenden, um mit einem Exchange Server zu kommunizieren, auf dem Exchange Online ausgeführt wird, Exchange Online als Teil Office 365 oder eine lokale Version von Exchange ab Exchange Server 2007.
    
- In Versionen der verwalteten EWS-API ab Version 2.1 können Sie die API im globalen Assemblycache (Global Assembly Cache, GAC) installieren. Die MSI-Datei fügt die DLL automatisch dem GAC hinzu und kann auf Computerbasis und nicht auf Benutzerbasis zugegriffen werden.
    
Die Lizenzbedingungen sind im Download der verwalteten EWS-API enthalten. Lesen Sie die Bedingungen für die autorisierenden Informationen dazu, was Sie mit der verwalteten EWS-API tun können.
  
## <a name="see-also"></a>Siehe auch


- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)
    
- [Verwaltete EWS-API (Download)](https://aka.ms/ews-managed-api-readme)
    

