---
title: Elemente des Objekts (MemberListType)
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
description: Das Member-Element enthält eine Liste der Mitglieder für eine Verteilerliste.
ms.openlocfilehash: 8cf9ed7a64a908614ce7be30a9bef631739fcebf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830439"
---
# <a name="members-memberlisttype"></a><span data-ttu-id="42be7-103">Elemente des Objekts (MemberListType)</span><span class="sxs-lookup"><span data-stu-id="42be7-103">Members (MemberListType)</span></span>

<span data-ttu-id="42be7-104">Das **Member** -Element enthält eine Liste der Mitglieder für eine Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="42be7-104">The **Members** element provides the list of members for a distribution list.</span></span> 
  
```xml
<Members>
   <Member/>
</Members>
```

<span data-ttu-id="42be7-105">**MemberListType**</span><span class="sxs-lookup"><span data-stu-id="42be7-105">**MemberListType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="42be7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="42be7-106">Attributes and elements</span></span>

<span data-ttu-id="42be7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="42be7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="42be7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="42be7-108">Attributes</span></span>

<span data-ttu-id="42be7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="42be7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="42be7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="42be7-110">Child elements</span></span>

|<span data-ttu-id="42be7-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="42be7-111">**Element**</span></span>|<span data-ttu-id="42be7-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="42be7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="42be7-113">Member</span><span class="sxs-lookup"><span data-stu-id="42be7-113">Member</span></span>](member-ex15websvcsotherref.md) <br/> |<span data-ttu-id="42be7-114">Stellt einen Bezeichner für eine vollständig aufgelöster E-mail-Adresse und den Status der Adresse auf dem Server bereit.</span><span class="sxs-lookup"><span data-stu-id="42be7-114">Provides an identifier for a fully resolved e-mail address, and the status of that address on the server.</span></span> <span data-ttu-id="42be7-115">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="42be7-115">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="42be7-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="42be7-116">Parent elements</span></span>

|<span data-ttu-id="42be7-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="42be7-117">**Element**</span></span>|<span data-ttu-id="42be7-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="42be7-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="42be7-119">DistributionList</span><span class="sxs-lookup"><span data-stu-id="42be7-119">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="42be7-120">Stellt eine Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="42be7-120">Represents a distribution list.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="42be7-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="42be7-121">Remarks</span></span>

<span data-ttu-id="42be7-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="42be7-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="42be7-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="42be7-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="42be7-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="42be7-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="42be7-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="42be7-125">Schema Name</span></span>  <br/> |<span data-ttu-id="42be7-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="42be7-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="42be7-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="42be7-127">Validation File</span></span>  <br/> |<span data-ttu-id="42be7-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="42be7-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="42be7-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="42be7-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="42be7-130">False</span><span class="sxs-lookup"><span data-stu-id="42be7-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="42be7-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42be7-131">See also</span></span>

- [<span data-ttu-id="42be7-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="42be7-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

