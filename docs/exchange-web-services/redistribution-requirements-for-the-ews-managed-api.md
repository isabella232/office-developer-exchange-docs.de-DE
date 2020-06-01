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
# <a name="redistribution-requirements-for-the-ews-managed-api"></a><span data-ttu-id="89024-103">Redistribution Anforderungen für die EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="89024-103">Redistribution requirements for the EWS Managed API</span></span>

<span data-ttu-id="89024-104">Erfahren Sie, wie Sie die verwaltete EWS-API-Assemblys mit Ihrer Anwendung neu verteilen können.</span><span class="sxs-lookup"><span data-stu-id="89024-104">Find out how you can redistribute the EWS Managed API assemblies with your application.</span></span>
  
<span data-ttu-id="89024-105">Wenn Sie Ihre verwaltete EWS-API-Anwendung entwerfen, sollten Sie auch prüfen, wie Sie Sie für Ihre Benutzer freigeben werden.</span><span class="sxs-lookup"><span data-stu-id="89024-105">As you design your EWS Managed API application, you'll also want to consider how you will release it to your users.</span></span> 
  
## <a name="redistributing-your-ews-managed-api-application"></a><span data-ttu-id="89024-106">Neuverteilen ihrer verwaltete EWS-API Anwendung</span><span class="sxs-lookup"><span data-stu-id="89024-106">Redistributing your EWS Managed API application</span></span>

<span data-ttu-id="89024-107">Wenn sich Ihre Anwendung nicht auf dem Exchange-Server befindet, müssen Sie die verwaltete EWS-API-Assemblys erneut verteilen.</span><span class="sxs-lookup"><span data-stu-id="89024-107">Unless your application is located on the Exchange server, you will need to redistribute the EWS Managed API assemblies.</span></span> <span data-ttu-id="89024-108">Der verwaltete EWS-API Download enthält zwei Assemblys, die Sie erneut verteilen können: Microsoft. Exchange. Webservices. dll und Microsoft. Exchange. Webservices. auth. dll.</span><span class="sxs-lookup"><span data-stu-id="89024-108">The EWS Managed API download contains two assemblies that you can redistribute: Microsoft.Exchange.WebServices.dll and Microsoft.Exchange.WebServices.Auth.dll.</span></span> <span data-ttu-id="89024-109">Beachten Sie beim Entwerfen der Veröffentlichung ihrer verwaltete EWS-API Anwendung die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="89024-109">Keep the following information in mind when you design how you will release your EWS Managed API application:</span></span>
  
- <span data-ttu-id="89024-110">Die verwaltete EWS-API wurde so konzipiert, dass Sie Sie herunterladen und mit Ihrer Anwendung, die auf einen Exchange-Server zielt, verteilen können.</span><span class="sxs-lookup"><span data-stu-id="89024-110">The EWS Managed API was designed such that you can download it and distribute it with your application that targets an Exchange server.</span></span> <span data-ttu-id="89024-111">Alternativ kann Ihre Anwendung die verwaltete EWS-API herunterladen.</span><span class="sxs-lookup"><span data-stu-id="89024-111">Alternatively, your application can download the EWS Managed API.</span></span>
    
- <span data-ttu-id="89024-112">Sie können die verwaltete EWS-API verwenden, um mit einem Exchange-Server zu kommunizieren, der Exchange Online ausführt, Exchange Online als Teil Office 365 oder einer lokalen Exchange-Version, die mit Exchange Server 2007 beginnt.</span><span class="sxs-lookup"><span data-stu-id="89024-112">You can use the EWS Managed API to communicate with an Exchange server running Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange Server 2007.</span></span>
    
- <span data-ttu-id="89024-113">In Versionen der verwaltete EWS-API ab Version 2,1 können Sie die API im globalen Assemblycache (GAC) installieren.</span><span class="sxs-lookup"><span data-stu-id="89024-113">In versions of the EWS Managed API starting with version 2.1, you can install the API in the Global Assembly Cache (GAC).</span></span> <span data-ttu-id="89024-114">Die MSI-Regel fügt die DLL automatisch dem GAC hinzu und ist auf pro Computerbasis und nicht pro Benutzer zugänglich.</span><span class="sxs-lookup"><span data-stu-id="89024-114">The MSI will automatically add the DLL to the GAC and will be accessible on per computer basis, not on a per user basis.</span></span>
    
<span data-ttu-id="89024-115">Die Lizenzbedingungen sind im verwaltete EWS-API Download enthalten.</span><span class="sxs-lookup"><span data-stu-id="89024-115">The license terms are included in the EWS Managed API download.</span></span> <span data-ttu-id="89024-116">Lesen Sie die Bestimmungen für die autorisierenden Informationen dazu, was Sie mit der verwaltete EWS-API tun können.</span><span class="sxs-lookup"><span data-stu-id="89024-116">Review the terms for the authoritative information about what you can do with the EWS Managed API.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="89024-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89024-117">See also</span></span>


- [<span data-ttu-id="89024-118">Übersicht über den EWS-Cliententwurf für Exchange</span><span class="sxs-lookup"><span data-stu-id="89024-118">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)
    
- [<span data-ttu-id="89024-119">Verwaltete EWS-API (herunterladen)</span><span class="sxs-lookup"><span data-stu-id="89024-119">EWS Managed API (download)</span></span>](https://aka.ms/ews-managed-api-readme)
    

