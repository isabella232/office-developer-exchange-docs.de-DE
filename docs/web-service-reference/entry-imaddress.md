---
title: Eintrag (IMAddress)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Entry
api_type:
- schema
ms.assetid: ee444170-7353-4e86-86c6-d7300a2f1777
description: Entry-Element stellt ein Instant messaging (IM)-Adresse für einen Kontakt.
ms.openlocfilehash: 77de059cef470dde90ab0b929845cb260b4b867c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758267"
---
# <a name="entry-imaddress"></a><span data-ttu-id="4450a-103">Eintrag (IMAddress)</span><span class="sxs-lookup"><span data-stu-id="4450a-103">Entry (IMAddress)</span></span>

<span data-ttu-id="4450a-104">**Entry** -Element stellt ein Instant messaging (IM)-Adresse für einen Kontakt.</span><span class="sxs-lookup"><span data-stu-id="4450a-104">The **Entry** element represents an instant messaging (IM) address for a contact.</span></span> 
  
```xml
<Entry Key=""/>
```

 <span data-ttu-id="4450a-105">**ImAddressDictionaryEntryType**</span><span class="sxs-lookup"><span data-stu-id="4450a-105">**ImAddressDictionaryEntryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4450a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4450a-106">Attributes and elements</span></span>

<span data-ttu-id="4450a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4450a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4450a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4450a-108">Attributes</span></span>

|<span data-ttu-id="4450a-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4450a-109">**Attribute**</span></span>|<span data-ttu-id="4450a-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4450a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4450a-111">**Key**</span><span class="sxs-lookup"><span data-stu-id="4450a-111">**Key**</span></span> <br/> | <span data-ttu-id="4450a-112">Die IM-Adresse identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4450a-112">Identifies the IM address.</span></span><br/><br/><span data-ttu-id="4450a-113">Es folgen die möglichen Werte für dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="4450a-113">The following are the possible values for this attribute:</span></span><br/><br/><span data-ttu-id="4450a-114">-ImAddress1</span><span class="sxs-lookup"><span data-stu-id="4450a-114">-  ImAddress1</span></span>  <br/><span data-ttu-id="4450a-115">-ImAddress2</span><span class="sxs-lookup"><span data-stu-id="4450a-115">-  ImAddress2</span></span>  <br/><span data-ttu-id="4450a-116">-ImAddress3</span><span class="sxs-lookup"><span data-stu-id="4450a-116">-  ImAddress3</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4450a-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4450a-117">Child elements</span></span>

<span data-ttu-id="4450a-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="4450a-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4450a-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4450a-119">Parent elements</span></span>

|<span data-ttu-id="4450a-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="4450a-120">**Element**</span></span>|<span data-ttu-id="4450a-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4450a-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4450a-122">ImAddresses</span><span class="sxs-lookup"><span data-stu-id="4450a-122">ImAddresses</span></span>](imaddresses.md) <br/> |<span data-ttu-id="4450a-123">Stellt eine Auflistung von Instant Messaging-Adressen für einen Kontakt.</span><span class="sxs-lookup"><span data-stu-id="4450a-123">Represents a collection of IM addresses for a contact.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4450a-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="4450a-124">Text value</span></span>

<span data-ttu-id="4450a-125">Ein Textwert, der die IM-Adresse darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4450a-125">A text value that represents the IM address is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4450a-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4450a-126">Remarks</span></span>

<span data-ttu-id="4450a-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="4450a-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4450a-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4450a-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4450a-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="4450a-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4450a-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4450a-130">Schema name</span></span>  <br/> |<span data-ttu-id="4450a-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="4450a-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="4450a-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4450a-132">Validation file</span></span>  <br/> |<span data-ttu-id="4450a-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4450a-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4450a-134">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="4450a-134">Can be empty</span></span>  <br/> |<span data-ttu-id="4450a-135">False</span><span class="sxs-lookup"><span data-stu-id="4450a-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4450a-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4450a-136">See also</span></span>

- [<span data-ttu-id="4450a-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4450a-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="4450a-138">Creating Contacts (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="4450a-138">Creating Contacts (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)  
- [<span data-ttu-id="4450a-139">Aktualisierung von Kontakten</span><span class="sxs-lookup"><span data-stu-id="4450a-139">Updating Contacts</span></span>](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)  
- [<span data-ttu-id="4450a-140">Deleting Contacts</span><span class="sxs-lookup"><span data-stu-id="4450a-140">Deleting Contacts</span></span>](http://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

