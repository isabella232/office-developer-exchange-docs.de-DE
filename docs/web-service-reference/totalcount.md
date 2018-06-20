---
title: TotalCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TotalCount
api_type:
- schema
ms.assetid: c48c6388-8449-4622-bc38-6f0e84293872
description: Das Element TotalCount stellt die Gesamtzahl der Elemente in einem bestimmten Ordner.
ms.openlocfilehash: e4a7bcb70d04bc5bcf66087c0272732a7be1231a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839241"
---
# <a name="totalcount"></a><span data-ttu-id="ec746-103">TotalCount</span><span class="sxs-lookup"><span data-stu-id="ec746-103">TotalCount</span></span>

<span data-ttu-id="ec746-104">Das Element **TotalCount** stellt die Gesamtzahl der Elemente in einem bestimmten Ordner.</span><span class="sxs-lookup"><span data-stu-id="ec746-104">The **TotalCount** element represents the total count of items within a given folder.</span></span> 
  
```xml
<TotalCount/>
```

 <span data-ttu-id="ec746-105">**int**</span><span class="sxs-lookup"><span data-stu-id="ec746-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ec746-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ec746-106">Attributes and elements</span></span>

<span data-ttu-id="ec746-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ec746-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ec746-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ec746-108">Attributes</span></span>

<span data-ttu-id="ec746-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ec746-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ec746-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ec746-110">Child elements</span></span>

<span data-ttu-id="ec746-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ec746-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ec746-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ec746-112">Parent elements</span></span>

|<span data-ttu-id="ec746-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ec746-113">**Element**</span></span>|<span data-ttu-id="ec746-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ec746-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ec746-115">Folder</span><span class="sxs-lookup"><span data-stu-id="ec746-115">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="ec746-116">Stellt einen Ordner in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="ec746-116">Represents a folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="ec746-117">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="ec746-117">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="ec746-118">Stellt einen Kalenderordner in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="ec746-118">Represents a calendar folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="ec746-119">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="ec746-119">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="ec746-120">Stellt einen Kontakteordner in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="ec746-120">Represents a contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="ec746-121">"SearchFolder"</span><span class="sxs-lookup"><span data-stu-id="ec746-121">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="ec746-122">Stellt einen Suchordner in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="ec746-122">Represents a search folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="ec746-123">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="ec746-123">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="ec746-124">Stellt einen Ordner in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="ec746-124">Represents a task folder in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ec746-125">Textwert</span><span class="sxs-lookup"><span data-stu-id="ec746-125">Text value</span></span>

<span data-ttu-id="ec746-126">Der Textwert stellt einen ganzzahligen Wert dar.</span><span class="sxs-lookup"><span data-stu-id="ec746-126">The text value represents an integer value.</span></span> <span data-ttu-id="ec746-127">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ec746-127">This property is read-only.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ec746-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ec746-128">Remarks</span></span>

<span data-ttu-id="ec746-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="ec746-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ec746-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ec746-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec746-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="ec746-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ec746-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ec746-132">Schema Name</span></span>  <br/> |<span data-ttu-id="ec746-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ec746-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="ec746-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ec746-134">Validation File</span></span>  <br/> |<span data-ttu-id="ec746-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ec746-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ec746-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ec746-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="ec746-137">False</span><span class="sxs-lookup"><span data-stu-id="ec746-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ec746-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec746-138">See also</span></span>



- [<span data-ttu-id="ec746-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ec746-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

