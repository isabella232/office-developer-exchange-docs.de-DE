---
title: DisableApp
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 42d2a888-fa62-4970-8306-9ddde4eeb1f0
description: Das DisableApp-Element gibt eine Anforderung an eine app zu deaktivieren.
ms.openlocfilehash: d6d895d98fb368a6912f9111a4b934ba9631268e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757996"
---
# <a name="disableapp"></a><span data-ttu-id="01907-103">DisableApp</span><span class="sxs-lookup"><span data-stu-id="01907-103">DisableApp</span></span>

<span data-ttu-id="01907-104">Das **DisableApp** -Element gibt eine Anforderung an eine app zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="01907-104">The **DisableApp** element specifies a request to disable an app.</span></span> 
  
```XML
<DisableApp>
    <ID></ID>
    <DisableReason></DisableReason>
</DisableApp>
```

 <span data-ttu-id="01907-105">**DisableAppType**</span><span class="sxs-lookup"><span data-stu-id="01907-105">**DisableAppType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="01907-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="01907-106">Attributes and elements</span></span>

<span data-ttu-id="01907-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="01907-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="01907-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="01907-108">Attributes</span></span>

<span data-ttu-id="01907-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="01907-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="01907-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="01907-110">Child elements</span></span>

|<span data-ttu-id="01907-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="01907-111">**Element**</span></span>|<span data-ttu-id="01907-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="01907-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="01907-113">ID (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="01907-113">ID (String)</span></span>](id-string.md) <br/> |<span data-ttu-id="01907-114">Gibt die ID eines Elements.</span><span class="sxs-lookup"><span data-stu-id="01907-114">Specifies the identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="01907-115">DisableReason</span><span class="sxs-lookup"><span data-stu-id="01907-115">DisableReason</span></span>](disablereason.md) <br/> |<span data-ttu-id="01907-116">Gibt den Grund für die Deaktivierung einer app.</span><span class="sxs-lookup"><span data-stu-id="01907-116">Specifies the reason for disabling an app.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="01907-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="01907-117">Parent elements</span></span>

<span data-ttu-id="01907-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="01907-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="01907-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="01907-119">Remarks</span></span>

<span data-ttu-id="01907-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="01907-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="01907-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="01907-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="01907-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="01907-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="01907-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="01907-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="01907-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="01907-124">Schema Name</span></span>  <br/> |<span data-ttu-id="01907-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="01907-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="01907-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="01907-126">Validation File</span></span>  <br/> |<span data-ttu-id="01907-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="01907-127">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="01907-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="01907-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="01907-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01907-129">See also</span></span>

- [<span data-ttu-id="01907-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="01907-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

