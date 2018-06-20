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
description: Das Element RestrictGroupIdentifier stellt die Gruppe Sicherheits-ID (SID) und Attribute für eine eingeschränkte Gruppe innerhalb einer Benutzertoken.
ms.openlocfilehash: c6db8672b2afa855e83f2e9a2bf84c9ff33bdc7a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831206"
---
# <a name="restrictedgroupidentifier"></a><span data-ttu-id="9b877-103">RestrictedGroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="9b877-103">RestrictedGroupIdentifier</span></span>

<span data-ttu-id="9b877-104">Das Element **RestrictGroupIdentifier** stellt die Gruppe Sicherheits-ID (SID) und Attribute für eine eingeschränkte Gruppe innerhalb einer Benutzertoken.</span><span class="sxs-lookup"><span data-stu-id="9b877-104">The **RestrictGroupIdentifier** element represents the group security identifier (SID) and attributes for a restricted group within a user token.</span></span> 
  
```xml
<RestrictedGroupIdentifier Attributes="">
   <SecurityIdentifier/>
</RestrictedGroupIdentifier>
```

 <span data-ttu-id="9b877-105">**SidAndAttributesType**</span><span class="sxs-lookup"><span data-stu-id="9b877-105">**SidAndAttributesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9b877-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9b877-106">Attributes and elements</span></span>

<span data-ttu-id="9b877-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9b877-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9b877-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9b877-108">Attributes</span></span>

|<span data-ttu-id="9b877-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9b877-109">**Attribute**</span></span>|<span data-ttu-id="9b877-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9b877-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9b877-111">**Attributes**</span><span class="sxs-lookup"><span data-stu-id="9b877-111">**Attributes**</span></span> <br/> |<span data-ttu-id="9b877-112">Enthält Gruppenattribute, die an.</span><span class="sxs-lookup"><span data-stu-id="9b877-112">Contains group attributes.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9b877-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9b877-113">Child elements</span></span>

|<span data-ttu-id="9b877-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="9b877-114">**Element**</span></span>|<span data-ttu-id="9b877-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9b877-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9b877-116">SecurityIdentifier</span><span class="sxs-lookup"><span data-stu-id="9b877-116">SecurityIdentifier</span></span>](securityidentifier.md) <br/> |<span data-ttu-id="9b877-117">Security Descriptor Definition Language (SDDL) Form von Sicherheits-ID darstellt.</span><span class="sxs-lookup"><span data-stu-id="9b877-117">Represents the security descriptor definition language (SDDL) form of a security identifier.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9b877-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9b877-118">Parent elements</span></span>

|<span data-ttu-id="9b877-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="9b877-119">**Element**</span></span>|<span data-ttu-id="9b877-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9b877-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9b877-121">RestrictedGroupSids</span><span class="sxs-lookup"><span data-stu-id="9b877-121">RestrictedGroupSids</span></span>](restrictedgroupsids.md) <br/> |<span data-ttu-id="9b877-122">Stellt eine Auflistung von eingeschränkte Gruppen innerhalb einer Benutzertoken dar.</span><span class="sxs-lookup"><span data-stu-id="9b877-122">Represents a collection of restricted groups within a user token.</span></span> <span data-ttu-id="9b877-123">Tokenserialisierung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9b877-123">Token serialization is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b877-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9b877-124">Remarks</span></span>

<span data-ttu-id="9b877-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="9b877-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9b877-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9b877-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9b877-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="9b877-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9b877-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9b877-128">Schema Name</span></span>  <br/> |<span data-ttu-id="9b877-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="9b877-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="9b877-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9b877-130">Validation File</span></span>  <br/> |<span data-ttu-id="9b877-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9b877-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9b877-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9b877-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="9b877-133">False</span><span class="sxs-lookup"><span data-stu-id="9b877-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9b877-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b877-134">See also</span></span>



- [<span data-ttu-id="9b877-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9b877-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

