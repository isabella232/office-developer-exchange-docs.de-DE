---
title: UserSMIMECertificate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66e6b4ba-368d-4469-bd47-e59441b7d64d
description: Das UserSMIMECertificate-Element enthält einen Wert, der das SMIME-Zertifikat eines Kontakts codiert.
ms.openlocfilehash: 7e2dbc6a9c8b04758ba99db036e237d8837850aa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467655"
---
# <a name="usersmimecertificate"></a><span data-ttu-id="b8d13-103">UserSMIMECertificate</span><span class="sxs-lookup"><span data-stu-id="b8d13-103">UserSMIMECertificate</span></span>

<span data-ttu-id="b8d13-104">Das **UserSMIMECertificate** -Element enthält einen Wert, der das SMIME-Zertifikat eines Kontakts codiert.</span><span class="sxs-lookup"><span data-stu-id="b8d13-104">The **UserSMIMECertificate** element contains a value that encodes a contact's SMIME certificate.</span></span> 
  
```XML
<UserSMIMECertificate/>
```

 <span data-ttu-id="b8d13-105">**ArrayOfBinaryType**</span><span class="sxs-lookup"><span data-stu-id="b8d13-105">**ArrayOfBinaryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b8d13-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b8d13-106">Attributes and elements</span></span>

<span data-ttu-id="b8d13-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b8d13-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b8d13-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b8d13-108">Attributes</span></span>

<span data-ttu-id="b8d13-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b8d13-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b8d13-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b8d13-110">Child elements</span></span>

|<span data-ttu-id="b8d13-111">**Elementname**</span><span class="sxs-lookup"><span data-stu-id="b8d13-111">**Element name**</span></span>|<span data-ttu-id="b8d13-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b8d13-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b8d13-113">Base64Binary</span><span class="sxs-lookup"><span data-stu-id="b8d13-113">Base64Binary</span></span>](base64binary.md) <br/> |<span data-ttu-id="b8d13-114">Enthält einen Base64-codierten Wert.</span><span class="sxs-lookup"><span data-stu-id="b8d13-114">Contains a Base64-encoded value.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b8d13-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b8d13-115">Parent elements</span></span>

|<span data-ttu-id="b8d13-116">**Elementname**</span><span class="sxs-lookup"><span data-stu-id="b8d13-116">**Element name**</span></span>|<span data-ttu-id="b8d13-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b8d13-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b8d13-118">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="b8d13-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="b8d13-119">Stellt ein Kontaktelement im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="b8d13-119">Represents a contact item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b8d13-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="b8d13-120">Text value</span></span>

<span data-ttu-id="b8d13-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="b8d13-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b8d13-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8d13-122">Remarks</span></span>

<span data-ttu-id="b8d13-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b8d13-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="b8d13-124">Dieses Element wurde in Exchange Server 2010 Service Pack 2 (SP2) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b8d13-124">This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b8d13-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b8d13-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b8d13-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="b8d13-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b8d13-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b8d13-127">Schema name</span></span>  <br/> |<span data-ttu-id="b8d13-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b8d13-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="b8d13-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b8d13-129">Validation file</span></span>  <br/> |<span data-ttu-id="b8d13-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b8d13-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b8d13-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b8d13-131">Can be empty</span></span>  <br/> |<span data-ttu-id="b8d13-132">False</span><span class="sxs-lookup"><span data-stu-id="b8d13-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b8d13-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8d13-133">See also</span></span>



- [<span data-ttu-id="b8d13-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b8d13-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="b8d13-135">Creating Contacts (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="b8d13-135">Creating Contacts (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)

