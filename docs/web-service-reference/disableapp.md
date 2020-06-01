---
title: DisableApp
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 42d2a888-fa62-4970-8306-9ddde4eeb1f0
description: Das DisableApp-Element gibt eine Anforderung zum Deaktivieren einer APP an.
ms.openlocfilehash: e99464677dc34e011e45548083fb830b819649fa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457823"
---
# <a name="disableapp"></a><span data-ttu-id="4794c-103">DisableApp</span><span class="sxs-lookup"><span data-stu-id="4794c-103">DisableApp</span></span>

<span data-ttu-id="4794c-104">Das **DisableApp** -Element gibt eine Anforderung zum Deaktivieren einer APP an.</span><span class="sxs-lookup"><span data-stu-id="4794c-104">The **DisableApp** element specifies a request to disable an app.</span></span> 
  
```XML
<DisableApp>
    <ID></ID>
    <DisableReason></DisableReason>
</DisableApp>
```

 <span data-ttu-id="4794c-105">**DisableAppType**</span><span class="sxs-lookup"><span data-stu-id="4794c-105">**DisableAppType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4794c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4794c-106">Attributes and elements</span></span>

<span data-ttu-id="4794c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4794c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4794c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4794c-108">Attributes</span></span>

<span data-ttu-id="4794c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4794c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4794c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4794c-110">Child elements</span></span>

|<span data-ttu-id="4794c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4794c-111">**Element**</span></span>|<span data-ttu-id="4794c-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4794c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4794c-113">ID (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="4794c-113">ID (String)</span></span>](id-string.md) <br/> |<span data-ttu-id="4794c-114">Gibt den Bezeichner eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="4794c-114">Specifies the identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="4794c-115">DisableReason</span><span class="sxs-lookup"><span data-stu-id="4794c-115">DisableReason</span></span>](disablereason.md) <br/> |<span data-ttu-id="4794c-116">Gibt den Grund für das Deaktivieren einer APP an.</span><span class="sxs-lookup"><span data-stu-id="4794c-116">Specifies the reason for disabling an app.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4794c-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4794c-117">Parent elements</span></span>

<span data-ttu-id="4794c-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="4794c-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4794c-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4794c-119">Remarks</span></span>

<span data-ttu-id="4794c-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4794c-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="4794c-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4794c-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4794c-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4794c-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4794c-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="4794c-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4794c-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4794c-124">Schema Name</span></span>  <br/> |<span data-ttu-id="4794c-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="4794c-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="4794c-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4794c-126">Validation File</span></span>  <br/> |<span data-ttu-id="4794c-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="4794c-127">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4794c-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="4794c-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="4794c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4794c-129">See also</span></span>

- [<span data-ttu-id="4794c-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4794c-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

