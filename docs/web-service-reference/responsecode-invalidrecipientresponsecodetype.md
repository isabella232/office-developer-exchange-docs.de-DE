---
title: Response Code (InvalidRecipientResponseCodeType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResponseCode
api_type:
- schema
ms.assetid: 582e9caa-d2bc-4be1-a460-739294f9ef18
description: Das Response Code-Element enthält Informationen dazu, warum der Empfänger ungültig ist.
ms.openlocfilehash: d78de64de7725007ec51a55dad13d1cc892a25e6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529721"
---
# <a name="responsecode-invalidrecipientresponsecodetype"></a><span data-ttu-id="b4b2b-103">Response Code (InvalidRecipientResponseCodeType)</span><span class="sxs-lookup"><span data-stu-id="b4b2b-103">ResponseCode (InvalidRecipientResponseCodeType)</span></span>

<span data-ttu-id="b4b2b-104">Das **Response Code** -Element enthält Informationen dazu, warum der Empfänger ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="b4b2b-104">The **ResponseCode** element provides information about why the recipient is invalid.</span></span> 
  
```XML
<ResponseCode>OtherError or RecipientOrganizationNotFederated or CannotObtainTokenFromSTS or SystemPolicyBlocksSharingWithThisRecipient or RecipientOrganizationFederatedWithUnknownTokenIssuer</ResponseCode>
```

 <span data-ttu-id="b4b2b-105">**InvalidRecipientResponseCodeType**</span><span class="sxs-lookup"><span data-stu-id="b4b2b-105">**InvalidRecipientResponseCodeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b4b2b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b4b2b-106">Attributes and elements</span></span>

<span data-ttu-id="b4b2b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b4b2b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b4b2b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b4b2b-108">Attributes</span></span>

<span data-ttu-id="b4b2b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b4b2b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b4b2b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b4b2b-110">Child elements</span></span>

<span data-ttu-id="b4b2b-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b4b2b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b4b2b-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b4b2b-112">Parent elements</span></span>

|<span data-ttu-id="b4b2b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b4b2b-113">**Element**</span></span>|<span data-ttu-id="b4b2b-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b4b2b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b4b2b-115">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="b4b2b-115">InvalidRecipient</span></span>](invalidrecipient.md) <br/> |<span data-ttu-id="b4b2b-116">Enthält die SMTP-Adresse des ungültige Empfänger und Informationen dazu, warum der Empfänger ungültig.</span><span class="sxs-lookup"><span data-stu-id="b4b2b-116">Contains the SMTP address of the invalid recipient and information about why the recipient is invalid.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b4b2b-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="b4b2b-117">Text value</span></span>

<span data-ttu-id="b4b2b-118">In der folgenden Tabelle sind die möglichen Werte für das **Response Code** -Element aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b4b2b-118">The following table lists the possible values for the **ResponseCode** element.</span></span> 
  
|<span data-ttu-id="b4b2b-119">**Code**</span><span class="sxs-lookup"><span data-stu-id="b4b2b-119">**Code**</span></span>|<span data-ttu-id="b4b2b-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b4b2b-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b4b2b-121">OtherError</span><span class="sxs-lookup"><span data-stu-id="b4b2b-121">OtherError</span></span>  <br/> |<span data-ttu-id="b4b2b-122">Gibt an, dass der Fehler nicht durch einen anderen Fehlerantwort Code angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b4b2b-122">Indicates that the error is not specified by another error response code.</span></span>  <br/> |
|<span data-ttu-id="b4b2b-123">RecipientOrganizationNotFederated</span><span class="sxs-lookup"><span data-stu-id="b4b2b-123">RecipientOrganizationNotFederated</span></span>  <br/> |<span data-ttu-id="b4b2b-124">Gibt an, dass eine Freigabebeziehung für die in der SMTP-e-Mail-Adresse des Empfängers angegebene Organisation nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b4b2b-124">Indicates that a sharing relationship is not available with the organization specified in the recipient's SMTP e-mail address.</span></span>  <br/> |
|<span data-ttu-id="b4b2b-125">CannotObtainTokenFromSTS</span><span class="sxs-lookup"><span data-stu-id="b4b2b-125">CannotObtainTokenFromSTS</span></span>  <br/> |<span data-ttu-id="b4b2b-126">Gibt an, dass ein Problem beim Abrufen eines Sicherheitstokens vom tokenserver aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b4b2b-126">Indicates that there was a problem obtaining a security token from the token server.</span></span>  <br/> |
|<span data-ttu-id="b4b2b-127">SystemPolicyBlocksSharingWithThisRecipient</span><span class="sxs-lookup"><span data-stu-id="b4b2b-127">SystemPolicyBlocksSharingWithThisRecipient</span></span>  <br/> |<span data-ttu-id="b4b2b-128">Gibt an, dass der System Administrator eine Systemrichtlinie festgelegt hat, die die Freigabe für den angegebenen Empfänger blockiert.</span><span class="sxs-lookup"><span data-stu-id="b4b2b-128">Indicates that the system administrator has set a system policy that blocks sharing with the specified recipient.</span></span>  <br/> |
|<span data-ttu-id="b4b2b-129">RecipientOrganizationFederatedWithUnknownTokenIssuer</span><span class="sxs-lookup"><span data-stu-id="b4b2b-129">RecipientOrganizationFederatedWithUnknownTokenIssuer</span></span>  <br/> |<span data-ttu-id="b4b2b-130">Gibt an, dass der vom angegebenen Empfänger verwendete Secure Token Service unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="b4b2b-130">Indicates that the secure token service that is used by the specified recipient is unknown.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4b2b-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4b2b-131">Remarks</span></span>

<span data-ttu-id="b4b2b-132">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b4b2b-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b4b2b-133">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b4b2b-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b4b2b-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="b4b2b-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b4b2b-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b4b2b-135">Schema Name</span></span>  <br/> |<span data-ttu-id="b4b2b-136">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b4b2b-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="b4b2b-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b4b2b-137">Validation File</span></span>  <br/> |<span data-ttu-id="b4b2b-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b4b2b-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b4b2b-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b4b2b-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="b4b2b-140">False</span><span class="sxs-lookup"><span data-stu-id="b4b2b-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b4b2b-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4b2b-141">See also</span></span>



[<span data-ttu-id="b4b2b-142">GetSharingMetadata-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b4b2b-142">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="b4b2b-143">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b4b2b-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

