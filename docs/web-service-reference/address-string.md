---
title: Address (Zeichenfolge)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Address
api_type:
- schema
ms.assetid: a3cdfcbd-d0c5-46d6-8daa-52405fc63ff0
description: Das Address-Element stellt die e-Mail-Adresse des Postfachbenutzers dar.
ms.openlocfilehash: 839107050f22df5c00cb4dea9c531563df52933d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463643"
---
# <a name="address-string"></a><span data-ttu-id="49802-103">Address (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="49802-103">Address (string)</span></span>

<span data-ttu-id="49802-104">Das **Address** -Element stellt die e-Mail-Adresse des Postfachbenutzers dar.</span><span class="sxs-lookup"><span data-stu-id="49802-104">The **Address** element represents the e-mail address of the mailbox user.</span></span> 
  
```xml
<Address>...</Address>
```

 <span data-ttu-id="49802-105">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="49802-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="49802-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="49802-106">Attributes and elements</span></span>

<span data-ttu-id="49802-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="49802-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="49802-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="49802-108">Attributes</span></span>

<span data-ttu-id="49802-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="49802-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="49802-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="49802-110">Child elements</span></span>

<span data-ttu-id="49802-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="49802-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="49802-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="49802-112">Parent elements</span></span>

|<span data-ttu-id="49802-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="49802-113">**Element**</span></span>|<span data-ttu-id="49802-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="49802-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="49802-115">E-Mail (e-Mail-Adresse)</span><span class="sxs-lookup"><span data-stu-id="49802-115">Email (EmailAddressType)</span></span>](email-emailaddresstype.md) <br/> |<span data-ttu-id="49802-116">Gibt die e-Mail-Adresse des MailboxData-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="49802-116">Specifies the e-mail address of the MailboxData object.</span></span> <span data-ttu-id="49802-117">Dieses Element wird im GetUserAvailability- [Vorgang](getuseravailability-operation.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="49802-117">This element is used in the [GetUserAvailability operation](getuseravailability-operation.md).</span></span><br/><br/> <span data-ttu-id="49802-118">Es folgt der XPath für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="49802-118">The following is the XPath to this element:</span></span><br/><br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData[i]/Email` <br/> |
|[<span data-ttu-id="49802-119">Postfach (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="49802-119">Mailbox (Availability)</span></span>](mailbox-availability.md) <br/> | <span data-ttu-id="49802-120">Stellt den Postfachbenutzer für eine SetUserOofSettings-oder GetUserOofSettings-Anforderung dar.</span><span class="sxs-lookup"><span data-stu-id="49802-120">Represents the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span><br/><br/>  <span data-ttu-id="49802-121">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="49802-121">The following are the XPath expressions to this element:</span></span><br/><br/>  `/GetUserOofSettingsRequest/Mailbox` <br/>  `/SetUserOofSettingsRequest/Mailbox` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="49802-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="49802-122">Text value</span></span>

<span data-ttu-id="49802-123">Wenn dieses Element verwendet wird, ist ein Textwert erforderlich.</span><span class="sxs-lookup"><span data-stu-id="49802-123">A text value is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="49802-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49802-124">Remarks</span></span>

<span data-ttu-id="49802-125">Dieses Element kann höchstens einmal im [e-Mail-Element (Epost)](email-emailaddresstype.md) und im [Postfachelement (Availability)](mailbox-availability.md) vorkommen.</span><span class="sxs-lookup"><span data-stu-id="49802-125">This element can occur at most one time in the [Email (EmailAddressType)](email-emailaddresstype.md) element and the [Mailbox (Availability)](mailbox-availability.md) element.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="49802-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="49802-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="49802-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="49802-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="49802-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="49802-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="49802-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="49802-129">Schema Name</span></span>  <br/> |<span data-ttu-id="49802-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="49802-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="49802-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="49802-131">Validation File</span></span>  <br/> |<span data-ttu-id="49802-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="49802-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="49802-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="49802-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="49802-134">False</span><span class="sxs-lookup"><span data-stu-id="49802-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="49802-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49802-135">See also</span></span>

- [<span data-ttu-id="49802-136">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="49802-136">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="49802-137">GetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="49802-137">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
- [<span data-ttu-id="49802-138">SetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="49802-138">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)
- [<span data-ttu-id="49802-139">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="49802-139">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="49802-140">GetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="49802-140">GetUserOofSettingsRequest</span></span>](getuseroofsettingsrequest.md)
- [<span data-ttu-id="49802-141">SetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="49802-141">SetUserOofSettingsRequest</span></span>](setuseroofsettingsrequest.md)
- [<span data-ttu-id="49802-142">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="49802-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

