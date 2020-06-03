---
title: LargeAudienceThreshold
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- LargeAudienceThreshold
api_type:
- schema
ms.assetid: dacd9db7-b8f0-445d-a3d1-3356b8c2bcd1
description: Das LargeAudienceThreshold-Element stellt den Schwellenwert für hohe Benutzergruppen für einen Client dar.
ms.openlocfilehash: 6d85f9eaf8b7723713877d376876461befa92324
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466388"
---
# <a name="largeaudiencethreshold"></a><span data-ttu-id="5e12c-103">LargeAudienceThreshold</span><span class="sxs-lookup"><span data-stu-id="5e12c-103">LargeAudienceThreshold</span></span>

<span data-ttu-id="5e12c-104">Das **LargeAudienceThreshold** -Element stellt den Schwellenwert für hohe Benutzergruppen für einen Client dar.</span><span class="sxs-lookup"><span data-stu-id="5e12c-104">The **LargeAudienceThreshold** element represents the large audience threshold for a client.</span></span> 
  
```XML
<LargeAudienceThreshold/>
```

 <span data-ttu-id="5e12c-105">**int**</span><span class="sxs-lookup"><span data-stu-id="5e12c-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5e12c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5e12c-106">Attributes and elements</span></span>

<span data-ttu-id="5e12c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5e12c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5e12c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5e12c-108">Attributes</span></span>

<span data-ttu-id="5e12c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5e12c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5e12c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5e12c-110">Child elements</span></span>

<span data-ttu-id="5e12c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="5e12c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5e12c-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5e12c-112">Parent elements</span></span>

|<span data-ttu-id="5e12c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5e12c-113">**Element**</span></span>|<span data-ttu-id="5e12c-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5e12c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5e12c-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="5e12c-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="5e12c-116">Enthält Dienstkonfigurationsinformationen für den e-Mail-Spitzen Dienst.</span><span class="sxs-lookup"><span data-stu-id="5e12c-116">Contains service configuration information for the mail tips service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5e12c-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="5e12c-117">Text value</span></span>

<span data-ttu-id="5e12c-118">Der Textwert ist eine ganze Zahl, die den Schwellenwert für die Benutzergruppe darstellt, der angibt, dass die Nachricht an mehr als eine Person geht.</span><span class="sxs-lookup"><span data-stu-id="5e12c-118">The text value is an integer that represents the audience threshold that indicates that the message is going to more than one person.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5e12c-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e12c-119">Remarks</span></span>

<span data-ttu-id="5e12c-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="5e12c-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5e12c-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="5e12c-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5e12c-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="5e12c-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5e12c-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5e12c-123">Schema Name</span></span>  <br/> |<span data-ttu-id="5e12c-124">Schematypen</span><span class="sxs-lookup"><span data-stu-id="5e12c-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="5e12c-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5e12c-125">Validation File</span></span>  <br/> |<span data-ttu-id="5e12c-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5e12c-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5e12c-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5e12c-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="5e12c-128">False</span><span class="sxs-lookup"><span data-stu-id="5e12c-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5e12c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e12c-129">See also</span></span>



- [<span data-ttu-id="5e12c-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5e12c-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

