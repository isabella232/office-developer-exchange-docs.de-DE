---
title: Kontakte
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Contacts
api_type:
- schema
ms.assetid: 0cc67cdf-9707-45e7-92c6-fa83a016cdbe
description: Kontakte-Element enthält eine Liste von Kontakten, die mit einem Vorgang verknüpft sind.
ms.openlocfilehash: da7963d30f58f7da52e76e3f7f1d0f7fd68abf74
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757614"
---
# <a name="contacts"></a><span data-ttu-id="117de-103">Kontakte</span><span class="sxs-lookup"><span data-stu-id="117de-103">Contacts</span></span>

<span data-ttu-id="117de-104">**Kontakte** -Element enthält eine Liste von Kontakten, die mit einem Vorgang verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="117de-104">The **Contacts** element contains a list of contacts that are associated with a task.</span></span> 
  
```xml
<Contacts>
   <String/>
</Contacts>
```

 <span data-ttu-id="117de-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="117de-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="117de-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="117de-106">Attributes and elements</span></span>

<span data-ttu-id="117de-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="117de-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="117de-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="117de-108">Attributes</span></span>

<span data-ttu-id="117de-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="117de-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="117de-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="117de-110">Child elements</span></span>

|<span data-ttu-id="117de-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="117de-111">**Element**</span></span>|<span data-ttu-id="117de-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="117de-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="117de-113">String</span><span class="sxs-lookup"><span data-stu-id="117de-113">String</span></span>](string.md) <br/> |<span data-ttu-id="117de-114">Stellt eine durch Trennzeichen getrennte Liste mit Kontaktnamen.</span><span class="sxs-lookup"><span data-stu-id="117de-114">Represents a comma-separated list of contact names.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="117de-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="117de-115">Parent elements</span></span>

|<span data-ttu-id="117de-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="117de-116">**Element**</span></span>|<span data-ttu-id="117de-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="117de-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="117de-118">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="117de-118">Task</span></span>](task.md) <br/> |<span data-ttu-id="117de-119">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="117de-119">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="117de-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="117de-120">Remarks</span></span>

<span data-ttu-id="117de-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="117de-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="117de-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="117de-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="117de-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="117de-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="117de-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="117de-124">Schema name</span></span>  <br/> |<span data-ttu-id="117de-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="117de-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="117de-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="117de-126">Validation file</span></span>  <br/> |<span data-ttu-id="117de-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="117de-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="117de-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="117de-128">Can be empty</span></span>  <br/> |<span data-ttu-id="117de-129">False</span><span class="sxs-lookup"><span data-stu-id="117de-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="117de-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="117de-130">See also</span></span>



- [<span data-ttu-id="117de-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="117de-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

