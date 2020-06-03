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
description: Das GroupIdentifier-Element stellt eine einzelne Sicherheits-ID und ein einzelnes Attribut für eine Active Directory Verzeichnisdienst-Objektgruppe dar, der das Konto angehört.
ms.openlocfilehash: 8b427b9228cc5e66f46f70389acf2fa4bcd283b3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530803"
---
# <a name="groupidentifier"></a><span data-ttu-id="6436d-103">GroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="6436d-103">GroupIdentifier</span></span>

<span data-ttu-id="6436d-104">Das **GroupIdentifier** -Element stellt eine einzelne Sicherheits-ID und ein einzelnes Attribut für eine Active Directory Verzeichnisdienst-Objektgruppe dar, der das Konto angehört.</span><span class="sxs-lookup"><span data-stu-id="6436d-104">The **GroupIdentifier** element represents a single security identifier and attribute for an Active Directory directory service object group of which the account is a member.</span></span> 
  
```xml
<GroupIdentifier>
   <SecurityIdentifier/>
</GroupIdentifier>
```

 <span data-ttu-id="6436d-105">**SidAndAttributesType**</span><span class="sxs-lookup"><span data-stu-id="6436d-105">**SidAndAttributesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6436d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6436d-106">Attributes and elements</span></span>

<span data-ttu-id="6436d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6436d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6436d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6436d-108">Attributes</span></span>

|<span data-ttu-id="6436d-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="6436d-109">**Attribute**</span></span>|<span data-ttu-id="6436d-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6436d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6436d-111">**Attributes**</span><span class="sxs-lookup"><span data-stu-id="6436d-111">**Attributes**</span></span> <br/> |<span data-ttu-id="6436d-112">Enthält Gruppenattribute.</span><span class="sxs-lookup"><span data-stu-id="6436d-112">Contains group attributes.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6436d-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6436d-113">Child elements</span></span>

|<span data-ttu-id="6436d-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="6436d-114">**Element**</span></span>|<span data-ttu-id="6436d-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6436d-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6436d-116">SecurityIdentifier</span><span class="sxs-lookup"><span data-stu-id="6436d-116">SecurityIdentifier</span></span>](securityidentifier.md) <br/> |<span data-ttu-id="6436d-117">Stellt das SDDL-Formular (Security Descriptor Definition Language) einer Sicherheits-ID (Security Identifier,[sid](sid.md)) dar, die die Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="6436d-117">Represents the security descriptor definition language (SDDL) form of a security identifier ([SID](sid.md)) that represents the group.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6436d-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6436d-118">Parent elements</span></span>

|<span data-ttu-id="6436d-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="6436d-119">**Element**</span></span>|<span data-ttu-id="6436d-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6436d-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6436d-121">GroupSids</span><span class="sxs-lookup"><span data-stu-id="6436d-121">GroupSids</span></span>](groupsids.md) <br/> |<span data-ttu-id="6436d-122">Stellt eine Auflistung von Sicherheits-IDs für Active Directory Group-Objekt dar, die ein Kontotoken für die Token-Serialisierung bilden.</span><span class="sxs-lookup"><span data-stu-id="6436d-122">Represents a collection of Active Directory group object security identifiers that make up an account token for token serialization.</span></span> <span data-ttu-id="6436d-123">Die Serialisierung von Token wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6436d-123">Token serialization is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6436d-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6436d-124">Remarks</span></span>

<span data-ttu-id="6436d-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="6436d-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6436d-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="6436d-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6436d-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="6436d-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6436d-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6436d-128">Schema Name</span></span>  <br/> |<span data-ttu-id="6436d-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="6436d-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="6436d-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6436d-130">Validation File</span></span>  <br/> |<span data-ttu-id="6436d-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6436d-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6436d-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6436d-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="6436d-133">False</span><span class="sxs-lookup"><span data-stu-id="6436d-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6436d-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6436d-134">See also</span></span>



- [<span data-ttu-id="6436d-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6436d-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

