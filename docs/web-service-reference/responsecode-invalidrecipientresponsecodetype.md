---
title: ResponseCode (InvalidRecipientResponseCodeType)
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
description: Das ResponseCode-Element enthält Informationen dazu, warum der Empfänger ungültig.
ms.openlocfilehash: 3bff99dd1ac6603ce31d5ceb074e73ef48190bb2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831186"
---
# <a name="responsecode-invalidrecipientresponsecodetype"></a><span data-ttu-id="414bb-103">ResponseCode (InvalidRecipientResponseCodeType)</span><span class="sxs-lookup"><span data-stu-id="414bb-103">ResponseCode (InvalidRecipientResponseCodeType)</span></span>

<span data-ttu-id="414bb-104">Das **ResponseCode** -Element enthält Informationen dazu, warum der Empfänger ungültig.</span><span class="sxs-lookup"><span data-stu-id="414bb-104">The **ResponseCode** element provides information about why the recipient is invalid.</span></span> 
  
```XML
<ResponseCode>OtherError or RecipientOrganizationNotFederated or CannotObtainTokenFromSTS or SystemPolicyBlocksSharingWithThisRecipient or RecipientOrganizationFederatedWithUnknownTokenIssuer</ResponseCode>
```

 <span data-ttu-id="414bb-105">**InvalidRecipientResponseCodeType**</span><span class="sxs-lookup"><span data-stu-id="414bb-105">**InvalidRecipientResponseCodeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="414bb-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="414bb-106">Attributes and elements</span></span>

<span data-ttu-id="414bb-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="414bb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="414bb-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="414bb-108">Attributes</span></span>

<span data-ttu-id="414bb-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="414bb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="414bb-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="414bb-110">Child elements</span></span>

<span data-ttu-id="414bb-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="414bb-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="414bb-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="414bb-112">Parent elements</span></span>

|<span data-ttu-id="414bb-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="414bb-113">**Element**</span></span>|<span data-ttu-id="414bb-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="414bb-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="414bb-115">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="414bb-115">InvalidRecipient</span></span>](invalidrecipient.md) <br/> |<span data-ttu-id="414bb-116">Enthält die SMTP-Adresse des ungültige Empfänger und Informationen dazu, warum der Empfänger ungültig.</span><span class="sxs-lookup"><span data-stu-id="414bb-116">Contains the SMTP address of the invalid recipient and information about why the recipient is invalid.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="414bb-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="414bb-117">Text value</span></span>

<span data-ttu-id="414bb-118">Die folgende Tabelle enthält die möglichen Werte für das **ResponseCode** -Element.</span><span class="sxs-lookup"><span data-stu-id="414bb-118">The following table lists the possible values for the **ResponseCode** element.</span></span> 
  
|<span data-ttu-id="414bb-119">**Code**</span><span class="sxs-lookup"><span data-stu-id="414bb-119">**Code**</span></span>|<span data-ttu-id="414bb-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="414bb-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="414bb-121">OtherError</span><span class="sxs-lookup"><span data-stu-id="414bb-121">OtherError</span></span>  <br/> |<span data-ttu-id="414bb-122">Gibt an, dass der Fehler nicht von einem anderen Fehlercode Antwort angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="414bb-122">Indicates that the error is not specified by another error response code.</span></span>  <br/> |
|<span data-ttu-id="414bb-123">RecipientOrganizationNotFederated</span><span class="sxs-lookup"><span data-stu-id="414bb-123">RecipientOrganizationNotFederated</span></span>  <br/> |<span data-ttu-id="414bb-124">Gibt an, dass eine Beziehung mit der Organisation im SMTP-e-Mail-Adresse des Empfängers angegebene nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="414bb-124">Indicates that a sharing relationship is not available with the organization specified in the recipient's SMTP e-mail address.</span></span>  <br/> |
|<span data-ttu-id="414bb-125">CannotObtainTokenFromSTS</span><span class="sxs-lookup"><span data-stu-id="414bb-125">CannotObtainTokenFromSTS</span></span>  <br/> |<span data-ttu-id="414bb-126">Gibt an, dass beim Abrufen von ein Sicherheitstoken vom Sicherheitstokendienst-Server ein Problem aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="414bb-126">Indicates that there was a problem obtaining a security token from the token server.</span></span>  <br/> |
|<span data-ttu-id="414bb-127">SystemPolicyBlocksSharingWithThisRecipient</span><span class="sxs-lookup"><span data-stu-id="414bb-127">SystemPolicyBlocksSharingWithThisRecipient</span></span>  <br/> |<span data-ttu-id="414bb-128">Gibt an, dass der Systemadministrator eine Systemrichtlinie festgelegt hat, die Freigabe für den angegebenen Empfänger blockiert.</span><span class="sxs-lookup"><span data-stu-id="414bb-128">Indicates that the system administrator has set a system policy that blocks sharing with the specified recipient.</span></span>  <br/> |
|<span data-ttu-id="414bb-129">RecipientOrganizationFederatedWithUnknownTokenIssuer</span><span class="sxs-lookup"><span data-stu-id="414bb-129">RecipientOrganizationFederatedWithUnknownTokenIssuer</span></span>  <br/> |<span data-ttu-id="414bb-130">Gibt an, dass des Sicherheitstokendiensts, die von den angegebenen Empfänger verwendet ist unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="414bb-130">Indicates that the secure token service that is used by the specified recipient is unknown.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="414bb-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="414bb-131">Remarks</span></span>

<span data-ttu-id="414bb-132">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="414bb-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="414bb-133">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="414bb-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="414bb-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="414bb-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="414bb-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="414bb-135">Schema Name</span></span>  <br/> |<span data-ttu-id="414bb-136">Schematypen</span><span class="sxs-lookup"><span data-stu-id="414bb-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="414bb-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="414bb-137">Validation File</span></span>  <br/> |<span data-ttu-id="414bb-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="414bb-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="414bb-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="414bb-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="414bb-140">False</span><span class="sxs-lookup"><span data-stu-id="414bb-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="414bb-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="414bb-141">See also</span></span>



[<span data-ttu-id="414bb-142">GetSharingMetadata-Vorgang</span><span class="sxs-lookup"><span data-stu-id="414bb-142">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="414bb-143">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="414bb-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

