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
# <a name="autodiscover-web-service-reference-for-exchange"></a><span data-ttu-id="c0037-103">AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="c0037-103">Autodiscover web service reference for Exchange</span></span>

<span data-ttu-id="c0037-104">Hier finden Sie Referenzinhalte für den AutoErmittlungsdienst in Exchange.</span><span class="sxs-lookup"><span data-stu-id="c0037-104">Find reference content for the Autodiscover web service in Exchange.</span></span>
  
<span data-ttu-id="c0037-105">Der AutoErmittlungsdienst stellt die Konfigurationsinformationen bereit, die Ihre Anwendung zum Erstellen einer Verbindung mit einem Exchange-Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="c0037-105">The Autodiscover web service provides the configuration information that your application uses to create a connection to an Exchange server.</span></span> <span data-ttu-id="c0037-106">Sie können eine der folgenden Optionen verwenden, um eine Verbindung mit der AutoErmittlung herzustellen:</span><span class="sxs-lookup"><span data-stu-id="c0037-106">You can use one of the following options to connect to Autodiscover:</span></span>
  
- <span data-ttu-id="c0037-107">SOAP-AutoErmittlungsdienst – verfügbar für Clients, die mit Exchange 2010, einschließlich Exchange Online, eine Verbindung mit Exchange-Versionen herstellen.</span><span class="sxs-lookup"><span data-stu-id="c0037-107">SOAP Autodiscover service —Available to clients that connect to versions of Exchange starting with Exchange 2010, including Exchange Online.</span></span>
    
- <span data-ttu-id="c0037-108">"Plain Old XML" (POX) AutoErmittlungsdienst – verfügbar für Clients, die eine Verbindung mit Exchange-Versionen herstellen, beginnend mit Exchange 2007, einschließlich Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="c0037-108">"plain old XML" (POX) Autodiscover service — Available to clients that connect to versions of Exchange starting with Exchange 2007, including Exchange Online.</span></span> 
    
<span data-ttu-id="c0037-109">Sowohl der SOAP-als auch der POX-AutoErmittlungsdienst können die Konfigurationsinformationen bereitstellen, die vom Client zum Erstellen einer Verbindung mit einem Exchange-Server verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0037-109">Both the SOAP and the POX Autodiscover service can provide the configuration information that your client will use to create a connection to an Exchange server.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c0037-110">Für Exchange-Versionen, die mit Exchange 2010 beginnen, wird empfohlen, den SOAP-AutoErmittlungsdienst anstelle des POX-AutoErmittlungsdiensts zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c0037-110">For versions of Exchange starting with Exchange 2010, we recommend that you use the SOAP Autodiscover service instead of the POX Autodiscover service.</span></span> <span data-ttu-id="c0037-111">Der SOAP-AutoErmittlungsdienst bietet Batched AutoErmittlungs-Einstellungsanforderungen und eine präzisere Kontrolle darüber, welche Einstellungen in der Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c0037-111">The SOAP Autodiscover service provides batched Autodiscover setting requests and more granular control over which settings are returned in the response.</span></span> 
  
<span data-ttu-id="c0037-112">Dieser Abschnitt enthält Referenzinformationen für den SOAP-AutoErmittlungsdienst und den POX-AutoErmittlungsdienst.</span><span class="sxs-lookup"><span data-stu-id="c0037-112">This section contains reference information for the SOAP Autodiscover service and the POX Autodiscover service.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="c0037-113">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="c0037-113">In this section</span></span>
<span data-ttu-id="c0037-114"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="c0037-114"><a name="bk_InThisSection"> </a></span></span>

- [<span data-ttu-id="c0037-115">Referenz zum SOAP-AutoErmittlungwebdienst für Exchange</span><span class="sxs-lookup"><span data-stu-id="c0037-115">SOAP Autodiscover web service reference for Exchange</span></span>](soap-autodiscover-web-service-reference-for-exchange.md)
    
- [<span data-ttu-id="c0037-116">Referenz zum POX-AutoErmittlungwebdienst für Exchange</span><span class="sxs-lookup"><span data-stu-id="c0037-116">POX Autodiscover web service reference for Exchange</span></span>](pox-autodiscover-web-service-reference-for-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="c0037-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0037-117">See also</span></span>

- [<span data-ttu-id="c0037-118">Webdienstreferenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="c0037-118">Web services reference for Exchange</span></span>](web-services-reference-for-exchange.md)
- [<span data-ttu-id="c0037-119">AutoErmittlungsdienst (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c0037-119">Autodiscover Service (SOAP)</span></span>](https://msdn.microsoft.com/library/e24d1a1f-0d20-4bd9-ae4c-9112ecacea78%28Office.15%29.aspx)
- [<span data-ttu-id="c0037-120">AutoErmittlungsdienst (POX)</span><span class="sxs-lookup"><span data-stu-id="c0037-120">Autodiscover Service (POX)</span></span>](https://msdn.microsoft.com/library/13c54de3-a91c-4424-8732-99dd8f2162ec%28Office.15%29.aspx)
    

