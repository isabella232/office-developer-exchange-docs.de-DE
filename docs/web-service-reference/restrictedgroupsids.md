---
title: RestrictedGroupSids
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RestrictedGroupSids
api_type:
- schema
ms.assetid: 569ab552-5616-444a-a7f5-de366a684a34
description: Das Element RestrictedGroupSids stellt eine Auflistung von eingeschränkte Gruppen von Token des Benutzers an.
ms.openlocfilehash: fcfee809261c7ed0a4e0d092c091841fec641e46
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831201"
---
# <a name="restrictedgroupsids"></a><span data-ttu-id="864bf-103">RestrictedGroupSids</span><span class="sxs-lookup"><span data-stu-id="864bf-103">RestrictedGroupSids</span></span>

<span data-ttu-id="864bf-104">Das Element **RestrictedGroupSids** stellt eine Auflistung von eingeschränkte Gruppen von Token des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="864bf-104">The **RestrictedGroupSids** element represents a collection of restricted groups from a user's token.</span></span> 
  
```xml
<RestrictedGroupSids>
   <RestrictedGroupIdentifier/>
</RestrictedGroupSids>
```

 <span data-ttu-id="864bf-105">**NonEmptyArrayOfRestrictedGroupIdentifiersType**</span><span class="sxs-lookup"><span data-stu-id="864bf-105">**NonEmptyArrayOfRestrictedGroupIdentifiersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="864bf-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="864bf-106">Attributes and elements</span></span>

<span data-ttu-id="864bf-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="864bf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="864bf-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="864bf-108">Attributes</span></span>

<span data-ttu-id="864bf-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="864bf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="864bf-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="864bf-110">Child elements</span></span>

|<span data-ttu-id="864bf-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="864bf-111">**Element**</span></span>|<span data-ttu-id="864bf-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="864bf-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="864bf-113">RestrictedGroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="864bf-113">RestrictedGroupIdentifier</span></span>](restrictedgroupidentifier.md) <br/> |<span data-ttu-id="864bf-114">Stellt die Gruppe Sicherheits-ID (SID) und Attribute für eine eingeschränkte Gruppe.</span><span class="sxs-lookup"><span data-stu-id="864bf-114">Represents the group security identifier (SID) and attributes for a restricted group.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="864bf-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="864bf-115">Parent elements</span></span>

|<span data-ttu-id="864bf-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="864bf-116">**Element**</span></span>|<span data-ttu-id="864bf-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="864bf-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="864bf-118">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="864bf-118">SerializedSecurityContext</span></span>](serializedsecuritycontext.md) <br/> |<span data-ttu-id="864bf-119">In den SOAP-Header verwendet für tokenserialisierung für Server-zu-Server-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="864bf-119">Used in the SOAP header for token serialization in server- to-server authentication.</span></span> <span data-ttu-id="864bf-120">Tokenserialisierung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="864bf-120">Token serialization is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="864bf-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="864bf-121">Remarks</span></span>

<span data-ttu-id="864bf-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="864bf-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="864bf-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="864bf-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="864bf-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="864bf-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="864bf-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="864bf-125">Schema Name</span></span>  <br/> |<span data-ttu-id="864bf-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="864bf-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="864bf-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="864bf-127">Validation File</span></span>  <br/> |<span data-ttu-id="864bf-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="864bf-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="864bf-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="864bf-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="864bf-130">False</span><span class="sxs-lookup"><span data-stu-id="864bf-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="864bf-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="864bf-131">See also</span></span>



- [<span data-ttu-id="864bf-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="864bf-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

