---
title: UnknownEntry
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnknownEntry
api_type:
- schema
ms.assetid: 3cb4c62e-052a-4326-8639-8c41dfd047b2
description: Das UnknownEntry-Element stellt einen einzelnen unbekannten Berechtigungseintrag dar, der nicht für den Active Directory Verzeichnisdienst aufgelöst werden kann. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 452857690f719ba3ee9dffa29e576ca4f3b2b945
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459398"
---
# <a name="unknownentry"></a><span data-ttu-id="da415-104">UnknownEntry</span><span class="sxs-lookup"><span data-stu-id="da415-104">UnknownEntry</span></span>

<span data-ttu-id="da415-105">Das **UnknownEntry** -Element stellt einen einzelnen unbekannten Berechtigungseintrag dar, der nicht für den Active Directory Verzeichnisdienst aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="da415-105">The **UnknownEntry** element represents a single unknown permission entry that cannot be resolved against the Active Directory directory service.</span></span> <span data-ttu-id="da415-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="da415-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<UnknownEntry/>
```

 <span data-ttu-id="da415-107">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="da415-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="da415-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="da415-108">Attributes and elements</span></span>

<span data-ttu-id="da415-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="da415-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="da415-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="da415-110">Attributes</span></span>

<span data-ttu-id="da415-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="da415-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="da415-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="da415-112">Child elements</span></span>

<span data-ttu-id="da415-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="da415-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="da415-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="da415-114">Parent elements</span></span>

|<span data-ttu-id="da415-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="da415-115">**Element**</span></span>|<span data-ttu-id="da415-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="da415-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="da415-117">UnknownEntries</span><span class="sxs-lookup"><span data-stu-id="da415-117">UnknownEntries</span></span>](unknownentries.md) <br/> |<span data-ttu-id="da415-118">Enthält ein Array von unbekannten Berechtigungseinträgen, die nicht für Active Directory aufgelöst werden können.</span><span class="sxs-lookup"><span data-stu-id="da415-118">Contains an array of unknown permission entries that cannot be resolved against Active Directory.</span></span> <span data-ttu-id="da415-119">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="da415-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="da415-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="da415-120">Text value</span></span>

<span data-ttu-id="da415-121">Der Wert Text stellt einen Berechtigungseintrag dar, der nicht für Active Directory aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="da415-121">The text value represents a permission entry that cannot be resolved against Active Directory.</span></span> <span data-ttu-id="da415-122">Der Wert Text stellt eine Sicherheits-ID (SID) dar.</span><span class="sxs-lookup"><span data-stu-id="da415-122">The text value represents a security identifier (SID).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="da415-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da415-123">Remarks</span></span>

<span data-ttu-id="da415-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="da415-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="da415-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="da415-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="da415-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="da415-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="da415-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="da415-127">Schema Name</span></span>  <br/> |<span data-ttu-id="da415-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="da415-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="da415-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="da415-129">Validation File</span></span>  <br/> |<span data-ttu-id="da415-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="da415-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="da415-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="da415-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="da415-132">False</span><span class="sxs-lookup"><span data-stu-id="da415-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="da415-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da415-133">See also</span></span>



- [<span data-ttu-id="da415-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="da415-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="da415-135">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="da415-135">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

