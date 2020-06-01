---
title: Name (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Name
api_type:
- schema
ms.assetid: 98c58c53-9acc-4e89-9fcf-03f1b05abee1
description: Das Name-Element stellt den Namen eines Postfachbenutzers dar.
ms.openlocfilehash: db6eb547b5c848dc31bbaa377692989b16771673
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "44466927"
---
# <a name="name-emailaddresstype"></a><span data-ttu-id="365ec-103">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="365ec-103">Name (EmailAddressType)</span></span>

<span data-ttu-id="365ec-104">Das **Name** -Element stellt den Namen eines Postfachbenutzers dar.</span><span class="sxs-lookup"><span data-stu-id="365ec-104">The **Name** element represents the name of a mailbox user.</span></span> 
  
```xml
<Name/>
```

<span data-ttu-id="365ec-105">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="365ec-105">**string**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="365ec-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="365ec-106">Attributes and elements</span></span>

<span data-ttu-id="365ec-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="365ec-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="365ec-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="365ec-108">Attributes</span></span>

<span data-ttu-id="365ec-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="365ec-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="365ec-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="365ec-110">Child elements</span></span>

<span data-ttu-id="365ec-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="365ec-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="365ec-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="365ec-112">Parent elements</span></span>

|<span data-ttu-id="365ec-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="365ec-113">**Element**</span></span>|<span data-ttu-id="365ec-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="365ec-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="365ec-115">Postfach</span><span class="sxs-lookup"><span data-stu-id="365ec-115">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="365ec-116">Identifiziert eine vollständig aufgelöste e-Mail-Adresse.</span><span class="sxs-lookup"><span data-stu-id="365ec-116">Identifies a fully resolved e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="365ec-117">RoomList</span><span class="sxs-lookup"><span data-stu-id="365ec-117">RoomList</span></span>](roomlist.md) <br/> |<span data-ttu-id="365ec-118">Gibt eine Liste von Besprechungsräumen an.</span><span class="sxs-lookup"><span data-stu-id="365ec-118">Identifies a list of meeting rooms.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="365ec-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="365ec-119">Text value</span></span>

<span data-ttu-id="365ec-120">Ein Textwert, der eine Zeichenfolge darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="365ec-120">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="365ec-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="365ec-121">Remarks</span></span>

<span data-ttu-id="365ec-122">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="365ec-122">This element is optional.</span></span> <span data-ttu-id="365ec-123">Das **Name** -Element ist in den Typen **AttachmentType**, **Email**Name und **e-** MailType vorhanden.</span><span class="sxs-lookup"><span data-stu-id="365ec-123">The **Name** element exists in the **AttachmentType**, **EmailAddressType**, and **EmailAddress** types.</span></span> <span data-ttu-id="365ec-124">Das **Name** -Element im **Adress** typentyp wird im Thema [Name (Email-Element)](name-emailaddress.md) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="365ec-124">The **Name** element in the **EmailAddress** type is described in the [Name (EmailAddress)](name-emailaddress.md) element topic.</span></span> 
  
<span data-ttu-id="365ec-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="365ec-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="365ec-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="365ec-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="365ec-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="365ec-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="365ec-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="365ec-128">Schema Name</span></span>  <br/> |<span data-ttu-id="365ec-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="365ec-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="365ec-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="365ec-130">Validation File</span></span>  <br/> |<span data-ttu-id="365ec-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="365ec-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="365ec-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="365ec-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="365ec-133">False</span><span class="sxs-lookup"><span data-stu-id="365ec-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="365ec-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="365ec-134">See also</span></span>

- [<span data-ttu-id="365ec-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="365ec-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

