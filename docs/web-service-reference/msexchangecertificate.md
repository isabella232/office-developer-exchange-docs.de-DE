---
title: MSExchangeCertificate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c514f22f-be3e-4cad-ac56-bdff6bafcee6
description: Das MSExchangeCertificate-Element enthält einen Wert, der das Microsoft Exchange-Zertifikat eines Kontakts codiert.
ms.openlocfilehash: 8d07198012485b5c6d22e1fb4721890bf9a5eb39
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830498"
---
# <a name="msexchangecertificate"></a><span data-ttu-id="054fd-103">MSExchangeCertificate</span><span class="sxs-lookup"><span data-stu-id="054fd-103">MSExchangeCertificate</span></span>

<span data-ttu-id="054fd-104">Das **MSExchangeCertificate** -Element enthält einen Wert, der das Microsoft Exchange-Zertifikat eines Kontakts codiert.</span><span class="sxs-lookup"><span data-stu-id="054fd-104">The **MSExchangeCertificate** element contains a value that encodes the Microsoft Exchange certificate of a contact.</span></span> 
  
```XML
<MSExchangeCertificate/>
```

 <span data-ttu-id="054fd-105">**ArrayOfBinaryType**</span><span class="sxs-lookup"><span data-stu-id="054fd-105">**ArrayOfBinaryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="054fd-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="054fd-106">Attributes and elements</span></span>

<span data-ttu-id="054fd-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="054fd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="054fd-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="054fd-108">Attributes</span></span>

<span data-ttu-id="054fd-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="054fd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="054fd-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="054fd-110">Child elements</span></span>

|<span data-ttu-id="054fd-111">**Elementname**</span><span class="sxs-lookup"><span data-stu-id="054fd-111">**Element name**</span></span>|<span data-ttu-id="054fd-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="054fd-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="054fd-113">Base64Binary</span><span class="sxs-lookup"><span data-stu-id="054fd-113">Base64Binary</span></span>](base64binary.md) <br/> |<span data-ttu-id="054fd-114">Enthält einen Base64-codierten Wert.</span><span class="sxs-lookup"><span data-stu-id="054fd-114">Contains a Base64-encoded value.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="054fd-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="054fd-115">Parent elements</span></span>

|<span data-ttu-id="054fd-116">**Elementname**</span><span class="sxs-lookup"><span data-stu-id="054fd-116">**Element name**</span></span>|<span data-ttu-id="054fd-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="054fd-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="054fd-118">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="054fd-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="054fd-119">Stellt ein Kontaktelement im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="054fd-119">Represents a contact item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="054fd-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="054fd-120">Text value</span></span>

<span data-ttu-id="054fd-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="054fd-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="054fd-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="054fd-122">Remarks</span></span>

<span data-ttu-id="054fd-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="054fd-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="054fd-124">Dieses Element wurde in Exchange Server 2010 Service Pack 2 (SP2) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="054fd-124">This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="054fd-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="054fd-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="054fd-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="054fd-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="054fd-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="054fd-127">Schema name</span></span>  <br/> |<span data-ttu-id="054fd-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="054fd-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="054fd-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="054fd-129">Validation file</span></span>  <br/> |<span data-ttu-id="054fd-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="054fd-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="054fd-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="054fd-131">Can be empty</span></span>  <br/> |<span data-ttu-id="054fd-132">False</span><span class="sxs-lookup"><span data-stu-id="054fd-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="054fd-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="054fd-133">See also</span></span>



- [<span data-ttu-id="054fd-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="054fd-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="054fd-135">Creating Contacts (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="054fd-135">Creating Contacts (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)

