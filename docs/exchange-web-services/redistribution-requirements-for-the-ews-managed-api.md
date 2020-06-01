---
title: Redistribution Anforderungen für die EWS Managed API
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8b206274-eaa4-40d3-b504-af27335c8f43
description: Erfahren Sie, wie Sie die verwaltete EWS-API-Assemblys mit Ihrer Anwendung neu verteilen können.
ms.openlocfilehash: e64b4cdb8938caa819ba30621112a25946ef0424
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463825"
---
# <a name="redistribution-requirements-for-the-ews-managed-api"></a>Redistribution Anforderungen für die EWS Managed API

Erfahren Sie, wie Sie die verwaltete EWS-API-Assemblys mit Ihrer Anwendung neu verteilen können.
  
Wenn Sie Ihre verwaltete EWS-API-Anwendung entwerfen, sollten Sie auch prüfen, wie Sie Sie für Ihre Benutzer freigeben werden. 
  
## <a name="redistributing-your-ews-managed-api-application"></a>Neuverteilen ihrer verwaltete EWS-API Anwendung

Wenn sich Ihre Anwendung nicht auf dem Exchange-Server befindet, müssen Sie die verwaltete EWS-API-Assemblys erneut verteilen. Der verwaltete EWS-API Download enthält zwei Assemblys, die Sie erneut verteilen können: Microsoft. Exchange. Webservices. dll und Microsoft. Exchange. Webservices. auth. dll. Beachten Sie beim Entwerfen der Veröffentlichung ihrer verwaltete EWS-API Anwendung die folgenden Informationen:
  
- Die verwaltete EWS-API wurde so konzipiert, dass Sie Sie herunterladen und mit Ihrer Anwendung, die auf einen Exchange-Server zielt, verteilen können. Alternativ kann Ihre Anwendung die verwaltete EWS-API herunterladen.
    
- Sie können die verwaltete EWS-API verwenden, um mit einem Exchange-Server zu kommunizieren, der Exchange Online ausführt, Exchange Online als Teil Office 365 oder einer lokalen Exchange-Version, die mit Exchange Server 2007 beginnt.
    
- In Versionen der verwaltete EWS-API ab Version 2,1 können Sie die API im globalen Assemblycache (GAC) installieren. Die MSI-Regel fügt die DLL automatisch dem GAC hinzu und ist auf pro Computerbasis und nicht pro Benutzer zugänglich.
    
Die Lizenzbedingungen sind im verwaltete EWS-API Download enthalten. Lesen Sie die Bestimmungen für die autorisierenden Informationen dazu, was Sie mit der verwaltete EWS-API tun können.
  
## <a name="see-also"></a>Siehe auch


- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)
    
- [Verwaltete EWS-API (herunterladen)](https://aka.ms/ews-managed-api-readme)
    

