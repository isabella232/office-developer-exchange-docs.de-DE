---
title: Unified Messaging-webdienstreferenz für Exchange
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
description: Hier finden Sie Verweis Inhalte für den Webdienst Unified Messaging (UM) in Exchange.
ms.openlocfilehash: 12ee91c5a8b7e1ba23b937f142a9ae2835697fef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839292"
---
# <a name="unified-messaging-web-service-reference-for-exchange"></a><span data-ttu-id="1f3e3-103">Unified Messaging-webdienstreferenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="1f3e3-103">Unified Messaging web service reference for Exchange</span></span>

<span data-ttu-id="1f3e3-104">Hier finden Sie Verweis Inhalte für den Webdienst Unified Messaging (UM) in Exchange.</span><span class="sxs-lookup"><span data-stu-id="1f3e3-104">Find reference content for the Unified Messaging (UM) web service in Exchange.</span></span>
  
<span data-ttu-id="1f3e3-105">Der Webdienst für Unified Messaging (UM) bietet einen Erweiterungspunkt, mit der Clients zum Lesen und Ändern von Informationen über UM-Eigenschaften und anfordern, dass Store Postfachelemente analysiert und über ein Telefoniegerät vorgegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="1f3e3-105">The Unified Messaging (UM) web service provides an extensibility point that enables clients to read and change information about UM properties and request that mailbox store items be parsed and dictated over a telephony device.</span></span> <span data-ttu-id="1f3e3-106">Dieser Abschnitt enthält Informationen zu den Vorgängen und Elemente, die die XML-Nachrichten für den Webdienst UM bilden.</span><span class="sxs-lookup"><span data-stu-id="1f3e3-106">This section contains information about the operations and elements that make up the XML messages for the UM web service.</span></span> <span data-ttu-id="1f3e3-107">Dieser Inhalt gilt für die Service-Endpunkt-URL, die https:// ähnelt\<Yourclientaccessserver\>.com/EWS/UM2007Legacy.asmx.</span><span class="sxs-lookup"><span data-stu-id="1f3e3-107">This content applies to the service endpoint URL that is similar to https://\<yourclientaccessserver\>.com/EWS/UM2007Legacy.asmx.</span></span> 
  
<span data-ttu-id="1f3e3-108">Den AutoErmittlungsdienst können Sie die URL auf die Webdienst-Endpunkt UM abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1f3e3-108">You can use the Autodiscover service to get the URL to the UM web service endpoint.</span></span> <span data-ttu-id="1f3e3-109">Weitere Informationen zur AutoErmittlung finden Sie unter [AutoErmittlung für Exchange](../exchange-web-services/autodiscover-for-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="1f3e3-109">For more information about Autodiscover, see [Autodiscover for Exchange](../exchange-web-services/autodiscover-for-exchange.md).</span></span>
  
> [!NOTE]
>  <span data-ttu-id="1f3e3-110">Exchange beginnend mit Exchange 2010-Versionen, sollten Sie die Unified Messaging-Vorgänge verwenden, die in der [Exchange-Webdienste (EWS)](http://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx) anstelle des UM-Webdiensts aus den folgenden Gründen zur Verfügung stehen: > des EWS-basierte UM Features haben Erstklassige Unterstützung in die EWS Managed API.</span><span class="sxs-lookup"><span data-stu-id="1f3e3-110">For versions of Exchange starting with Exchange 2010, we recommend that you use the Unified Messaging operations that are available in [Exchange Web Services (EWS)](http://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx) instead of the UM web service, for the following reasons: >  The EWS-based UM features have first-class support in the EWS Managed API.</span></span> <span data-ttu-id="1f3e3-111">> In Exchange beginnend mit Exchange 2010-Versionen werden neue UM-Features für EWS jedoch nicht für den Unified Messaging-Webdienst hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1f3e3-111">>  In versions of Exchange starting with Exchange 2010, new UM features are added to EWS but not to the Unified Messaging web service.</span></span> 
  
<span data-ttu-id="1f3e3-112">Des UM-Webdiensts muss eine explizite Schema nicht.</span><span class="sxs-lookup"><span data-stu-id="1f3e3-112">The UM web service does not have an explicit schema.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="1f3e3-113">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="1f3e3-113">In this section</span></span>
<span data-ttu-id="1f3e3-114"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="1f3e3-114"></span></span>

- [<span data-ttu-id="1f3e3-115">Unified Messaging Web Service-Vorgänge für Exchange</span><span class="sxs-lookup"><span data-stu-id="1f3e3-115">Unified Messaging web service operations for Exchange</span></span>](unified-messaging-web-service-operations-for-exchange.md)
    
- [<span data-ttu-id="1f3e3-116">Unified Messaging Web Service XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="1f3e3-116">Unified Messaging web service XML elements for Exchange</span></span>](unified-messaging-web-service-xml-elements-for-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="1f3e3-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f3e3-117">See also</span></span>

- [<span data-ttu-id="1f3e3-118">AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="1f3e3-118">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="1f3e3-119">AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="1f3e3-119">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
- [<span data-ttu-id="1f3e3-120">Erste Schritte mit Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="1f3e3-120">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

