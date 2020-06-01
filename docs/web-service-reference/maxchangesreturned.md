---
title: MaxChangesReturned
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MaxChangesReturned
api_type:
- schema
ms.assetid: f471db84-a666-4dfa-9993-8ca9113a0384
description: Das MaxChangesReturned-Element beschreibt die maximale Anzahl von Änderungen, die in einer Synchronisierungsantwort zurückgegeben werden können.
ms.openlocfilehash: caf96b6e95f2e63d0e544ead26fbea18cd637861
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460085"
---
# <a name="maxchangesreturned"></a><span data-ttu-id="369cb-103">MaxChangesReturned</span><span class="sxs-lookup"><span data-stu-id="369cb-103">MaxChangesReturned</span></span>

<span data-ttu-id="369cb-104">Das **MaxChangesReturned** -Element beschreibt die maximale Anzahl von Änderungen, die in einer Synchronisierungsantwort zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="369cb-104">The **MaxChangesReturned** element describes the maximum number of changes that can be returned in a synchronization response.</span></span> 
  
[<span data-ttu-id="369cb-105">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="369cb-105">SyncFolderItems</span></span>](syncfolderitems.md)
  
[<span data-ttu-id="369cb-106">MaxChangesReturned</span><span class="sxs-lookup"><span data-stu-id="369cb-106">MaxChangesReturned</span></span>](maxchangesreturned.md)
  
```xml
<MaxChangesReturned/>
```

 <span data-ttu-id="369cb-107">**int**</span><span class="sxs-lookup"><span data-stu-id="369cb-107">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="369cb-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="369cb-108">Attributes and elements</span></span>

<span data-ttu-id="369cb-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="369cb-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="369cb-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="369cb-110">Attributes</span></span>

<span data-ttu-id="369cb-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="369cb-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="369cb-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="369cb-112">Child elements</span></span>

<span data-ttu-id="369cb-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="369cb-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="369cb-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="369cb-114">Parent elements</span></span>

|<span data-ttu-id="369cb-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="369cb-115">**Element**</span></span>|<span data-ttu-id="369cb-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="369cb-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="369cb-117">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="369cb-117">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="369cb-118">Definiert eine Anforderung zum Synchronisieren von Elementen in einem Exchange-Informationsspeicher Ordner.</span><span class="sxs-lookup"><span data-stu-id="369cb-118">Defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="369cb-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="369cb-119">Text value</span></span>

<span data-ttu-id="369cb-120">Der Wert Text stellt eine ganze Zahl dar, die die maximale Anzahl von Elementen beschreibt, die in einem einzelnen Synchronisierungsaufruf zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="369cb-120">The text value represents an integer that describes the maximum number of items that are returned in a single synchronization call.</span></span> <span data-ttu-id="369cb-121">Der Wert muss zwischen 1 und 512 liegen, einschließlich.</span><span class="sxs-lookup"><span data-stu-id="369cb-121">The value must be between 1 and 512, inclusive.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="369cb-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="369cb-122">Remarks</span></span>

<span data-ttu-id="369cb-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="369cb-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="369cb-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="369cb-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="369cb-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="369cb-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="369cb-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="369cb-126">Schema name</span></span>  <br/> |<span data-ttu-id="369cb-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="369cb-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="369cb-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="369cb-128">Validation file</span></span>  <br/> |<span data-ttu-id="369cb-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="369cb-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="369cb-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="369cb-130">Can be empty</span></span>  <br/> |<span data-ttu-id="369cb-131">False</span><span class="sxs-lookup"><span data-stu-id="369cb-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="369cb-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="369cb-132">See also</span></span>



[<span data-ttu-id="369cb-133">SyncFolderItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="369cb-133">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="369cb-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="369cb-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

