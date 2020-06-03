---
title: SmtpAddress (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 984ccd97-c337-47b6-ba42-3405a8b55a71
description: Das SmtpAddress-Element enthält die SMTP-Adresse, die dem Nachrichtenspeicher für Öffentliche Ordner zugewiesen ist, der für den Benutzer konfiguriert ist.
ms.openlocfilehash: 48703a11fb056967c6c76073c2e928d5f6efa264
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468642"
---
# <a name="smtpaddress-pox"></a><span data-ttu-id="537d9-103">SmtpAddress (POX)</span><span class="sxs-lookup"><span data-stu-id="537d9-103">SmtpAddress (POX)</span></span>

<span data-ttu-id="537d9-104">Das **SmtpAddress** -Element enthält die SMTP-Adresse, die dem Nachrichtenspeicher für Öffentliche Ordner zugewiesen ist, der für den Benutzer konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="537d9-104">The **SmtpAddress** element contains the SMTP address assigned to the public folder message store configured for the user.</span></span> 
  
- [<span data-ttu-id="537d9-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="537d9-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
- [<span data-ttu-id="537d9-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="537d9-106">Response (POX)</span></span>](response-pox.md)
  
- [<span data-ttu-id="537d9-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="537d9-107">Account (POX)</span></span>](account-pox.md)
  
- [<span data-ttu-id="537d9-108">PublicFolderInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="537d9-108">PublicFolderInformation (POX)</span></span>](publicfolderinformation-pox.md)
  
- [<span data-ttu-id="537d9-109">SmtpAddress (POX)</span><span class="sxs-lookup"><span data-stu-id="537d9-109">SmtpAddress (POX)</span></span>](smtpaddress-pox.md)
  
```XML
<SmtpAddress/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="537d9-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="537d9-110">Attributes and elements</span></span>

<span data-ttu-id="537d9-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="537d9-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="537d9-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="537d9-112">Attributes</span></span>

<span data-ttu-id="537d9-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="537d9-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="537d9-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="537d9-114">Child elements</span></span>

<span data-ttu-id="537d9-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="537d9-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="537d9-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="537d9-116">Parent elements</span></span>

|<span data-ttu-id="537d9-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="537d9-117">**Element**</span></span>|<span data-ttu-id="537d9-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="537d9-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="537d9-119">PublicFolderInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="537d9-119">PublicFolderInformation (POX)</span></span>](publicfolderinformation-pox.md) <br/> |<span data-ttu-id="537d9-120">Enthält Informationen, die Clients verwenden können, um eine Auto Ermittlungsanforderung zu senden, um Informationen zu öffentlichen Ordnern für den Benutzer zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="537d9-120">Contains information that clients can use to send an Autodiscover request to discover public folder information for the user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="537d9-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="537d9-121">Text value</span></span>

<span data-ttu-id="537d9-122">Der Wert Text stellt die SMTP-Adresse dar, die dem für den Benutzer konfigurierten Informationsspeicher für Öffentliche Ordner zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="537d9-122">The text value represents the SMTP address assigned to the public folder store configured for the user.</span></span> <span data-ttu-id="537d9-123">Diese SMTP-Adresse kann im [Pocken Element (POX)](emailaddress-pox.md) einer Auto Ermittlungsanforderung verwendet werden, um Einstellungen für Öffentliche Ordner zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="537d9-123">This SMTP address can be used in the [EMailAddress (POX)](emailaddress-pox.md) element of an Autodiscover request to discover public folder settings.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="537d9-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="537d9-124">Remarks</span></span>

<span data-ttu-id="537d9-125">Das **SmtpAddress** -Element ist ein erforderliches untergeordnetes Element des **PublicFolderInformation** -Elements.</span><span class="sxs-lookup"><span data-stu-id="537d9-125">The **SmtpAddress** element is a required child element of the **PublicFolderInformation** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="537d9-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="537d9-126">See also</span></span>

- [<span data-ttu-id="537d9-127">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="537d9-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

