---
title: Redistribution Anforderungen für die EWS Managed API
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8b206274-eaa4-40d3-b504-af27335c8f43
description: Erfahren Sie, wie Sie die EWS Managed API-Assemblys mit der Anwendung verteilen können.
ms.openlocfilehash: d8fc57c4a2b3ed7d6218aeeed0fe88c2d3e0fbe0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757120"
---
# <a name="redistribution-requirements-for-the-ews-managed-api"></a>Redistribution Anforderungen für die EWS Managed API

Erfahren Sie, wie Sie die EWS Managed API-Assemblys mit der Anwendung verteilen können.
  
Wie Sie die EWS Managed API-Anwendung entwerfen, sollten Sie berücksichtigen, wie Sie es den Benutzern freigegeben werden. 
  
## <a name="redistributing-your-ews-managed-api-application"></a>Verteilen von Ihrer Anwendung EWS Managed API

Es sei denn, die Anwendung auf dem Exchange-Server befindet, müssen Sie die EWS Managed API-Assemblys verteilen. Der EWS Managed API-Download enthält zwei Assemblys, die Sie weitergeben können: Microsoft.Exchange.WebServices.dll und Microsoft.Exchange.WebServices.Auth.dll. Beachten Sie die folgende Informationen beachten Sie beim Entwerfen, wie Sie Ihre Anwendung EWS Managed API freigegeben werden:
  
- Die EWS Managed API wurde so entworfen, dass Sie herunterladen und verteilen es mit der Anwendung, die auf einen Exchange-Server zu verweisen. Alternativ können Sie Ihre Anwendung die EWS Managed API herunterladen.
    
- Die EWS Managed API können Sie die Kommunikation mit einem Exchange-Server mit Exchange Online, Exchange Online als Teil von Office 365 oder eine lokale Version von Exchange, beginnend mit Exchange Server 2007.
    
- In Versionen von EWS Managed API beginnend mit Version 2.1 können Sie die API im globalen Assemblycache (GAC) installieren. Die MSI-Datei wird automatisch die DLL im globalen Assemblycache hinzufügen und auf Computerebene, nicht für jeden Benutzer einzeln zugegriffen werden.
    
Dazu gehören die Lizenzbedingungen im Download EWS Managed API. Beachten Sie die Bestimmungen für die autorisierende Informationen zu den Verwendungsmöglichkeiten für die EWS Managed API.
  
## <a name="see-also"></a>Siehe auch


- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)
    
- [EWS Managed API (Download)](http://aka.ms/ews-managed-api-readme)
    

