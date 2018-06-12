---
title: Untergeordnete Objekte
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Children
api_type:
- schema
ms.assetid: ceaffddd-f9bc-43ea-b348-a20fdade738f
description: Das untergeordnete Element enthält die Namen der untergeordneten Elemente eines Kontakts.
ms.openlocfilehash: 9b1e06529fcf74850755daefc299242cfbf81f1e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757562"
---
# <a name="children"></a><span data-ttu-id="60541-103">Untergeordnete Objekte</span><span class="sxs-lookup"><span data-stu-id="60541-103">Children</span></span>

<span data-ttu-id="60541-104">Das **untergeordnete** Element enthält die Namen der untergeordneten Elemente eines Kontakts.</span><span class="sxs-lookup"><span data-stu-id="60541-104">The **Children** element contains the names of a contact's children.</span></span> 
  
```xml
<Children>
   <String/>
</Children>
```

 <span data-ttu-id="60541-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="60541-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="60541-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="60541-106">Attributes and elements</span></span>

<span data-ttu-id="60541-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="60541-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="60541-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="60541-108">Attributes</span></span>

<span data-ttu-id="60541-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="60541-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="60541-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="60541-110">Child elements</span></span>

|<span data-ttu-id="60541-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="60541-111">**Element**</span></span>|<span data-ttu-id="60541-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="60541-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="60541-113">String</span><span class="sxs-lookup"><span data-stu-id="60541-113">String</span></span>](string.md) <br/> |<span data-ttu-id="60541-114">Enthält den Namen des untergeordneten Elements des Kontakts.</span><span class="sxs-lookup"><span data-stu-id="60541-114">Contains the name of a contact's child.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="60541-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="60541-115">Parent elements</span></span>

|<span data-ttu-id="60541-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="60541-116">**Element**</span></span>|<span data-ttu-id="60541-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="60541-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="60541-118">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="60541-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="60541-119">Stellt einen Kontakt in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="60541-119">Represents a contact in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="60541-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60541-120">Remarks</span></span>

<span data-ttu-id="60541-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="60541-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="60541-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="60541-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="60541-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="60541-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="60541-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="60541-124">Schema name</span></span>  <br/> |<span data-ttu-id="60541-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="60541-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="60541-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="60541-126">Validation file</span></span>  <br/> |<span data-ttu-id="60541-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="60541-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="60541-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="60541-128">Can be empty</span></span>  <br/> |<span data-ttu-id="60541-129">False</span><span class="sxs-lookup"><span data-stu-id="60541-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="60541-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60541-130">See also</span></span>



- [<span data-ttu-id="60541-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="60541-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
