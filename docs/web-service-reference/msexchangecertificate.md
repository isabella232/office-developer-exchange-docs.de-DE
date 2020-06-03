---
title: MSExchangeCertificate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c514f22f-be3e-4cad-ac56-bdff6bafcee6
description: Das MSExchangeCertificate-Element enthält einen Wert, der das Microsoft Exchange Zertifikat eines Kontakts codiert.
ms.openlocfilehash: 60bbcfb45e52dc92140d03cdd24a251ea84217b1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465674"
---
# <a name="msexchangecertificate"></a><span data-ttu-id="166d3-103">MSExchangeCertificate</span><span class="sxs-lookup"><span data-stu-id="166d3-103">MSExchangeCertificate</span></span>

<span data-ttu-id="166d3-104">Das **MSExchangeCertificate** -Element enthält einen Wert, der das Microsoft Exchange Zertifikat eines Kontakts codiert.</span><span class="sxs-lookup"><span data-stu-id="166d3-104">The **MSExchangeCertificate** element contains a value that encodes the Microsoft Exchange certificate of a contact.</span></span> 
  
```XML
<MSExchangeCertificate/>
```

 <span data-ttu-id="166d3-105">**ArrayOfBinaryType**</span><span class="sxs-lookup"><span data-stu-id="166d3-105">**ArrayOfBinaryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="166d3-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="166d3-106">Attributes and elements</span></span>

<span data-ttu-id="166d3-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="166d3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="166d3-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="166d3-108">Attributes</span></span>

<span data-ttu-id="166d3-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="166d3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="166d3-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="166d3-110">Child elements</span></span>

|<span data-ttu-id="166d3-111">**Elementname**</span><span class="sxs-lookup"><span data-stu-id="166d3-111">**Element name**</span></span>|<span data-ttu-id="166d3-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="166d3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="166d3-113">Base64Binary</span><span class="sxs-lookup"><span data-stu-id="166d3-113">Base64Binary</span></span>](base64binary.md) <br/> |<span data-ttu-id="166d3-114">Enthält einen Base64-codierten Wert.</span><span class="sxs-lookup"><span data-stu-id="166d3-114">Contains a Base64-encoded value.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="166d3-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="166d3-115">Parent elements</span></span>

|<span data-ttu-id="166d3-116">**Elementname**</span><span class="sxs-lookup"><span data-stu-id="166d3-116">**Element name**</span></span>|<span data-ttu-id="166d3-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="166d3-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="166d3-118">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="166d3-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="166d3-119">Stellt ein Kontaktelement im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="166d3-119">Represents a contact item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="166d3-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="166d3-120">Text value</span></span>

<span data-ttu-id="166d3-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="166d3-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="166d3-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="166d3-122">Remarks</span></span>

<span data-ttu-id="166d3-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="166d3-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="166d3-124">Dieses Element wurde in Exchange Server 2010 Service Pack 2 (SP2) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="166d3-124">This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="166d3-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="166d3-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="166d3-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="166d3-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="166d3-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="166d3-127">Schema name</span></span>  <br/> |<span data-ttu-id="166d3-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="166d3-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="166d3-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="166d3-129">Validation file</span></span>  <br/> |<span data-ttu-id="166d3-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="166d3-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="166d3-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="166d3-131">Can be empty</span></span>  <br/> |<span data-ttu-id="166d3-132">False</span><span class="sxs-lookup"><span data-stu-id="166d3-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="166d3-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="166d3-133">See also</span></span>



- [<span data-ttu-id="166d3-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="166d3-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="166d3-135">Creating Contacts (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="166d3-135">Creating Contacts (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)

