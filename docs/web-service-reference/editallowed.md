---
title: EditAllowed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e63c4f7e-77c0-4826-b4e2-43b795d03914
description: Das EditAllowed-Element gibt an, ob die Verwaltung von Informationsrechten bearbeitet werden kann.
ms.openlocfilehash: 979fbaa9fcfbd1015468a8ae00628959bad0bf56
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463482"
---
# <a name="editallowed"></a><span data-ttu-id="3e0b5-103">EditAllowed</span><span class="sxs-lookup"><span data-stu-id="3e0b5-103">EditAllowed</span></span>

<span data-ttu-id="3e0b5-104">Das **EditAllowed** -Element gibt an, ob die Verwaltung von Informationsrechten bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3e0b5-104">The **EditAllowed** element specifies whether Information Rights Management can be edited.</span></span> 
  
```XML
<EditAllowed> true | false </EditAllowed>
```

 <span data-ttu-id="3e0b5-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="3e0b5-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3e0b5-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3e0b5-106">Attributes and elements</span></span>

<span data-ttu-id="3e0b5-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3e0b5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3e0b5-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3e0b5-108">Attributes</span></span>

<span data-ttu-id="3e0b5-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3e0b5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3e0b5-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3e0b5-110">Child elements</span></span>

<span data-ttu-id="3e0b5-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="3e0b5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3e0b5-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3e0b5-112">Parent elements</span></span>

|<span data-ttu-id="3e0b5-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3e0b5-113">**Element**</span></span>|<span data-ttu-id="3e0b5-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3e0b5-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3e0b5-115">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="3e0b5-115">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md) <br/> |<span data-ttu-id="3e0b5-116">Gibt Informationen zur Rechteverwaltungslizenz an.</span><span class="sxs-lookup"><span data-stu-id="3e0b5-116">Specifies information about the rights management license.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3e0b5-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="3e0b5-117">Text value</span></span>

<span data-ttu-id="3e0b5-118">Der Textwert **true** für das **EditAllowed** -Element gibt an, dass die Verwaltung von Informationsrechten (Information Rights Management, IRM) bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3e0b5-118">A text value of **true** for the **EditAllowed** element indicates that Information Rights Management (IRM) can be edited.</span></span> <span data-ttu-id="3e0b5-119">Der Wert **false** gibt an, dass IRM nicht bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3e0b5-119">A value of **false** indicates that IRM cannot be edited.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3e0b5-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e0b5-120">Remarks</span></span>

<span data-ttu-id="3e0b5-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3e0b5-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3e0b5-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3e0b5-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3e0b5-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3e0b5-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3e0b5-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="3e0b5-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3e0b5-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3e0b5-125">Schema Name</span></span>  <br/> |<span data-ttu-id="3e0b5-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="3e0b5-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="3e0b5-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3e0b5-127">Validation File</span></span>  <br/> |<span data-ttu-id="3e0b5-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="3e0b5-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="3e0b5-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="3e0b5-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="3e0b5-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e0b5-130">See also</span></span>



- [<span data-ttu-id="3e0b5-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3e0b5-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

