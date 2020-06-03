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
description: Das RestrictedGroupSids-Element stellt eine Auflistung von eingeschränkten Gruppen aus dem Token eines Benutzers dar.
ms.openlocfilehash: 739a73d2ac4bdbbee03650d035271b5c8d9ea25a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465359"
---
# <a name="restrictedgroupsids"></a><span data-ttu-id="21bfc-103">RestrictedGroupSids</span><span class="sxs-lookup"><span data-stu-id="21bfc-103">RestrictedGroupSids</span></span>

<span data-ttu-id="21bfc-104">Das **RestrictedGroupSids** -Element stellt eine Auflistung von eingeschränkten Gruppen aus dem Token eines Benutzers dar.</span><span class="sxs-lookup"><span data-stu-id="21bfc-104">The **RestrictedGroupSids** element represents a collection of restricted groups from a user's token.</span></span> 
  
```xml
<RestrictedGroupSids>
   <RestrictedGroupIdentifier/>
</RestrictedGroupSids>
```

 <span data-ttu-id="21bfc-105">**NonEmptyArrayOfRestrictedGroupIdentifiersType**</span><span class="sxs-lookup"><span data-stu-id="21bfc-105">**NonEmptyArrayOfRestrictedGroupIdentifiersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="21bfc-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="21bfc-106">Attributes and elements</span></span>

<span data-ttu-id="21bfc-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="21bfc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="21bfc-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="21bfc-108">Attributes</span></span>

<span data-ttu-id="21bfc-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="21bfc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="21bfc-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="21bfc-110">Child elements</span></span>

|<span data-ttu-id="21bfc-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="21bfc-111">**Element**</span></span>|<span data-ttu-id="21bfc-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="21bfc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="21bfc-113">RestrictedGroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="21bfc-113">RestrictedGroupIdentifier</span></span>](restrictedgroupidentifier.md) <br/> |<span data-ttu-id="21bfc-114">Stellt die sid (Group Security Identifier) und die Attribute für eine eingeschränkte Gruppe dar.</span><span class="sxs-lookup"><span data-stu-id="21bfc-114">Represents the group security identifier (SID) and attributes for a restricted group.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="21bfc-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="21bfc-115">Parent elements</span></span>

|<span data-ttu-id="21bfc-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="21bfc-116">**Element**</span></span>|<span data-ttu-id="21bfc-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="21bfc-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="21bfc-118">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="21bfc-118">SerializedSecurityContext</span></span>](serializedsecuritycontext.md) <br/> |<span data-ttu-id="21bfc-119">Wird im SOAP-Header für die Token-Serialisierung in der Server-zu-Server-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="21bfc-119">Used in the SOAP header for token serialization in server- to-server authentication.</span></span> <span data-ttu-id="21bfc-120">Die Serialisierung von Token wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="21bfc-120">Token serialization is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="21bfc-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21bfc-121">Remarks</span></span>

<span data-ttu-id="21bfc-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="21bfc-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="21bfc-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="21bfc-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="21bfc-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="21bfc-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="21bfc-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="21bfc-125">Schema Name</span></span>  <br/> |<span data-ttu-id="21bfc-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="21bfc-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="21bfc-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="21bfc-127">Validation File</span></span>  <br/> |<span data-ttu-id="21bfc-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="21bfc-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="21bfc-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="21bfc-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="21bfc-130">False</span><span class="sxs-lookup"><span data-stu-id="21bfc-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="21bfc-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21bfc-131">See also</span></span>



- [<span data-ttu-id="21bfc-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="21bfc-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

