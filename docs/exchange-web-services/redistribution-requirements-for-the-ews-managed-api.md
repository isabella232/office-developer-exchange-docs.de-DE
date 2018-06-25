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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757120"
---
# <a name="redistribution-requirements-for-the-ews-managed-api"></a><span data-ttu-id="9d1d7-103">Redistribution Anforderungen für die EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="9d1d7-103">Redistribution requirements for the EWS Managed API</span></span>

<span data-ttu-id="9d1d7-104">Erfahren Sie, wie Sie die EWS Managed API-Assemblys mit der Anwendung verteilen können.</span><span class="sxs-lookup"><span data-stu-id="9d1d7-104">Find out how you can redistribute the EWS Managed API assemblies with your application.</span></span>
  
<span data-ttu-id="9d1d7-105">Wie Sie die EWS Managed API-Anwendung entwerfen, sollten Sie berücksichtigen, wie Sie es den Benutzern freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9d1d7-105">As you design your EWS Managed API application, you'll also want to consider how you will release it to your users.</span></span> 
  
## <a name="redistributing-your-ews-managed-api-application"></a><span data-ttu-id="9d1d7-106">Verteilen von Ihrer Anwendung EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="9d1d7-106">Redistributing your EWS Managed API application</span></span>

<span data-ttu-id="9d1d7-107">Es sei denn, die Anwendung auf dem Exchange-Server befindet, müssen Sie die EWS Managed API-Assemblys verteilen.</span><span class="sxs-lookup"><span data-stu-id="9d1d7-107">Unless your application is located on the Exchange server, you will need to redistribute the EWS Managed API assemblies.</span></span> <span data-ttu-id="9d1d7-108">Der EWS Managed API-Download enthält zwei Assemblys, die Sie weitergeben können: Microsoft.Exchange.WebServices.dll und Microsoft.Exchange.WebServices.Auth.dll.</span><span class="sxs-lookup"><span data-stu-id="9d1d7-108">The EWS Managed API download contains two assemblies that you can redistribute: Microsoft.Exchange.WebServices.dll and Microsoft.Exchange.WebServices.Auth.dll.</span></span> <span data-ttu-id="9d1d7-109">Beachten Sie die folgende Informationen beachten Sie beim Entwerfen, wie Sie Ihre Anwendung EWS Managed API freigegeben werden:</span><span class="sxs-lookup"><span data-stu-id="9d1d7-109">Keep the following information in mind when you design how you will release your EWS Managed API application:</span></span>
  
- <span data-ttu-id="9d1d7-110">Die EWS Managed API wurde so entworfen, dass Sie herunterladen und verteilen es mit der Anwendung, die auf einen Exchange-Server zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="9d1d7-110">The EWS Managed API was designed such that you can download it and distribute it with your application that targets an Exchange server.</span></span> <span data-ttu-id="9d1d7-111">Alternativ können Sie Ihre Anwendung die EWS Managed API herunterladen.</span><span class="sxs-lookup"><span data-stu-id="9d1d7-111">Alternatively, your application can download the EWS Managed API.</span></span>
    
- <span data-ttu-id="9d1d7-112">Die EWS Managed API können Sie die Kommunikation mit einem Exchange-Server mit Exchange Online, Exchange Online als Teil von Office 365 oder eine lokale Version von Exchange, beginnend mit Exchange Server 2007.</span><span class="sxs-lookup"><span data-stu-id="9d1d7-112">You can use the EWS Managed API to communicate with an Exchange server running Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange Server 2007.</span></span>
    
- <span data-ttu-id="9d1d7-113">In Versionen von EWS Managed API beginnend mit Version 2.1 können Sie die API im globalen Assemblycache (GAC) installieren.</span><span class="sxs-lookup"><span data-stu-id="9d1d7-113">In versions of the EWS Managed API starting with version 2.1, you can install the API in the Global Assembly Cache (GAC).</span></span> <span data-ttu-id="9d1d7-114">Die MSI-Datei wird automatisch die DLL im globalen Assemblycache hinzufügen und auf Computerebene, nicht für jeden Benutzer einzeln zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="9d1d7-114">The MSI will automatically add the DLL to the GAC and will be accessible on per computer basis, not on a per user basis.</span></span>
    
<span data-ttu-id="9d1d7-115">Dazu gehören die Lizenzbedingungen im Download EWS Managed API.</span><span class="sxs-lookup"><span data-stu-id="9d1d7-115">The license terms are included in the EWS Managed API download.</span></span> <span data-ttu-id="9d1d7-116">Beachten Sie die Bestimmungen für die autorisierende Informationen zu den Verwendungsmöglichkeiten für die EWS Managed API.</span><span class="sxs-lookup"><span data-stu-id="9d1d7-116">Review the terms for the authoritative information about what you can do with the EWS Managed API.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9d1d7-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d1d7-117">See also</span></span>


- [<span data-ttu-id="9d1d7-118">Übersicht über den EWS-Cliententwurf für Exchange</span><span class="sxs-lookup"><span data-stu-id="9d1d7-118">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)
    
- [<span data-ttu-id="9d1d7-119">EWS Managed API (Download)</span><span class="sxs-lookup"><span data-stu-id="9d1d7-119">EWS Managed API (download)</span></span>](http://aka.ms/ews-managed-api-readme)
    

