---
title: OofSettings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OofSettings
api_type:
- schema
ms.assetid: 8f37d174-db11-427c-bbed-fdde754a60c7
description: Das OofSettings-Element enthält die Abwesenheit (Out of Office, OOF) Einstellungen.
ms.openlocfilehash: c1b214fd8bfab5b7a82d41a5187cf6e0fc4ba79c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467193"
---
# <a name="oofsettings"></a><span data-ttu-id="bed29-103">OofSettings</span><span class="sxs-lookup"><span data-stu-id="bed29-103">OofSettings</span></span>

<span data-ttu-id="bed29-104">Das **OofSettings** -Element enthält die Abwesenheit (Out of Office, OOF) Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="bed29-104">The **OofSettings** element contains the Out of Office (OOF) settings.</span></span> 
  
[<span data-ttu-id="bed29-105">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="bed29-105">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md)
  
[<span data-ttu-id="bed29-106">OofSettings</span><span class="sxs-lookup"><span data-stu-id="bed29-106">OofSettings</span></span>](oofsettings.md)
  
```xml
<OofSettings>
   <OofState>...</OofState>
   <ExternalAudience>...</ExternalAudience>
   <Duration>...</Duration>
   <InternalReply>...</InternalReply>
   <ExternalReply>...</ExternalReply>
</OofSettings>
```

 <span data-ttu-id="bed29-107">**UserOofSettings**</span><span class="sxs-lookup"><span data-stu-id="bed29-107">**UserOofSettings**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bed29-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bed29-108">Attributes and elements</span></span>

<span data-ttu-id="bed29-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bed29-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bed29-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="bed29-110">Attributes</span></span>

<span data-ttu-id="bed29-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="bed29-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bed29-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bed29-112">Child elements</span></span>

|<span data-ttu-id="bed29-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="bed29-113">**Element**</span></span>|<span data-ttu-id="bed29-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bed29-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bed29-115">OofState</span><span class="sxs-lookup"><span data-stu-id="bed29-115">OofState</span></span>](oofstate.md) <br/> |<span data-ttu-id="bed29-116">Enthält den Abwesenheitsstatus des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="bed29-116">Contains the user's OOF state.</span></span>  <br/> |
|[<span data-ttu-id="bed29-117">ExternalAudience</span><span class="sxs-lookup"><span data-stu-id="bed29-117">ExternalAudience</span></span>](externalaudience.md) <br/> |<span data-ttu-id="bed29-118">Enthält einen Wert, der bestimmt, an wen externe Abwesenheitsnachrichten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="bed29-118">Contains a value that determines to whom external OOF messages are sent.</span></span>  <br/> |
|[<span data-ttu-id="bed29-119">Dauer (UserOofSettings)</span><span class="sxs-lookup"><span data-stu-id="bed29-119">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md) <br/> |<span data-ttu-id="bed29-120">Enthält die Dauer, für die der Abwesenheitsstatus aktiviert ist, wenn das [OofState](oofstate.md) -Element auf **Scheduled**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bed29-120">Contains the duration for which the OOF status is enabled if the [OofState](oofstate.md) element is set to **Scheduled**.</span></span> <span data-ttu-id="bed29-121">Wenn das [OofState](oofstate.md) -Element auf **aktiviert** oder **deaktiviert**festgelegt ist, wird der Wert dieses Elements ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bed29-121">If the [OofState](oofstate.md) element is set to **Enabled** or **Disabled**, the value of this element is ignored.</span></span>  <br/> |
|[<span data-ttu-id="bed29-122">InternalReply</span><span class="sxs-lookup"><span data-stu-id="bed29-122">InternalReply</span></span>](internalreply.md) <br/> |<span data-ttu-id="bed29-123">Enthält die Abwesenheitsantwort, die an andere Benutzer in der Domäne des Benutzers oder der vertrauenswürdigen Domäne gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="bed29-123">Contains the OOF response sent to other users in the user's domain or trusted domain.</span></span>  <br/> |
|[<span data-ttu-id="bed29-124">ExternalReply</span><span class="sxs-lookup"><span data-stu-id="bed29-124">ExternalReply</span></span>](externalreply.md) <br/> |<span data-ttu-id="bed29-125">Enthält die Abwesenheitsantwort, die an Adressen außerhalb der Domäne des Empfängers oder vertrauenswürdiger Domänen gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="bed29-125">Contains the OOF response sent to addresses outside the recipient's domain or trusted domains.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bed29-126">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bed29-126">Parent elements</span></span>

|<span data-ttu-id="bed29-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="bed29-127">**Element**</span></span>|<span data-ttu-id="bed29-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bed29-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bed29-129">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="bed29-129">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md) <br/> |<span data-ttu-id="bed29-130">Enthält die Antwortergebnisse und die Abwesenheitseinstellungen für einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="bed29-130">Contains the response results and the OOF settings for a user.</span></span>  <br/> <span data-ttu-id="bed29-131">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="bed29-131">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserOofSettingsResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bed29-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bed29-132">Remarks</span></span>

<span data-ttu-id="bed29-133">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="bed29-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bed29-134">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="bed29-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bed29-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="bed29-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bed29-136">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="bed29-136">Schema Name</span></span>  <br/> |<span data-ttu-id="bed29-137">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="bed29-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="bed29-138">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="bed29-138">Validation File</span></span>  <br/> |<span data-ttu-id="bed29-139">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="bed29-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bed29-140">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="bed29-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="bed29-141">False</span><span class="sxs-lookup"><span data-stu-id="bed29-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bed29-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bed29-142">See also</span></span>



[<span data-ttu-id="bed29-143">GetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="bed29-143">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
  
[<span data-ttu-id="bed29-144">SetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="bed29-144">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

