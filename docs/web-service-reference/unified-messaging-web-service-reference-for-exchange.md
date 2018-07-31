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
ms.openlocfilehash: 9e124f504ecee517edc51610696f06729904d75f
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354274"
---
# <a name="unified-messaging-web-service-reference-for-exchange"></a><span data-ttu-id="37d16-103">Unified Messaging-webdienstreferenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="37d16-103">Unified Messaging web service reference for Exchange</span></span>

<span data-ttu-id="37d16-104">Hier finden Sie Verweis Inhalte für den Webdienst Unified Messaging (UM) in Exchange.</span><span class="sxs-lookup"><span data-stu-id="37d16-104">Find reference content for the Unified Messaging (UM) web service in Exchange.</span></span>
  
<span data-ttu-id="37d16-105">Der Webdienst für Unified Messaging (UM) bietet einen Erweiterungspunkt, mit der Clients zum Lesen und Ändern von Informationen über UM-Eigenschaften und anfordern, dass Store Postfachelemente analysiert und über ein Telefoniegerät vorgegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="37d16-105">The Unified Messaging (UM) web service provides an extensibility point that enables clients to read and change information about UM properties and request that mailbox store items be parsed and dictated over a telephony device.</span></span> <span data-ttu-id="37d16-106">Dieser Abschnitt enthält Informationen zu den Vorgängen und Elemente, die die XML-Nachrichten für den Webdienst UM bilden.</span><span class="sxs-lookup"><span data-stu-id="37d16-106">This section contains information about the operations and elements that make up the XML messages for the UM web service.</span></span> <span data-ttu-id="37d16-107">Dieser Inhalt gilt für die Service-Endpunkt-URL, die https:// ähnelt\<Yourclientaccessserver\>.com/EWS/UM2007Legacy.asmx.</span><span class="sxs-lookup"><span data-stu-id="37d16-107">This content applies to the service endpoint URL that is similar to https://\<yourclientaccessserver\>.com/EWS/UM2007Legacy.asmx.</span></span> 
  
<span data-ttu-id="37d16-108">Den AutoErmittlungsdienst können Sie die URL auf die Webdienst-Endpunkt UM abzurufen.</span><span class="sxs-lookup"><span data-stu-id="37d16-108">You can use the Autodiscover service to get the URL to the UM web service endpoint.</span></span> <span data-ttu-id="37d16-109">Weitere Informationen zur AutoErmittlung finden Sie unter [AutoErmittlung für Exchange](../exchange-web-services/autodiscover-for-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="37d16-109">For more information about Autodiscover, see [Autodiscover for Exchange](../exchange-web-services/autodiscover-for-exchange.md).</span></span>
  
> [!NOTE]
>  <span data-ttu-id="37d16-110">Exchange beginnend mit Exchange 2010-Versionen wird empfohlen, dass Sie die Unified Messaging-Vorgänge verwenden, die in der [Exchange-Webdienste (EWS)](http://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx) anstelle des UM-Webdiensts aus den folgenden Gründen verfügbar sind:</span><span class="sxs-lookup"><span data-stu-id="37d16-110">For versions of Exchange starting with Exchange 2010, we recommend that you use the Unified Messaging operations that are available in [Exchange Web Services (EWS)](http://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx) instead of the UM web service, for the following reasons:</span></span> 
> - <span data-ttu-id="37d16-111">Der EWS-basierte UM Features haben erstklassige Unterstützung in die EWS Managed API.</span><span class="sxs-lookup"><span data-stu-id="37d16-111">The EWS-based UM features have first-class support in the EWS Managed API.</span></span> 
> - <span data-ttu-id="37d16-112">In Versionen von Exchange, beginnend mit Exchange 2010 werden neue UM-Features für EWS jedoch nicht für den Unified Messaging-Webdienst hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37d16-112">In versions of Exchange starting with Exchange 2010, new UM features are added to EWS but not to the Unified Messaging web service.</span></span> 
  
<span data-ttu-id="37d16-113">Des UM-Webdiensts muss eine explizite Schema nicht.</span><span class="sxs-lookup"><span data-stu-id="37d16-113">The UM web service does not have an explicit schema.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="37d16-114">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="37d16-114">In this section</span></span>
<span data-ttu-id="37d16-115"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="37d16-115"></span></span>

- [<span data-ttu-id="37d16-116">Unified Messaging Web Service-Vorgänge für Exchange</span><span class="sxs-lookup"><span data-stu-id="37d16-116">Unified Messaging web service operations for Exchange</span></span>](unified-messaging-web-service-operations-for-exchange.md)   
- [<span data-ttu-id="37d16-117">Unified Messaging Web Service XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="37d16-117">Unified Messaging web service XML elements for Exchange</span></span>](unified-messaging-web-service-xml-elements-for-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="37d16-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37d16-118">See also</span></span>

- [<span data-ttu-id="37d16-119">AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="37d16-119">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="37d16-120">AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="37d16-120">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
- [<span data-ttu-id="37d16-121">Erste Schritte mit Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="37d16-121">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

