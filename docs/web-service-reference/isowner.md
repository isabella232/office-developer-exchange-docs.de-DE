---
title: IsOwner
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ea0f0afc-32fe-46cb-8530-62a6ce9490f6
description: Das IsOwner-Element gibt an, ob der angegebene e-Mail-Benutzer den Besitzer ist.
ms.openlocfilehash: aac3c2a599093282542025468d73c55ec4569e29
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830080"
---
# <a name="isowner"></a><span data-ttu-id="56960-103">IsOwner</span><span class="sxs-lookup"><span data-stu-id="56960-103">IsOwner</span></span>

<span data-ttu-id="56960-104">Das **IsOwner** -Element gibt an, ob der angegebene e-Mail-Benutzer den Besitzer ist.</span><span class="sxs-lookup"><span data-stu-id="56960-104">The **IsOwner** element specifies whether the specified email user is the owner.</span></span> 
  
```XML
<IsOwner>true | false</IsOwner>
```

 <span data-ttu-id="56960-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="56960-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="56960-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="56960-106">Attributes and elements</span></span>

<span data-ttu-id="56960-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="56960-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="56960-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="56960-108">Attributes</span></span>

<span data-ttu-id="56960-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="56960-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="56960-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="56960-110">Child elements</span></span>

<span data-ttu-id="56960-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="56960-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="56960-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="56960-112">Parent elements</span></span>

|<span data-ttu-id="56960-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="56960-113">**Element**</span></span>|<span data-ttu-id="56960-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="56960-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="56960-115">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="56960-115">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md) <br/> |<span data-ttu-id="56960-116">Gibt Informationen zu den Rights Management-Lizenz.</span><span class="sxs-lookup"><span data-stu-id="56960-116">Specifies information about the rights management license.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="56960-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="56960-117">Text value</span></span>

<span data-ttu-id="56960-118">Der Textwert **true** für das **IsOwner** -Element gibt an, dass der Benutzer den Besitzer der Rechte für ein Element ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="56960-118">A text value of **true** for the **IsOwner** element indicates that the user is the owner of rights issued on an item.</span></span> <span data-ttu-id="56960-119">Der Wert **false** gibt an, dass der Benutzer nicht der Besitzer der Rechte für ein Element ausgestellt ist.</span><span class="sxs-lookup"><span data-stu-id="56960-119">A value of **false** indicates that the user is not the owner of rights issued on an item.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="56960-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="56960-120">Remarks</span></span>

<span data-ttu-id="56960-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="56960-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="56960-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="56960-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="56960-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="56960-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="56960-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="56960-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="56960-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="56960-125">Schema Name</span></span>  <br/> |<span data-ttu-id="56960-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="56960-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="56960-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="56960-127">Validation File</span></span>  <br/> |<span data-ttu-id="56960-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="56960-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="56960-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="56960-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="56960-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56960-130">See also</span></span>



- [<span data-ttu-id="56960-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="56960-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

