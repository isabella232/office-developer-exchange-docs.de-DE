---
title: Postfach (Verfügbarkeit)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Mailbox
api_type:
- schema
ms.assetid: affd192e-8914-473f-9098-d9bdf898de2c
description: Das Postfach-Element stellt den Postfachbenutzer für eine SetUserOofSettings oder GetUserOofSettings anfordern.
ms.openlocfilehash: 2e901ae0df56542f56f247184254294735018468
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830254"
---
# <a name="mailbox-availability"></a><span data-ttu-id="f869f-103">Postfach (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="f869f-103">Mailbox (Availability)</span></span>

<span data-ttu-id="f869f-104">Das **Postfach** -Element stellt den Postfachbenutzer für eine SetUserOofSettings oder GetUserOofSettings anfordern.</span><span class="sxs-lookup"><span data-stu-id="f869f-104">The **Mailbox** element represents the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span> 
  
```xml
<Mailbox>
   <Name>...</Name>
   <Address>...</Address>
   <RoutingType>...</RoutingType>
</Mailbox>
```

<span data-ttu-id="f869f-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="f869f-105">**EmailAddressType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f869f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f869f-106">Attributes and elements</span></span>

<span data-ttu-id="f869f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f869f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f869f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f869f-108">Attributes</span></span>

<span data-ttu-id="f869f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f869f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f869f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f869f-110">Child elements</span></span>

|<span data-ttu-id="f869f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f869f-111">**Element**</span></span>|<span data-ttu-id="f869f-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f869f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f869f-113">Name (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="f869f-113">Name (EmailAddress)</span></span>](name-emailaddress.md) <br/> |<span data-ttu-id="f869f-114">Stellt den Anzeigenamen des Postfachbenutzers an.</span><span class="sxs-lookup"><span data-stu-id="f869f-114">Represents the display name of the mailbox user.</span></span> <span data-ttu-id="f869f-115">Dieses Element ist in der SetUserOofSettingsRequest optional.</span><span class="sxs-lookup"><span data-stu-id="f869f-115">This element is optional in the SetUserOofSettingsRequest.</span></span> <span data-ttu-id="f869f-116">Die GetUserOofSettingsRequest gibt dieses Element zurück.</span><span class="sxs-lookup"><span data-stu-id="f869f-116">The GetUserOofSettingsRequest will return this element.</span></span>  <br/> |
|[<span data-ttu-id="f869f-117">Adresse (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="f869f-117">Address (string)</span></span>](address-string.md) <br/> |<span data-ttu-id="f869f-118">Stellt die e-Mail-Adresse des Postfachbenutzers an.</span><span class="sxs-lookup"><span data-stu-id="f869f-118">Represents the e-mail address of the mailbox user.</span></span> <span data-ttu-id="f869f-119">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f869f-119">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="f869f-120">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="f869f-120">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="f869f-121">Stellt das routing-Protokoll für die Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="f869f-121">Represents the routing protocol for the message.</span></span> <span data-ttu-id="f869f-122">Dieses Element ist in der SetUserOofSettingsRequest optional.</span><span class="sxs-lookup"><span data-stu-id="f869f-122">This element is optional in the SetUserOofSettingsRequest.</span></span> <span data-ttu-id="f869f-123">Die GetUserOofSettingsRequest gibt dieses Element zurück.</span><span class="sxs-lookup"><span data-stu-id="f869f-123">The GetUserOofSettingsRequest will return this element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f869f-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f869f-124">Parent elements</span></span>

|<span data-ttu-id="f869f-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="f869f-125">**Element**</span></span>|<span data-ttu-id="f869f-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f869f-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f869f-127">GetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="f869f-127">GetUserOofSettingsRequest</span></span>](getuseroofsettingsrequest.md) <br/> |<span data-ttu-id="f869f-128">Zum Abrufen von Einstellungen von Office (ABWESEND) und Nachrichten eines Postfachbenutzers verwendet.</span><span class="sxs-lookup"><span data-stu-id="f869f-128">Used to get a mailbox user's Out of Office (OOF) settings and messages.</span></span>  <br/> <span data-ttu-id="f869f-129">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="f869f-129">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserOofSettingsRequest` <br/> |
|[<span data-ttu-id="f869f-130">SetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="f869f-130">SetUserOofSettingsRequest</span></span>](setuseroofsettingsrequest.md) <br/> |<span data-ttu-id="f869f-131">Verwendet, um eines Postfachbenutzers OOF Einstellungen und Nachrichten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="f869f-131">Used to set a mailbox user's OOF settings and messages.</span></span>  <br/> <span data-ttu-id="f869f-132">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="f869f-132">The following is the XPath expression to this element:</span></span>  <br/>  `/SetUserOofSettingsRequest` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f869f-133">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f869f-133">Remarks</span></span>

<span data-ttu-id="f869f-134">Die E-mail-Adresse wird verwendet, um den Kalenderordner zu identifizieren, der die OOF Einstellungen enthält.</span><span class="sxs-lookup"><span data-stu-id="f869f-134">The e-mail address is used to identify the calendar folder that contains the OOF settings.</span></span> 
  
<span data-ttu-id="f869f-135">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="f869f-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f869f-136">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f869f-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f869f-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="f869f-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f869f-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f869f-138">Schema Name</span></span>  <br/> |<span data-ttu-id="f869f-139">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f869f-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="f869f-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f869f-140">Validation File</span></span>  <br/> |<span data-ttu-id="f869f-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f869f-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f869f-142">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f869f-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="f869f-143">False</span><span class="sxs-lookup"><span data-stu-id="f869f-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f869f-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f869f-144">See also</span></span>

- [<span data-ttu-id="f869f-145">GetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f869f-145">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
- [<span data-ttu-id="f869f-146">SetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f869f-146">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

