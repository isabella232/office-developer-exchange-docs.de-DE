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
description: Das Mailbox-Element stellt den Postfachbenutzer für eine SetUserOofSettings-oder GetUserOofSettings-Anforderung dar.
ms.openlocfilehash: 1bda6e8b90551b86b4e1c2711ac25693a65e5410
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458075"
---
# <a name="mailbox-availability"></a><span data-ttu-id="62500-103">Postfach (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="62500-103">Mailbox (Availability)</span></span>

<span data-ttu-id="62500-104">Das **Mailbox** -Element stellt den Postfachbenutzer für eine SetUserOofSettings-oder GetUserOofSettings-Anforderung dar.</span><span class="sxs-lookup"><span data-stu-id="62500-104">The **Mailbox** element represents the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span> 
  
```xml
<Mailbox>
   <Name>...</Name>
   <Address>...</Address>
   <RoutingType>...</RoutingType>
</Mailbox>
```

<span data-ttu-id="62500-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="62500-105">**EmailAddressType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="62500-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="62500-106">Attributes and elements</span></span>

<span data-ttu-id="62500-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="62500-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="62500-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="62500-108">Attributes</span></span>

<span data-ttu-id="62500-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="62500-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="62500-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="62500-110">Child elements</span></span>

|<span data-ttu-id="62500-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="62500-111">**Element**</span></span>|<span data-ttu-id="62500-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="62500-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="62500-113">Name (e-mailemail)</span><span class="sxs-lookup"><span data-stu-id="62500-113">Name (EmailAddress)</span></span>](name-emailaddress.md) <br/> |<span data-ttu-id="62500-114">Stellt den Anzeigenamen des Postfachbenutzers dar.</span><span class="sxs-lookup"><span data-stu-id="62500-114">Represents the display name of the mailbox user.</span></span> <span data-ttu-id="62500-115">Dieses Element ist in der SetUserOofSettingsRequest optional.</span><span class="sxs-lookup"><span data-stu-id="62500-115">This element is optional in the SetUserOofSettingsRequest.</span></span> <span data-ttu-id="62500-116">Das GetUserOofSettingsRequest-Objekt gibt dieses Element zurück.</span><span class="sxs-lookup"><span data-stu-id="62500-116">The GetUserOofSettingsRequest will return this element.</span></span>  <br/> |
|[<span data-ttu-id="62500-117">Address (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="62500-117">Address (string)</span></span>](address-string.md) <br/> |<span data-ttu-id="62500-118">Stellt die e-Mail-Adresse des Postfachbenutzers dar.</span><span class="sxs-lookup"><span data-stu-id="62500-118">Represents the e-mail address of the mailbox user.</span></span> <span data-ttu-id="62500-119">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="62500-119">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="62500-120">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="62500-120">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="62500-121">Stellt das Routingprotokoll für die Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="62500-121">Represents the routing protocol for the message.</span></span> <span data-ttu-id="62500-122">Dieses Element ist in der SetUserOofSettingsRequest optional.</span><span class="sxs-lookup"><span data-stu-id="62500-122">This element is optional in the SetUserOofSettingsRequest.</span></span> <span data-ttu-id="62500-123">Das GetUserOofSettingsRequest-Objekt gibt dieses Element zurück.</span><span class="sxs-lookup"><span data-stu-id="62500-123">The GetUserOofSettingsRequest will return this element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="62500-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="62500-124">Parent elements</span></span>

|<span data-ttu-id="62500-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="62500-125">**Element**</span></span>|<span data-ttu-id="62500-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="62500-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="62500-127">GetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="62500-127">GetUserOofSettingsRequest</span></span>](getuseroofsettingsrequest.md) <br/> |<span data-ttu-id="62500-128">Dient zum Abrufen der Abwesenheit (Out of Office, OOF) Einstellungen und Nachrichten eines Postfachbenutzers.</span><span class="sxs-lookup"><span data-stu-id="62500-128">Used to get a mailbox user's Out of Office (OOF) settings and messages.</span></span>  <br/> <span data-ttu-id="62500-129">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="62500-129">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserOofSettingsRequest` <br/> |
|[<span data-ttu-id="62500-130">SetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="62500-130">SetUserOofSettingsRequest</span></span>](setuseroofsettingsrequest.md) <br/> |<span data-ttu-id="62500-131">Wird verwendet, um die Abwesenheitseinstellungen und-Nachrichten eines Postfachbenutzers festzulegen.</span><span class="sxs-lookup"><span data-stu-id="62500-131">Used to set a mailbox user's OOF settings and messages.</span></span>  <br/> <span data-ttu-id="62500-132">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="62500-132">The following is the XPath expression to this element:</span></span>  <br/>  `/SetUserOofSettingsRequest` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62500-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62500-133">Remarks</span></span>

<span data-ttu-id="62500-134">Die e-Mail-Adresse wird verwendet, um den Kalenderordner zu identifizieren, der die Abwesenheitseinstellungen enthält.</span><span class="sxs-lookup"><span data-stu-id="62500-134">The e-mail address is used to identify the calendar folder that contains the OOF settings.</span></span> 
  
<span data-ttu-id="62500-135">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="62500-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="62500-136">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="62500-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="62500-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="62500-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="62500-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="62500-138">Schema Name</span></span>  <br/> |<span data-ttu-id="62500-139">Schematypen</span><span class="sxs-lookup"><span data-stu-id="62500-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="62500-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="62500-140">Validation File</span></span>  <br/> |<span data-ttu-id="62500-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="62500-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="62500-142">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="62500-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="62500-143">False</span><span class="sxs-lookup"><span data-stu-id="62500-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="62500-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62500-144">See also</span></span>

- [<span data-ttu-id="62500-145">GetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="62500-145">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
- [<span data-ttu-id="62500-146">SetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="62500-146">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

