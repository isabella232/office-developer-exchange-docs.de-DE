---
title: Members (MemberListType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Members
api_type:
- schema
ms.assetid: cbd38049-2ef7-40bf-9bec-0469af0f58ec
description: Das Members-Element stellt die Liste der Mitglieder für eine Verteilerliste bereit.
ms.openlocfilehash: 2cdfb81dfbc223db365d49ed44d4893339eb4653
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462430"
---
# <a name="members-memberlisttype"></a><span data-ttu-id="bc21e-103">Members (MemberListType)</span><span class="sxs-lookup"><span data-stu-id="bc21e-103">Members (MemberListType)</span></span>

<span data-ttu-id="bc21e-104">Das **Members** -Element stellt die Liste der Mitglieder für eine Verteilerliste bereit.</span><span class="sxs-lookup"><span data-stu-id="bc21e-104">The **Members** element provides the list of members for a distribution list.</span></span> 
  
```xml
<Members>
   <Member/>
</Members>
```

<span data-ttu-id="bc21e-105">**MemberListType**</span><span class="sxs-lookup"><span data-stu-id="bc21e-105">**MemberListType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="bc21e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bc21e-106">Attributes and elements</span></span>

<span data-ttu-id="bc21e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bc21e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bc21e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="bc21e-108">Attributes</span></span>

<span data-ttu-id="bc21e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="bc21e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bc21e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bc21e-110">Child elements</span></span>

|<span data-ttu-id="bc21e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="bc21e-111">**Element**</span></span>|<span data-ttu-id="bc21e-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bc21e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bc21e-113">Element</span><span class="sxs-lookup"><span data-stu-id="bc21e-113">Member</span></span>](member-ex15websvcsotherref.md) <br/> |<span data-ttu-id="bc21e-114">Stellt einen Bezeichner für eine vollständig aufgelöste e-Mail-Adresse und den Status dieser Adresse auf dem Server bereit.</span><span class="sxs-lookup"><span data-stu-id="bc21e-114">Provides an identifier for a fully resolved e-mail address, and the status of that address on the server.</span></span> <span data-ttu-id="bc21e-115">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="bc21e-115">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bc21e-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bc21e-116">Parent elements</span></span>

|<span data-ttu-id="bc21e-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="bc21e-117">**Element**</span></span>|<span data-ttu-id="bc21e-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bc21e-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bc21e-119">DistributionList</span><span class="sxs-lookup"><span data-stu-id="bc21e-119">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="bc21e-120">Stellt eine Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="bc21e-120">Represents a distribution list.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc21e-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc21e-121">Remarks</span></span>

<span data-ttu-id="bc21e-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="bc21e-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bc21e-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="bc21e-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bc21e-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="bc21e-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bc21e-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="bc21e-125">Schema Name</span></span>  <br/> |<span data-ttu-id="bc21e-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="bc21e-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="bc21e-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="bc21e-127">Validation File</span></span>  <br/> |<span data-ttu-id="bc21e-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bc21e-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bc21e-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="bc21e-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="bc21e-130">False</span><span class="sxs-lookup"><span data-stu-id="bc21e-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bc21e-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc21e-131">See also</span></span>

- [<span data-ttu-id="bc21e-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="bc21e-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

