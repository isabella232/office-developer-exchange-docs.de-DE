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
ms.openlocfilehash: addb86ece2be3091ac55a52ee2f16f5c5f72ae41
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829958"
---
# <a name="invalidrecipient-mailtips"></a><span data-ttu-id="eff27-103">InvalidRecipient (e-Mail-Infos)</span><span class="sxs-lookup"><span data-stu-id="eff27-103">InvalidRecipient (MailTips)</span></span>

<span data-ttu-id="eff27-104">Das **InvalidRecipient** -Element gibt an, ob der Empfänger ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="eff27-104">The **InvalidRecipient** element indicates whether the recipient is invalid.</span></span> 
  
```XML
<InvalidRecipient>true | false</InvalidRecipient>
```

 <span data-ttu-id="eff27-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="eff27-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eff27-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="eff27-106">Attributes and elements</span></span>

<span data-ttu-id="eff27-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="eff27-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eff27-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="eff27-108">Attributes</span></span>

<span data-ttu-id="eff27-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="eff27-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eff27-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="eff27-110">Child elements</span></span>

<span data-ttu-id="eff27-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="eff27-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="eff27-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="eff27-112">Parent elements</span></span>

|<span data-ttu-id="eff27-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="eff27-113">**Element**</span></span>|<span data-ttu-id="eff27-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="eff27-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eff27-115">E-Mail-Infos</span><span class="sxs-lookup"><span data-stu-id="eff27-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="eff27-116">Stellt Werte für verschiedene Arten von e-Mail-Infos.</span><span class="sxs-lookup"><span data-stu-id="eff27-116">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="eff27-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="eff27-117">Text value</span></span>

<span data-ttu-id="eff27-118">Der Textwert der dieses Element ist **true** , wenn der Empfänger ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="eff27-118">The text value of this element is **true** if the recipient is invalid.</span></span> <span data-ttu-id="eff27-119">Der Wert ist **false** , wenn der Empfänger nicht ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="eff27-119">The value is **false** if the recipient is not invalid.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="eff27-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="eff27-120">Remarks</span></span>

<span data-ttu-id="eff27-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="eff27-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eff27-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="eff27-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eff27-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="eff27-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="eff27-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="eff27-124">Schema Name</span></span>  <br/> |<span data-ttu-id="eff27-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="eff27-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="eff27-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="eff27-126">Validation File</span></span>  <br/> |<span data-ttu-id="eff27-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="eff27-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="eff27-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="eff27-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="eff27-129">False</span><span class="sxs-lookup"><span data-stu-id="eff27-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eff27-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eff27-130">See also</span></span>



- [<span data-ttu-id="eff27-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="eff27-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

