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
description: Rules-Element enthält ein Array von Regeln für den Schutz.
ms.openlocfilehash: 5d511f977f3eb3273dc43f56356a059985b2a929
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831269"
---
# <a name="rules"></a><span data-ttu-id="abc46-103">Regeln</span><span class="sxs-lookup"><span data-stu-id="abc46-103">Rules</span></span>

<span data-ttu-id="abc46-104">**Rules** -Element enthält ein Array von Regeln für den Schutz.</span><span class="sxs-lookup"><span data-stu-id="abc46-104">The **Rules** element contains an array of protection rules.</span></span> 
  
```xml
<Rules>   <Rule/></Rules>
```

 <span data-ttu-id="abc46-105">**ArrayOfProtectionRulesType**</span><span class="sxs-lookup"><span data-stu-id="abc46-105">**ArrayOfProtectionRulesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="abc46-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="abc46-106">Attributes and elements</span></span>

<span data-ttu-id="abc46-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="abc46-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="abc46-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="abc46-108">Attributes</span></span>

<span data-ttu-id="abc46-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="abc46-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="abc46-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="abc46-110">Child elements</span></span>

|<span data-ttu-id="abc46-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="abc46-111">**Element**</span></span>|<span data-ttu-id="abc46-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="abc46-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="abc46-113">Rule</span><span class="sxs-lookup"><span data-stu-id="abc46-113">Rule</span></span>](rule.md) <br/> |<span data-ttu-id="abc46-114">Enthält eine einzelne Schutzregel.</span><span class="sxs-lookup"><span data-stu-id="abc46-114">Contains a single protection rule.</span></span> <span data-ttu-id="abc46-115">Dieses Element kann NULL oder mehrere Male vorkommen.</span><span class="sxs-lookup"><span data-stu-id="abc46-115">This element can occur zero or more times.</span></span> <span data-ttu-id="abc46-116">Dieses Element tritt Male, wenn keine Regeln für den Schutz von der Organisation definiert sind.</span><span class="sxs-lookup"><span data-stu-id="abc46-116">This element occurs zero times when no protection rules are defined by the organization.</span></span> <span data-ttu-id="abc46-117">Es tritt ein oder mehrere Male, wenn mindestens eine Regel, die von der Organisation definiert ist.</span><span class="sxs-lookup"><span data-stu-id="abc46-117">It occurs one or more times if at least one rule is defined by the organization.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="abc46-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="abc46-118">Parent elements</span></span>

|<span data-ttu-id="abc46-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="abc46-119">**Element**</span></span>|<span data-ttu-id="abc46-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="abc46-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="abc46-121">ProtectionRulesConfiguration</span><span class="sxs-lookup"><span data-stu-id="abc46-121">ProtectionRulesConfiguration</span></span>](protectionrulesconfiguration.md) <br/> |<span data-ttu-id="abc46-122">Konfiguration für den Schutz Regeln Dienst enthält.</span><span class="sxs-lookup"><span data-stu-id="abc46-122">Contains service configuration for the protection rules service.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="abc46-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="abc46-123">Remarks</span></span>

<span data-ttu-id="abc46-124">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="abc46-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="abc46-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="abc46-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="abc46-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="abc46-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="abc46-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="abc46-127">Schema Name</span></span>  <br/> |<span data-ttu-id="abc46-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="abc46-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="abc46-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="abc46-129">Validation File</span></span>  <br/> |<span data-ttu-id="abc46-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="abc46-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="abc46-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="abc46-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="abc46-132">False</span><span class="sxs-lookup"><span data-stu-id="abc46-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="abc46-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abc46-133">See also</span></span>



- [<span data-ttu-id="abc46-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="abc46-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

