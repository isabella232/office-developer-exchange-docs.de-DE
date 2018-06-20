---
title: GroupIdentifier
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupIdentifier
api_type:
- schema
ms.assetid: bdc6fc1e-4979-42da-a35b-e3017988c7d3
description: Das Element GroupIdentifier stellt eine einzelne Sicherheits-ID und das Attribut für eine Active Directory Directory Service-Objekt-Gruppe, der das Konto ein Mitglied ist.
ms.openlocfilehash: d73d72979762238ca09496cfbd6636b4ff44a969
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829767"
---
# <a name="groupidentifier"></a><span data-ttu-id="81169-103">GroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="81169-103">GroupIdentifier</span></span>

<span data-ttu-id="81169-104">Das Element **GroupIdentifier** stellt eine einzelne Sicherheits-ID und das Attribut für eine Active Directory Directory Service-Objekt-Gruppe, der das Konto ein Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="81169-104">The **GroupIdentifier** element represents a single security identifier and attribute for an Active Directory directory service object group of which the account is a member.</span></span> 
  
```xml
<GroupIdentifier>
   <SecurityIdentifier/>
</GroupIdentifier>
```

 <span data-ttu-id="81169-105">**SidAndAttributesType**</span><span class="sxs-lookup"><span data-stu-id="81169-105">**SidAndAttributesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="81169-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="81169-106">Attributes and elements</span></span>

<span data-ttu-id="81169-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="81169-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="81169-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="81169-108">Attributes</span></span>

|<span data-ttu-id="81169-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="81169-109">**Attribute**</span></span>|<span data-ttu-id="81169-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="81169-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="81169-111">**Attributes**</span><span class="sxs-lookup"><span data-stu-id="81169-111">**Attributes**</span></span> <br/> |<span data-ttu-id="81169-112">Enthält Gruppenattribute, die an.</span><span class="sxs-lookup"><span data-stu-id="81169-112">Contains group attributes.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="81169-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="81169-113">Child elements</span></span>

|<span data-ttu-id="81169-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="81169-114">**Element**</span></span>|<span data-ttu-id="81169-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="81169-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="81169-116">SecurityIdentifier</span><span class="sxs-lookup"><span data-stu-id="81169-116">SecurityIdentifier</span></span>](securityidentifier.md) <br/> |<span data-ttu-id="81169-117">Stellt die Security Descriptor Definition Language (SDDL) Form einer Sicherheits-ID ([SID](sid.md)), die die Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="81169-117">Represents the security descriptor definition language (SDDL) form of a security identifier ([SID](sid.md)) that represents the group.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="81169-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="81169-118">Parent elements</span></span>

|<span data-ttu-id="81169-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="81169-119">**Element**</span></span>|<span data-ttu-id="81169-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="81169-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="81169-121">GroupSids</span><span class="sxs-lookup"><span data-stu-id="81169-121">GroupSids</span></span>](groupsids.md) <br/> |<span data-ttu-id="81169-122">Stellt eine Auflistung von Active Directory-Gruppe Objekt Sicherheits-IDs, die ein Kontotoken für tokenserialisierung bilden.</span><span class="sxs-lookup"><span data-stu-id="81169-122">Represents a collection of Active Directory group object security identifiers that make up an account token for token serialization.</span></span> <span data-ttu-id="81169-123">Tokenserialisierung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="81169-123">Token serialization is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81169-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="81169-124">Remarks</span></span>

<span data-ttu-id="81169-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="81169-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="81169-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="81169-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="81169-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="81169-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="81169-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="81169-128">Schema Name</span></span>  <br/> |<span data-ttu-id="81169-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="81169-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="81169-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="81169-130">Validation File</span></span>  <br/> |<span data-ttu-id="81169-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="81169-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="81169-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="81169-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="81169-133">False</span><span class="sxs-lookup"><span data-stu-id="81169-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="81169-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81169-134">See also</span></span>



- [<span data-ttu-id="81169-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="81169-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

