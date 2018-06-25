---
title: SmtpAddress (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 984ccd97-c337-47b6-ba42-3405a8b55a71
description: Das SmtpAddress-Element enthält die SMTP-Adresse für den Benutzer konfigurierten Nachricht Informationsspeicher für Öffentliche Ordner zugewiesen.
ms.openlocfilehash: 43ebb328e31cdec11412e80b743d4d4393b7960a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831507"
---
# <a name="smtpaddress-pox"></a><span data-ttu-id="a949a-103">SmtpAddress (POX)</span><span class="sxs-lookup"><span data-stu-id="a949a-103">SmtpAddress (POX)</span></span>

<span data-ttu-id="a949a-104">Das **SmtpAddress** -Element enthält die SMTP-Adresse für den Benutzer konfigurierten Nachricht Informationsspeicher für Öffentliche Ordner zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="a949a-104">The **SmtpAddress** element contains the SMTP address assigned to the public folder message store configured for the user.</span></span> 
  
- [<span data-ttu-id="a949a-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="a949a-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
- [<span data-ttu-id="a949a-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="a949a-106">Response (POX)</span></span>](response-pox.md)
  
- [<span data-ttu-id="a949a-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="a949a-107">Account (POX)</span></span>](account-pox.md)
  
- [<span data-ttu-id="a949a-108">PublicFolderInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="a949a-108">PublicFolderInformation (POX)</span></span>](publicfolderinformation-pox.md)
  
- [<span data-ttu-id="a949a-109">SmtpAddress (POX)</span><span class="sxs-lookup"><span data-stu-id="a949a-109">SmtpAddress (POX)</span></span>](smtpaddress-pox.md)
  
```XML
<SmtpAddress/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="a949a-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a949a-110">Attributes and elements</span></span>

<span data-ttu-id="a949a-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a949a-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a949a-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="a949a-112">Attributes</span></span>

<span data-ttu-id="a949a-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="a949a-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a949a-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a949a-114">Child elements</span></span>

<span data-ttu-id="a949a-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="a949a-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a949a-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a949a-116">Parent elements</span></span>

|<span data-ttu-id="a949a-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="a949a-117">**Element**</span></span>|<span data-ttu-id="a949a-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a949a-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a949a-119">PublicFolderInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="a949a-119">PublicFolderInformation (POX)</span></span>](publicfolderinformation-pox.md) <br/> |<span data-ttu-id="a949a-120">Enthält Informationen, mit denen Clients eine Anforderung der AutoErmittlung zum Ermitteln von Öffentliche Ordner-Informationen für den Benutzer zu senden.</span><span class="sxs-lookup"><span data-stu-id="a949a-120">Contains information that clients can use to send an Autodiscover request to discover public folder information for the user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a949a-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="a949a-121">Text value</span></span>

<span data-ttu-id="a949a-122">Der Textwert stellt die SMTP-Adresse für den Benutzer konfigurierten Informationsspeicher für Öffentliche Ordner zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="a949a-122">The text value represents the SMTP address assigned to the public folder store configured for the user.</span></span> <span data-ttu-id="a949a-123">Diese SMTP-Adresse kann zum Ermitteln der Öffentliche Ordner-Einstellungen im Element ["EmailAddress" (POX)](emailaddress-pox.md) einer Anforderung für die AutoErmittlung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a949a-123">This SMTP address can be used in the [EMailAddress (POX)](emailaddress-pox.md) element of an Autodiscover request to discover public folder settings.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a949a-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a949a-124">Remarks</span></span>

<span data-ttu-id="a949a-125">Das **SmtpAddress** -Element ist ein erforderliches untergeordnetes Element des **PublicFolderInformation** -Elements.</span><span class="sxs-lookup"><span data-stu-id="a949a-125">The **SmtpAddress** element is a required child element of the **PublicFolderInformation** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a949a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a949a-126">See also</span></span>

- [<span data-ttu-id="a949a-127">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="a949a-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

