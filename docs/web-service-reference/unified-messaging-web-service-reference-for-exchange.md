---
title: Unified Messaging-Webdienst Referenz für Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- Unified
api_type:
- schema
ms.assetid: 83afea8a-c716-41df-9eb2-e1000357afb6
description: Hier finden Sie Referenzinhalte für den um-Webdienst (Unified Messaging) in Exchange.
ms.openlocfilehash: e4bb63f34650dae8fc28016196c97a6b79e69df0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467375"
---
# <a name="unified-messaging-web-service-reference-for-exchange"></a><span data-ttu-id="9c318-103">Unified Messaging-Webdienst Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="9c318-103">Unified Messaging web service reference for Exchange</span></span>

<span data-ttu-id="9c318-104">Hier finden Sie Referenzinhalte für den um-Webdienst (Unified Messaging) in Exchange.</span><span class="sxs-lookup"><span data-stu-id="9c318-104">Find reference content for the Unified Messaging (UM) web service in Exchange.</span></span>
  
<span data-ttu-id="9c318-105">Der um-Webdienst (Unified Messaging) stellt einen Erweiterbarkeits Pfad bereit, mit dem Clients Informationen zu um-Eigenschaften lesen und ändern und anfordern können, dass Postfachspeicher Elemente analysiert und über ein Telefongerät diktiert werden.</span><span class="sxs-lookup"><span data-stu-id="9c318-105">The Unified Messaging (UM) web service provides an extensibility point that enables clients to read and change information about UM properties and request that mailbox store items be parsed and dictated over a telephony device.</span></span> <span data-ttu-id="9c318-106">Dieser Abschnitt enthält Informationen zu den Vorgängen und Elementen, aus denen sich die XML-Nachrichten für den um-Webdienst zusammensetzen.</span><span class="sxs-lookup"><span data-stu-id="9c318-106">This section contains information about the operations and elements that make up the XML messages for the UM web service.</span></span> <span data-ttu-id="9c318-107">Dieser Inhalt bezieht sich auf die Dienstendpunkt-URL, die https:// \<yourclientaccessserver\> . com/EWS/UM2007Legacy. asmx ähnelt.</span><span class="sxs-lookup"><span data-stu-id="9c318-107">This content applies to the service endpoint URL that is similar to https://\<yourclientaccessserver\>.com/EWS/UM2007Legacy.asmx.</span></span> 
  
<span data-ttu-id="9c318-108">Sie können den AutoErmittlungsdienst verwenden, um die URL zum um-Webdienst-Endpunkt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9c318-108">You can use the Autodiscover service to get the URL to the UM web service endpoint.</span></span> <span data-ttu-id="9c318-109">Weitere Informationen zur AutoErmittlung finden Sie unter [AutoErmittlung für Exchange](../exchange-web-services/autodiscover-for-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="9c318-109">For more information about Autodiscover, see [Autodiscover for Exchange](../exchange-web-services/autodiscover-for-exchange.md).</span></span>
  
> [!NOTE]
>  <span data-ttu-id="9c318-110">Für Exchange-Versionen, die mit Exchange 2010 beginnen, wird empfohlen, dass Sie die Unified Messaging-Vorgänge verwenden, die in [Exchange-Webdienste](https://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx) anstelle des um-Webdiensts verfügbar sind, aus den folgenden Gründen:</span><span class="sxs-lookup"><span data-stu-id="9c318-110">For versions of Exchange starting with Exchange 2010, we recommend that you use the Unified Messaging operations that are available in [Exchange Web Services (EWS)](https://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx) instead of the UM web service, for the following reasons:</span></span> 
> - <span data-ttu-id="9c318-111">Die EWS-basierten um-Features haben im verwaltete EWS-API eine erstklassige Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="9c318-111">The EWS-based UM features have first-class support in the EWS Managed API.</span></span> 
> - <span data-ttu-id="9c318-112">In Exchange-Versionen, die mit Exchange 2010 beginnen, werden dem EWS neue um-Features hinzugefügt, jedoch nicht dem Unified Messaging-Webdienst.</span><span class="sxs-lookup"><span data-stu-id="9c318-112">In versions of Exchange starting with Exchange 2010, new UM features are added to EWS but not to the Unified Messaging web service.</span></span> 
  
<span data-ttu-id="9c318-113">Der um-Webdienst verfügt nicht über ein explizites Schema.</span><span class="sxs-lookup"><span data-stu-id="9c318-113">The UM web service does not have an explicit schema.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="9c318-114">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="9c318-114">In this section</span></span>
<span data-ttu-id="9c318-115"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="9c318-115"><a name="bk_InThisSection"> </a></span></span>

- [<span data-ttu-id="9c318-116">Unified Messaging-Webdienstvorgänge für Exchange</span><span class="sxs-lookup"><span data-stu-id="9c318-116">Unified Messaging web service operations for Exchange</span></span>](unified-messaging-web-service-operations-for-exchange.md)   
- [<span data-ttu-id="9c318-117">XML-Elemente des Unified Messaging-Webdiensts für Exchange</span><span class="sxs-lookup"><span data-stu-id="9c318-117">Unified Messaging web service XML elements for Exchange</span></span>](unified-messaging-web-service-xml-elements-for-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="9c318-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c318-118">See also</span></span>

- [<span data-ttu-id="9c318-119">AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="9c318-119">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="9c318-120">AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="9c318-120">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
- [<span data-ttu-id="9c318-121">Erste Schritte mit Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="9c318-121">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

