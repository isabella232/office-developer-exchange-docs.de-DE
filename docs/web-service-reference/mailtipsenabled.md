---
title: MailTipsEnabled
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailTipsEnabled
api_type:
- schema
ms.assetid: 737388b3-7b73-42af-94d3-3dbb0659718f
description: Das MailTipsEnabled-Element gibt an, ob der Mail-Tipps-Dienst verfügbar ist.
ms.openlocfilehash: 6be923733f1cbd584010ce5f8ee5b96178d5c2c0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468012"
---
# <a name="mailtipsenabled"></a><span data-ttu-id="95b83-103">MailTipsEnabled</span><span class="sxs-lookup"><span data-stu-id="95b83-103">MailTipsEnabled</span></span>

<span data-ttu-id="95b83-104">Das **MailTipsEnabled** -Element gibt an, ob der Mail-Tipps-Dienst verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="95b83-104">The **MailTipsEnabled** element indicates whether the mail tips service is available.</span></span> 
  
```xml
<MailTipsEnabled>true | false</MailTipsEnabled>
```

 <span data-ttu-id="95b83-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="95b83-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="95b83-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="95b83-106">Attributes and elements</span></span>

<span data-ttu-id="95b83-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="95b83-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="95b83-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="95b83-108">Attributes</span></span>

<span data-ttu-id="95b83-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="95b83-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="95b83-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="95b83-110">Child elements</span></span>

<span data-ttu-id="95b83-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="95b83-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="95b83-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="95b83-112">Parent elements</span></span>

|<span data-ttu-id="95b83-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="95b83-113">**Element**</span></span>|<span data-ttu-id="95b83-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="95b83-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="95b83-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="95b83-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="95b83-116">Enthält Dienstkonfigurationsinformationen für den e-Mail-Spitzen Dienst.</span><span class="sxs-lookup"><span data-stu-id="95b83-116">Contains service configuration information for the mail tips service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="95b83-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="95b83-117">Text value</span></span>

<span data-ttu-id="95b83-118">Der Textwert dieses Elements ist **true** , wenn der e-Mail-Spitzen Dienst verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="95b83-118">The text value of this element is **true** if the mail tips service is available.</span></span> <span data-ttu-id="95b83-119">Der Wert ist **false** , wenn der e-Mail-Spitzen Dienst nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="95b83-119">The value is **false** if the mail tips service is not available.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="95b83-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95b83-120">Remarks</span></span>

<span data-ttu-id="95b83-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="95b83-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="95b83-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="95b83-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95b83-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="95b83-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="95b83-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="95b83-124">Schema Name</span></span>  <br/> |<span data-ttu-id="95b83-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="95b83-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="95b83-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="95b83-126">Validation File</span></span>  <br/> |<span data-ttu-id="95b83-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="95b83-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="95b83-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="95b83-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="95b83-129">False</span><span class="sxs-lookup"><span data-stu-id="95b83-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="95b83-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95b83-130">See also</span></span>



- [<span data-ttu-id="95b83-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="95b83-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

