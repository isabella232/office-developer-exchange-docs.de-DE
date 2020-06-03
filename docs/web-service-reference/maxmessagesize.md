---
title: MaxMessageSize
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MaxMessageSize
api_type:
- schema
ms.assetid: bb98ac72-9409-4332-81bb-ee3bebb9a00e
description: Das MaxMessageSize-Element stellt die maximale Nachrichtengröße dar, die ein Empfänger annehmen kann.
ms.openlocfilehash: 727eed38a129800b7d38aa49c41cdacfa13e7a36
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468411"
---
# <a name="maxmessagesize"></a><span data-ttu-id="69497-103">MaxMessageSize</span><span class="sxs-lookup"><span data-stu-id="69497-103">MaxMessageSize</span></span>

<span data-ttu-id="69497-104">Das **MaxMessageSize** -Element stellt die maximale Nachrichtengröße dar, die ein Empfänger annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="69497-104">The **MaxMessageSize** element represents the maximum message size a recipient can accept.</span></span> 
  
```XML
<MaxMessageSize/>
```

 <span data-ttu-id="69497-105">**int**</span><span class="sxs-lookup"><span data-stu-id="69497-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="69497-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="69497-106">Attributes and elements</span></span>

<span data-ttu-id="69497-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="69497-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="69497-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="69497-108">Attributes</span></span>

<span data-ttu-id="69497-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="69497-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="69497-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="69497-110">Child elements</span></span>

<span data-ttu-id="69497-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="69497-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="69497-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="69497-112">Parent elements</span></span>

|<span data-ttu-id="69497-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="69497-113">**Element**</span></span>|<span data-ttu-id="69497-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="69497-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="69497-115">E-Mail-Info</span><span class="sxs-lookup"><span data-stu-id="69497-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="69497-116">Stellt Werte für verschiedene Arten von e-Mail-Tipps dar.</span><span class="sxs-lookup"><span data-stu-id="69497-116">Represents values for various types of mail tips.</span></span>  <br/> |
|[<span data-ttu-id="69497-117">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="69497-117">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="69497-118">Enthält Dienstkonfigurationsinformationen für den e-Mail-Spitzen Dienst.</span><span class="sxs-lookup"><span data-stu-id="69497-118">Contains service configuration information for the mail tips service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="69497-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="69497-119">Text value</span></span>

<span data-ttu-id="69497-120">Der Textwert ist eine ganze Zahl, die die maximale Nachrichtengröße darstellt, die ein Empfänger annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="69497-120">The text value is an integer that represents the maximum message size a recipient can accept.</span></span> <span data-ttu-id="69497-121">Dieser Wert kann in Kilobyte oder Megabyte gemessen werden.</span><span class="sxs-lookup"><span data-stu-id="69497-121">This value can be measured in kilobytes or megabytes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="69497-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69497-122">Remarks</span></span>

<span data-ttu-id="69497-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="69497-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="69497-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="69497-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="69497-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="69497-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="69497-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="69497-126">Schema Name</span></span>  <br/> |<span data-ttu-id="69497-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="69497-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="69497-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="69497-128">Validation File</span></span>  <br/> |<span data-ttu-id="69497-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="69497-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="69497-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="69497-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="69497-131">False</span><span class="sxs-lookup"><span data-stu-id="69497-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="69497-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69497-132">See also</span></span>



- [<span data-ttu-id="69497-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="69497-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

