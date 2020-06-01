---
title: Regeln
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Rules
api_type:
- schema
ms.assetid: 53f59054-8f68-4eaa-be9c-ccfc9383bcf2
description: Das rules-Element enthält ein Array von Schutzregeln.
ms.openlocfilehash: d848abfe0c97d07836f28bc75806f506c5433d44
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464938"
---
# <a name="rules"></a><span data-ttu-id="5a4e8-103">Regeln</span><span class="sxs-lookup"><span data-stu-id="5a4e8-103">Rules</span></span>

<span data-ttu-id="5a4e8-104">Das **Rules** -Element enthält ein Array von Schutzregeln.</span><span class="sxs-lookup"><span data-stu-id="5a4e8-104">The **Rules** element contains an array of protection rules.</span></span> 
  
```xml
<Rules>   <Rule/></Rules>
```

 <span data-ttu-id="5a4e8-105">**ArrayOfProtectionRulesType**</span><span class="sxs-lookup"><span data-stu-id="5a4e8-105">**ArrayOfProtectionRulesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5a4e8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5a4e8-106">Attributes and elements</span></span>

<span data-ttu-id="5a4e8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5a4e8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5a4e8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5a4e8-108">Attributes</span></span>

<span data-ttu-id="5a4e8-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5a4e8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5a4e8-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5a4e8-110">Child elements</span></span>

|<span data-ttu-id="5a4e8-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="5a4e8-111">**Element**</span></span>|<span data-ttu-id="5a4e8-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5a4e8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5a4e8-113">Rule</span><span class="sxs-lookup"><span data-stu-id="5a4e8-113">Rule</span></span>](rule.md) <br/> |<span data-ttu-id="5a4e8-114">Enthält eine einzelne Schutz Regel.</span><span class="sxs-lookup"><span data-stu-id="5a4e8-114">Contains a single protection rule.</span></span> <span data-ttu-id="5a4e8-115">Dieses Element kann 0 oder mehr Male vorkommen.</span><span class="sxs-lookup"><span data-stu-id="5a4e8-115">This element can occur zero or more times.</span></span> <span data-ttu-id="5a4e8-116">Dieses Element tritt null mal auf, wenn keine Schutzregeln durch die Organisation definiert sind.</span><span class="sxs-lookup"><span data-stu-id="5a4e8-116">This element occurs zero times when no protection rules are defined by the organization.</span></span> <span data-ttu-id="5a4e8-117">Es tritt mindestens einmal auf, wenn mindestens eine Regel von der Organisation definiert wird.</span><span class="sxs-lookup"><span data-stu-id="5a4e8-117">It occurs one or more times if at least one rule is defined by the organization.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5a4e8-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5a4e8-118">Parent elements</span></span>

|<span data-ttu-id="5a4e8-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="5a4e8-119">**Element**</span></span>|<span data-ttu-id="5a4e8-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5a4e8-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5a4e8-121">ProtectionRulesConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a4e8-121">ProtectionRulesConfiguration</span></span>](protectionrulesconfiguration.md) <br/> |<span data-ttu-id="5a4e8-122">Enthält die Dienstkonfiguration für den Schutz Regeldienst.</span><span class="sxs-lookup"><span data-stu-id="5a4e8-122">Contains service configuration for the protection rules service.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a4e8-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a4e8-123">Remarks</span></span>

<span data-ttu-id="5a4e8-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="5a4e8-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5a4e8-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="5a4e8-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5a4e8-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="5a4e8-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5a4e8-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5a4e8-127">Schema Name</span></span>  <br/> |<span data-ttu-id="5a4e8-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="5a4e8-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="5a4e8-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5a4e8-129">Validation File</span></span>  <br/> |<span data-ttu-id="5a4e8-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5a4e8-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5a4e8-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5a4e8-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="5a4e8-132">False</span><span class="sxs-lookup"><span data-stu-id="5a4e8-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5a4e8-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a4e8-133">See also</span></span>



- [<span data-ttu-id="5a4e8-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5a4e8-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

