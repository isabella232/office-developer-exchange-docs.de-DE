---
title: PublicFolderInformation (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a221aa9e-b4ac-4ec5-aa42-7e2a69e8eaa6
description: Das PublicFolderInformation-Element enthält Informationen, die Clients verwenden können, um eine Auto Ermittlungsanforderung zu senden, um Informationen zu öffentlichen Ordnern für den Benutzer zu ermitteln.
ms.openlocfilehash: e044a1feddfaeb4eb93c289c617dde9adc66f332
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457718"
---
# <a name="publicfolderinformation-pox"></a><span data-ttu-id="8c0a0-103">PublicFolderInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="8c0a0-103">PublicFolderInformation (POX)</span></span>

<span data-ttu-id="8c0a0-104">Das **PublicFolderInformation** -Element enthält Informationen, die Clients verwenden können, um eine Auto Ermittlungsanforderung zu senden, um Informationen zu öffentlichen Ordnern für den Benutzer zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="8c0a0-104">The **PublicFolderInformation** element contains information that clients can use to send an Autodiscover request to discover public folder information for the user.</span></span> 
  
[<span data-ttu-id="8c0a0-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="8c0a0-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="8c0a0-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="8c0a0-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="8c0a0-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="8c0a0-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="8c0a0-108">PublicFolderInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="8c0a0-108">PublicFolderInformation (POX)</span></span>](publicfolderinformation-pox.md)
  
```XML
<PublicFolderInformation>
   <SmtpAddress/>
</PublicFolderInformation>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="8c0a0-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8c0a0-109">Attributes and elements</span></span>

<span data-ttu-id="8c0a0-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8c0a0-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8c0a0-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="8c0a0-111">Attributes</span></span>

<span data-ttu-id="8c0a0-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="8c0a0-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8c0a0-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8c0a0-113">Child elements</span></span>

|<span data-ttu-id="8c0a0-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="8c0a0-114">**Element**</span></span>|<span data-ttu-id="8c0a0-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8c0a0-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c0a0-116">SmtpAddress (POX)</span><span class="sxs-lookup"><span data-stu-id="8c0a0-116">SmtpAddress (POX)</span></span>](smtpaddress-pox.md) <br/> |<span data-ttu-id="8c0a0-117">Enthält die SMTP-Adresse, die dem Nachrichtenspeicher für Öffentliche Ordner zugewiesen ist, der für den Benutzer konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="8c0a0-117">Contains the SMTP address assigned to the public folder message store configured for the user.</span></span> <span data-ttu-id="8c0a0-118">Diese SMTP-Adresse kann im [Pocken Element (POX)](emailaddress-pox.md) einer Auto Ermittlungsanforderung verwendet werden, um Einstellungen für Öffentliche Ordner zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="8c0a0-118">This SMTP address can be used in the [EMailAddress (POX)](emailaddress-pox.md) element of an Autodiscover request to discover public folder settings.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8c0a0-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8c0a0-119">Parent elements</span></span>

|<span data-ttu-id="8c0a0-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="8c0a0-120">**Element**</span></span>|<span data-ttu-id="8c0a0-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8c0a0-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c0a0-122">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="8c0a0-122">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="8c0a0-123">Gibt Kontoeinstellungen für den Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="8c0a0-123">Specifies account settings for the user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c0a0-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c0a0-124">Remarks</span></span>

<span data-ttu-id="8c0a0-125">Das **PublicFolderInformation** -Element ist ein optionales untergeordnetes Element des **Account** -Elements.</span><span class="sxs-lookup"><span data-stu-id="8c0a0-125">The **PublicFolderInformation** element is an optional child element of the **Account** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8c0a0-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c0a0-126">See also</span></span>



[<span data-ttu-id="8c0a0-127">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="8c0a0-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

