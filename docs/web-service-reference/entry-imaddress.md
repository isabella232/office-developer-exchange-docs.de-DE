---
title: Eintrag (imaddresse)
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
description: Das Entry-Element stellt eine Chat Adresse (Instant Messaging) für einen Kontakt dar.
ms.openlocfilehash: b6cc37447eb0f231e9e852a6c3cd64d6e1f3a89f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460701"
---
# <a name="entry-imaddress"></a><span data-ttu-id="0bba7-103">Eintrag (imaddresse)</span><span class="sxs-lookup"><span data-stu-id="0bba7-103">Entry (IMAddress)</span></span>

<span data-ttu-id="0bba7-104">Das **Entry** -Element stellt eine Chat Adresse (Instant Messaging) für einen Kontakt dar.</span><span class="sxs-lookup"><span data-stu-id="0bba7-104">The **Entry** element represents an instant messaging (IM) address for a contact.</span></span> 
  
```xml
<Entry Key=""/>
```

 <span data-ttu-id="0bba7-105">**ImAddressDictionaryEntryType**</span><span class="sxs-lookup"><span data-stu-id="0bba7-105">**ImAddressDictionaryEntryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0bba7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0bba7-106">Attributes and elements</span></span>

<span data-ttu-id="0bba7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0bba7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0bba7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="0bba7-108">Attributes</span></span>

|<span data-ttu-id="0bba7-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0bba7-109">**Attribute**</span></span>|<span data-ttu-id="0bba7-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0bba7-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0bba7-111">**Key**</span><span class="sxs-lookup"><span data-stu-id="0bba7-111">**Key**</span></span> <br/> | <span data-ttu-id="0bba7-112">Identifiziert die Chat Adresse.</span><span class="sxs-lookup"><span data-stu-id="0bba7-112">Identifies the IM address.</span></span><br/><br/><span data-ttu-id="0bba7-113">Es folgen die möglichen Werte für dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="0bba7-113">The following are the possible values for this attribute:</span></span><br/><br/><span data-ttu-id="0bba7-114">- ImAddress1</span><span class="sxs-lookup"><span data-stu-id="0bba7-114">-  ImAddress1</span></span>  <br/><span data-ttu-id="0bba7-115">- ImAddress2</span><span class="sxs-lookup"><span data-stu-id="0bba7-115">-  ImAddress2</span></span>  <br/><span data-ttu-id="0bba7-116">- ImAddress3</span><span class="sxs-lookup"><span data-stu-id="0bba7-116">-  ImAddress3</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0bba7-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0bba7-117">Child elements</span></span>

<span data-ttu-id="0bba7-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="0bba7-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0bba7-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0bba7-119">Parent elements</span></span>

|<span data-ttu-id="0bba7-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="0bba7-120">**Element**</span></span>|<span data-ttu-id="0bba7-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0bba7-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0bba7-122">Imaddresses</span><span class="sxs-lookup"><span data-stu-id="0bba7-122">ImAddresses</span></span>](imaddresses.md) <br/> |<span data-ttu-id="0bba7-123">Stellt eine Auflistung von Chat Adressen für einen Kontakt dar.</span><span class="sxs-lookup"><span data-stu-id="0bba7-123">Represents a collection of IM addresses for a contact.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0bba7-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="0bba7-124">Text value</span></span>

<span data-ttu-id="0bba7-125">Ein Textwert, der die Chat Adresse darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0bba7-125">A text value that represents the IM address is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0bba7-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0bba7-126">Remarks</span></span>

<span data-ttu-id="0bba7-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="0bba7-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0bba7-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="0bba7-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0bba7-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="0bba7-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0bba7-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0bba7-130">Schema name</span></span>  <br/> |<span data-ttu-id="0bba7-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="0bba7-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="0bba7-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0bba7-132">Validation file</span></span>  <br/> |<span data-ttu-id="0bba7-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0bba7-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0bba7-134">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="0bba7-134">Can be empty</span></span>  <br/> |<span data-ttu-id="0bba7-135">False</span><span class="sxs-lookup"><span data-stu-id="0bba7-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0bba7-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0bba7-136">See also</span></span>

- [<span data-ttu-id="0bba7-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0bba7-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="0bba7-138">Creating Contacts (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="0bba7-138">Creating Contacts (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)  
- [<span data-ttu-id="0bba7-139">Aktualisieren von Kontakten</span><span class="sxs-lookup"><span data-stu-id="0bba7-139">Updating Contacts</span></span>](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)  
- [<span data-ttu-id="0bba7-140">Deleting Contacts</span><span class="sxs-lookup"><span data-stu-id="0bba7-140">Deleting Contacts</span></span>](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

