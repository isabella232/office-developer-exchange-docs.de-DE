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
ms.openlocfilehash: 48c7d751c018bf5702b05b41eeaa7ad350189e3a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758134"
---
# <a name="editallowed"></a><span data-ttu-id="1f231-103">EditAllowed</span><span class="sxs-lookup"><span data-stu-id="1f231-103">EditAllowed</span></span>

<span data-ttu-id="1f231-104">Das **EditAllowed** -Element gibt an, ob die Verwaltung von Informationsrechten bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1f231-104">The **EditAllowed** element specifies whether Information Rights Management can be edited.</span></span> 
  
```XML
<EditAllowed> true | false </EditAllowed>
```

 <span data-ttu-id="1f231-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="1f231-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1f231-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1f231-106">Attributes and elements</span></span>

<span data-ttu-id="1f231-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1f231-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1f231-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1f231-108">Attributes</span></span>

<span data-ttu-id="1f231-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1f231-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1f231-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1f231-110">Child elements</span></span>

<span data-ttu-id="1f231-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="1f231-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1f231-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1f231-112">Parent elements</span></span>

|<span data-ttu-id="1f231-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1f231-113">**Element**</span></span>|<span data-ttu-id="1f231-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1f231-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1f231-115">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="1f231-115">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md) <br/> |<span data-ttu-id="1f231-116">Gibt Informationen zu den Rights Management-Lizenz.</span><span class="sxs-lookup"><span data-stu-id="1f231-116">Specifies information about the rights management license.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1f231-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="1f231-117">Text value</span></span>

<span data-ttu-id="1f231-118">Der Textwert **true** für das **EditAllowed** -Element gibt an, dass (Information Rights Management, IRM) bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1f231-118">A text value of **true** for the **EditAllowed** element indicates that Information Rights Management (IRM) can be edited.</span></span> <span data-ttu-id="1f231-119">Der Wert **false** gibt an, dass IRM nicht bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1f231-119">A value of **false** indicates that IRM cannot be edited.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1f231-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1f231-120">Remarks</span></span>

<span data-ttu-id="1f231-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1f231-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1f231-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1f231-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1f231-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1f231-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1f231-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="1f231-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1f231-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1f231-125">Schema Name</span></span>  <br/> |<span data-ttu-id="1f231-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="1f231-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="1f231-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1f231-127">Validation File</span></span>  <br/> |<span data-ttu-id="1f231-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1f231-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="1f231-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="1f231-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="1f231-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f231-130">See also</span></span>



- [<span data-ttu-id="1f231-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1f231-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

