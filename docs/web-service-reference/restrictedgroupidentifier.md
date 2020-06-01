---
title: RestrictedGroupIdentifier
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RestrictedGroupIdentifier
api_type:
- schema
ms.assetid: a3ea3c81-9f99-4836-8cb4-2384ea63f093
description: Das RestrictGroupIdentifier-Element stellt die Gruppen-Sicherheits-ID (SID) und die Attribute für eine eingeschränkte Gruppe innerhalb eines Benutzertokens dar.
ms.openlocfilehash: c95af4e09324e96f4551a05490dc200aec0cbd46
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465366"
---
# <a name="restrictedgroupidentifier"></a><span data-ttu-id="a3ea9-103">RestrictedGroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="a3ea9-103">RestrictedGroupIdentifier</span></span>

<span data-ttu-id="a3ea9-104">Das **RestrictGroupIdentifier** -Element stellt die Gruppen-Sicherheits-ID (SID) und die Attribute für eine eingeschränkte Gruppe innerhalb eines Benutzertokens dar.</span><span class="sxs-lookup"><span data-stu-id="a3ea9-104">The **RestrictGroupIdentifier** element represents the group security identifier (SID) and attributes for a restricted group within a user token.</span></span> 
  
```xml
<RestrictedGroupIdentifier Attributes="">
   <SecurityIdentifier/>
</RestrictedGroupIdentifier>
```

 <span data-ttu-id="a3ea9-105">**SidAndAttributesType**</span><span class="sxs-lookup"><span data-stu-id="a3ea9-105">**SidAndAttributesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a3ea9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a3ea9-106">Attributes and elements</span></span>

<span data-ttu-id="a3ea9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a3ea9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a3ea9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a3ea9-108">Attributes</span></span>

|<span data-ttu-id="a3ea9-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a3ea9-109">**Attribute**</span></span>|<span data-ttu-id="a3ea9-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a3ea9-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a3ea9-111">**Attributes**</span><span class="sxs-lookup"><span data-stu-id="a3ea9-111">**Attributes**</span></span> <br/> |<span data-ttu-id="a3ea9-112">Enthält Gruppenattribute.</span><span class="sxs-lookup"><span data-stu-id="a3ea9-112">Contains group attributes.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a3ea9-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a3ea9-113">Child elements</span></span>

|<span data-ttu-id="a3ea9-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="a3ea9-114">**Element**</span></span>|<span data-ttu-id="a3ea9-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a3ea9-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a3ea9-116">SecurityIdentifier</span><span class="sxs-lookup"><span data-stu-id="a3ea9-116">SecurityIdentifier</span></span>](securityidentifier.md) <br/> |<span data-ttu-id="a3ea9-117">Stellt das SDDL-Formular (Security Descriptor Definition Language) einer Sicherheits-ID dar.</span><span class="sxs-lookup"><span data-stu-id="a3ea9-117">Represents the security descriptor definition language (SDDL) form of a security identifier.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a3ea9-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a3ea9-118">Parent elements</span></span>

|<span data-ttu-id="a3ea9-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="a3ea9-119">**Element**</span></span>|<span data-ttu-id="a3ea9-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a3ea9-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a3ea9-121">RestrictedGroupSids</span><span class="sxs-lookup"><span data-stu-id="a3ea9-121">RestrictedGroupSids</span></span>](restrictedgroupsids.md) <br/> |<span data-ttu-id="a3ea9-122">Stellt eine Auflistung von eingeschränkten Gruppen in einem Benutzertoken dar.</span><span class="sxs-lookup"><span data-stu-id="a3ea9-122">Represents a collection of restricted groups within a user token.</span></span> <span data-ttu-id="a3ea9-123">Die Serialisierung von Token wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a3ea9-123">Token serialization is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a3ea9-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3ea9-124">Remarks</span></span>

<span data-ttu-id="a3ea9-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="a3ea9-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a3ea9-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a3ea9-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a3ea9-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="a3ea9-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a3ea9-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a3ea9-128">Schema Name</span></span>  <br/> |<span data-ttu-id="a3ea9-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="a3ea9-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="a3ea9-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a3ea9-130">Validation File</span></span>  <br/> |<span data-ttu-id="a3ea9-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a3ea9-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a3ea9-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a3ea9-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="a3ea9-133">False</span><span class="sxs-lookup"><span data-stu-id="a3ea9-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a3ea9-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3ea9-134">See also</span></span>



- [<span data-ttu-id="a3ea9-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a3ea9-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

