---
title: Unternehmen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Companies
api_type:
- schema
ms.assetid: 5d9ea76f-e14d-4424-8842-0c3cc3305119
description: Das Companies-Element stellt die Auflistung von Unternehmen dar, die einem Kontakt oder einer Aufgabe zugeordnet sind.
ms.openlocfilehash: eda2b92f3ca874aeeceef6a0935a49a98af0ec39
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461450"
---
# <a name="companies"></a><span data-ttu-id="5b4e0-103">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="5b4e0-103">Companies</span></span>

<span data-ttu-id="5b4e0-104">Das **Companies** -Element stellt die Auflistung von Unternehmen dar, die einem Kontakt oder einer Aufgabe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5b4e0-104">The **Companies** element represents the collection of companies that are associated with a contact or task.</span></span> 
  
```xml
<Companies>
   <String/>
</Companies>
```

 <span data-ttu-id="5b4e0-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="5b4e0-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5b4e0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5b4e0-106">Attributes and elements</span></span>

<span data-ttu-id="5b4e0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5b4e0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5b4e0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5b4e0-108">Attributes</span></span>

<span data-ttu-id="5b4e0-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5b4e0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5b4e0-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5b4e0-110">Child elements</span></span>

|<span data-ttu-id="5b4e0-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="5b4e0-111">**Element**</span></span>|<span data-ttu-id="5b4e0-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5b4e0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5b4e0-113">String</span><span class="sxs-lookup"><span data-stu-id="5b4e0-113">String</span></span>](string.md) <br/> |<span data-ttu-id="5b4e0-114">Stellt den Namen eines Unternehmens dar.</span><span class="sxs-lookup"><span data-stu-id="5b4e0-114">Represents the name of a company.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5b4e0-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5b4e0-115">Parent elements</span></span>

|<span data-ttu-id="5b4e0-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="5b4e0-116">**Element**</span></span>|<span data-ttu-id="5b4e0-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5b4e0-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5b4e0-118">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="5b4e0-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="5b4e0-119">Stellt einen Kontakt im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="5b4e0-119">Represents a contact in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5b4e0-120">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="5b4e0-120">Task</span></span>](task.md) <br/> |<span data-ttu-id="5b4e0-121">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="5b4e0-121">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b4e0-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b4e0-122">Remarks</span></span>

<span data-ttu-id="5b4e0-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="5b4e0-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5b4e0-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="5b4e0-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5b4e0-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="5b4e0-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5b4e0-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5b4e0-126">Schema name</span></span>  <br/> |<span data-ttu-id="5b4e0-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="5b4e0-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="5b4e0-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5b4e0-128">Validation file</span></span>  <br/> |<span data-ttu-id="5b4e0-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5b4e0-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5b4e0-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="5b4e0-130">Can be empty</span></span>  <br/> |<span data-ttu-id="5b4e0-131">False</span><span class="sxs-lookup"><span data-stu-id="5b4e0-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5b4e0-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b4e0-132">See also</span></span>



- [<span data-ttu-id="5b4e0-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5b4e0-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

