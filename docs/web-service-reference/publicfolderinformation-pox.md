---
title: PublicFolderInformation (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a221aa9e-b4ac-4ec5-aa42-7e2a69e8eaa6
description: Das PublicFolderInformation-Element enthält Informationen, die Clients zum Senden einer Anforderung der AutoErmittlung zum Ermitteln von Informationen für den Benutzer für Öffentliche Ordner verwenden können.
ms.openlocfilehash: bb4432a664024c3d1ccb17826948cfe7a1b58cdf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830927"
---
# <a name="publicfolderinformation-pox"></a><span data-ttu-id="55dbe-103">PublicFolderInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="55dbe-103">PublicFolderInformation (POX)</span></span>

<span data-ttu-id="55dbe-104">Das **PublicFolderInformation** -Element enthält Informationen, die Clients zum Senden einer Anforderung der AutoErmittlung zum Ermitteln von Informationen für den Benutzer für Öffentliche Ordner verwenden können.</span><span class="sxs-lookup"><span data-stu-id="55dbe-104">The **PublicFolderInformation** element contains information that clients can use to send an Autodiscover request to discover public folder information for the user.</span></span> 
  
[<span data-ttu-id="55dbe-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="55dbe-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="55dbe-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="55dbe-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="55dbe-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="55dbe-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="55dbe-108">PublicFolderInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="55dbe-108">PublicFolderInformation (POX)</span></span>](publicfolderinformation-pox.md)
  
```XML
<PublicFolderInformation>
   <SmtpAddress/>
</PublicFolderInformation>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="55dbe-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="55dbe-109">Attributes and elements</span></span>

<span data-ttu-id="55dbe-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="55dbe-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="55dbe-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="55dbe-111">Attributes</span></span>

<span data-ttu-id="55dbe-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="55dbe-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="55dbe-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="55dbe-113">Child elements</span></span>

|<span data-ttu-id="55dbe-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="55dbe-114">**Element**</span></span>|<span data-ttu-id="55dbe-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="55dbe-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="55dbe-116">SmtpAddress (POX)</span><span class="sxs-lookup"><span data-stu-id="55dbe-116">SmtpAddress (POX)</span></span>](smtpaddress-pox.md) <br/> |<span data-ttu-id="55dbe-117">Enthält die SMTP-Adresse für den Benutzer konfigurierten Nachricht Informationsspeicher für Öffentliche Ordner zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="55dbe-117">Contains the SMTP address assigned to the public folder message store configured for the user.</span></span> <span data-ttu-id="55dbe-118">Diese SMTP-Adresse kann zum Ermitteln der Öffentliche Ordner-Einstellungen im Element ["EmailAddress" (POX)](emailaddress-pox.md) einer Anforderung für die AutoErmittlung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="55dbe-118">This SMTP address can be used in the [EMailAddress (POX)](emailaddress-pox.md) element of an Autodiscover request to discover public folder settings.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="55dbe-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="55dbe-119">Parent elements</span></span>

|<span data-ttu-id="55dbe-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="55dbe-120">**Element**</span></span>|<span data-ttu-id="55dbe-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="55dbe-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="55dbe-122">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="55dbe-122">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="55dbe-123">Gibt die kontoeinstellungen für den Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="55dbe-123">Specifies account settings for the user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55dbe-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="55dbe-124">Remarks</span></span>

<span data-ttu-id="55dbe-125">Das **PublicFolderInformation** -Element ist ein optionales untergeordnetes Element des Elements **Konto** .</span><span class="sxs-lookup"><span data-stu-id="55dbe-125">The **PublicFolderInformation** element is an optional child element of the **Account** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="55dbe-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55dbe-126">See also</span></span>



[<span data-ttu-id="55dbe-127">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="55dbe-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

