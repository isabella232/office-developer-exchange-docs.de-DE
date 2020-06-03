---
title: InvalidRecipient (e-Mail-Infos)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InvalidRecipient
api_type:
- schema
ms.assetid: 48959a99-bb0d-4004-963e-5a5baaa96476
description: Das InvalidRecipient-Element gibt an, ob der Empfänger ungültig ist.
ms.openlocfilehash: fddd75beb2228c50084bd38b4f4745064cc281dc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530002"
---
# <a name="invalidrecipient-mailtips"></a><span data-ttu-id="f9414-103">InvalidRecipient (e-Mail-Infos)</span><span class="sxs-lookup"><span data-stu-id="f9414-103">InvalidRecipient (MailTips)</span></span>

<span data-ttu-id="f9414-104">Das **InvalidRecipient** -Element gibt an, ob der Empfänger ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="f9414-104">The **InvalidRecipient** element indicates whether the recipient is invalid.</span></span> 
  
```XML
<InvalidRecipient>true | false</InvalidRecipient>
```

 <span data-ttu-id="f9414-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="f9414-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f9414-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f9414-106">Attributes and elements</span></span>

<span data-ttu-id="f9414-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f9414-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f9414-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f9414-108">Attributes</span></span>

<span data-ttu-id="f9414-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f9414-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f9414-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f9414-110">Child elements</span></span>

<span data-ttu-id="f9414-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="f9414-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f9414-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f9414-112">Parent elements</span></span>

|<span data-ttu-id="f9414-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f9414-113">**Element**</span></span>|<span data-ttu-id="f9414-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f9414-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f9414-115">E-Mail-Info</span><span class="sxs-lookup"><span data-stu-id="f9414-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="f9414-116">Stellt Werte für verschiedene Arten von e-Mail-Tipps dar.</span><span class="sxs-lookup"><span data-stu-id="f9414-116">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f9414-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="f9414-117">Text value</span></span>

<span data-ttu-id="f9414-118">Der Textwert dieses Elements ist **true** , wenn der Empfänger ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="f9414-118">The text value of this element is **true** if the recipient is invalid.</span></span> <span data-ttu-id="f9414-119">Der Wert ist **false** , wenn der Empfänger nicht ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="f9414-119">The value is **false** if the recipient is not invalid.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f9414-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9414-120">Remarks</span></span>

<span data-ttu-id="f9414-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f9414-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f9414-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f9414-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f9414-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="f9414-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f9414-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f9414-124">Schema Name</span></span>  <br/> |<span data-ttu-id="f9414-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f9414-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="f9414-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f9414-126">Validation File</span></span>  <br/> |<span data-ttu-id="f9414-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f9414-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f9414-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f9414-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="f9414-129">False</span><span class="sxs-lookup"><span data-stu-id="f9414-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f9414-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9414-130">See also</span></span>



- [<span data-ttu-id="f9414-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f9414-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

