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
description: Hier finden Sie Verweis Inhalte für den Webdienst für die AutoErmittlung in Exchange.
ms.openlocfilehash: 48ca4a93c2120079cb675eabbc460bf0e75570b2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757416"
---
# <a name="autodiscover-web-service-reference-for-exchange"></a><span data-ttu-id="60ff1-103">AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="60ff1-103">Autodiscover web service reference for Exchange</span></span>

<span data-ttu-id="60ff1-104">Hier finden Sie Verweis Inhalte für den Webdienst für die AutoErmittlung in Exchange.</span><span class="sxs-lookup"><span data-stu-id="60ff1-104">Find reference content for the Autodiscover web service in Exchange.</span></span>
  
<span data-ttu-id="60ff1-105">Der AutoErmittlung-Webdienst bietet die Konfigurationsinformationen, die die Anwendung wird verwendet, um eine Verbindung mit einem Exchange-Server erstellen.</span><span class="sxs-lookup"><span data-stu-id="60ff1-105">The Autodiscover web service provides the configuration information that your application uses to create a connection to an Exchange server.</span></span> <span data-ttu-id="60ff1-106">Sie können eine der folgenden Optionen zum Herstellen einer Verbindung für die AutoErmittlung verwenden:</span><span class="sxs-lookup"><span data-stu-id="60ff1-106">You can use one of the following options to connect to Autodiscover:</span></span>
  
- <span data-ttu-id="60ff1-107">SOAP-AutoErmittlungsdienst – verfügbar für Clients, die Versionen von Exchange, beginnend mit Exchange 2010, einschließlich Exchange Online herstellen.</span><span class="sxs-lookup"><span data-stu-id="60ff1-107">SOAP Autodiscover service —Available to clients that connect to versions of Exchange starting with Exchange 2010, including Exchange Online.</span></span>
    
- <span data-ttu-id="60ff1-108">"einfache alte XML" AutoErmittlungsdienst (POX) – verfügbar für Clients, die Versionen von Exchange, beginnend mit Exchange 2007, einschließlich Exchange Online herstellen.</span><span class="sxs-lookup"><span data-stu-id="60ff1-108">"plain old XML" (POX) Autodiscover service — Available to clients that connect to versions of Exchange starting with Exchange 2007, including Exchange Online.</span></span> 
    
<span data-ttu-id="60ff1-109">Die SOAP- und den AutoErmittlungsdienst POX können die Konfigurationsinformationen bereitstellen, mit denen der Client eine Verbindung mit einem Exchange-Server erstellen.</span><span class="sxs-lookup"><span data-stu-id="60ff1-109">Both the SOAP and the POX Autodiscover service can provide the configuration information that your client will use to create a connection to an Exchange server.</span></span>
  
> [!NOTE]
> <span data-ttu-id="60ff1-110">Für Exchange, beginnend mit Exchange 2010-Versionen wird empfohlen, für die Verwendung von SOAP-AutoErmittlungsdienst anstelle des AutoErmittlungsdiensts POX.</span><span class="sxs-lookup"><span data-stu-id="60ff1-110">For versions of Exchange starting with Exchange 2010, we recommend that you use the SOAP Autodiscover service instead of the POX Autodiscover service.</span></span> <span data-ttu-id="60ff1-111">Der SOAP-AutoErmittlungsdienst enthält Batchanforderungen AutoErmittlung Einstellung und eine genauere Kontrolle über die Einstellungen in der Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="60ff1-111">The SOAP Autodiscover service provides batched Autodiscover setting requests and more granular control over which settings are returned in the response.</span></span> 
  
<span data-ttu-id="60ff1-112">Dieser Abschnitt enthält Referenzinformationen für die SOAP-AutoErmittlungsdienst und POX AutoErmittlungsdienst.</span><span class="sxs-lookup"><span data-stu-id="60ff1-112">This section contains reference information for the SOAP Autodiscover service and the POX Autodiscover service.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="60ff1-113">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="60ff1-113">In this section</span></span>
<span data-ttu-id="60ff1-114"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="60ff1-114"></span></span>

- [<span data-ttu-id="60ff1-115">SOAP-Webdienst-Verweis für die AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="60ff1-115">SOAP Autodiscover web service reference for Exchange</span></span>](soap-autodiscover-web-service-reference-for-exchange.md)
    
- [<span data-ttu-id="60ff1-116">POX AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="60ff1-116">POX Autodiscover web service reference for Exchange</span></span>](pox-autodiscover-web-service-reference-for-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="60ff1-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60ff1-117">See also</span></span>

- [<span data-ttu-id="60ff1-118">Referenz für Webdienste für Exchange</span><span class="sxs-lookup"><span data-stu-id="60ff1-118">Web services reference for Exchange</span></span>](web-services-reference-for-exchange.md)
- [<span data-ttu-id="60ff1-119">AutoErmittlungsdienst (SOAP)</span><span class="sxs-lookup"><span data-stu-id="60ff1-119">Autodiscover Service (SOAP)</span></span>](http://msdn.microsoft.com/library/e24d1a1f-0d20-4bd9-ae4c-9112ecacea78%28Office.15%29.aspx)
- [<span data-ttu-id="60ff1-120">AutoErmittlungsdienst (POX)</span><span class="sxs-lookup"><span data-stu-id="60ff1-120">Autodiscover Service (POX)</span></span>](http://msdn.microsoft.com/library/13c54de3-a91c-4424-8732-99dd8f2162ec%28Office.15%29.aspx)
    

