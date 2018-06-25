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
description: Das OofSettings-Element enthält die Einstellungen von Office (OOF).
ms.openlocfilehash: d71f068ff24af22da98b6b4de090ab26d3f74f26
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830649"
---
# <a name="oofsettings"></a><span data-ttu-id="d6115-103">OofSettings</span><span class="sxs-lookup"><span data-stu-id="d6115-103">OofSettings</span></span>

<span data-ttu-id="d6115-104">Das **OofSettings** -Element enthält die Einstellungen von Office (OOF).</span><span class="sxs-lookup"><span data-stu-id="d6115-104">The **OofSettings** element contains the Out of Office (OOF) settings.</span></span> 
  
[<span data-ttu-id="d6115-105">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="d6115-105">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md)
  
[<span data-ttu-id="d6115-106">OofSettings</span><span class="sxs-lookup"><span data-stu-id="d6115-106">OofSettings</span></span>](oofsettings.md)
  
```xml
<OofSettings>
   <OofState>...</OofState>
   <ExternalAudience>...</ExternalAudience>
   <Duration>...</Duration>
   <InternalReply>...</InternalReply>
   <ExternalReply>...</ExternalReply>
</OofSettings>
```

 <span data-ttu-id="d6115-107">**' UserOofSettings '**</span><span class="sxs-lookup"><span data-stu-id="d6115-107">**UserOofSettings**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d6115-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d6115-108">Attributes and elements</span></span>

<span data-ttu-id="d6115-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d6115-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d6115-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="d6115-110">Attributes</span></span>

<span data-ttu-id="d6115-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d6115-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d6115-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d6115-112">Child elements</span></span>

|<span data-ttu-id="d6115-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d6115-113">**Element**</span></span>|<span data-ttu-id="d6115-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6115-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d6115-115">OofState</span><span class="sxs-lookup"><span data-stu-id="d6115-115">OofState</span></span>](oofstate.md) <br/> |<span data-ttu-id="d6115-116">Enthält den Status des Benutzers OOF.</span><span class="sxs-lookup"><span data-stu-id="d6115-116">Contains the user's OOF state.</span></span>  <br/> |
|[<span data-ttu-id="d6115-117">ExternalAudience</span><span class="sxs-lookup"><span data-stu-id="d6115-117">ExternalAudience</span></span>](externalaudience.md) <br/> |<span data-ttu-id="d6115-118">Enthält einen Wert, der bestimmt, denen externe OOF Testnachrichten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="d6115-118">Contains a value that determines to whom external OOF messages are sent.</span></span>  <br/> |
|[<span data-ttu-id="d6115-119">Dauer (' UserOofSettings ')</span><span class="sxs-lookup"><span data-stu-id="d6115-119">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md) <br/> |<span data-ttu-id="d6115-120">Enthält die Dauer, für die der Status ABWESEND aktiviert ist, wenn das Element [OofState](oofstate.md) **geplant**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d6115-120">Contains the duration for which the OOF status is enabled if the [OofState](oofstate.md) element is set to **Scheduled**.</span></span> <span data-ttu-id="d6115-121">Wenn das Element [OofState](oofstate.md) auf **aktiviert** oder **deaktiviert**festgelegt ist, wird der Wert der dieses Element ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d6115-121">If the [OofState](oofstate.md) element is set to **Enabled** or **Disabled**, the value of this element is ignored.</span></span>  <br/> |
|[<span data-ttu-id="d6115-122">InternalReply</span><span class="sxs-lookup"><span data-stu-id="d6115-122">InternalReply</span></span>](internalreply.md) <br/> |<span data-ttu-id="d6115-123">Enthält die OOF Antwort an andere Benutzer in der Domäne oder der vertrauenswürdigen Domäne des Benutzers gesendet.</span><span class="sxs-lookup"><span data-stu-id="d6115-123">Contains the OOF response sent to other users in the user's domain or trusted domain.</span></span>  <br/> |
|[<span data-ttu-id="d6115-124">ExternalReply</span><span class="sxs-lookup"><span data-stu-id="d6115-124">ExternalReply</span></span>](externalreply.md) <br/> |<span data-ttu-id="d6115-125">Enthält die OOF Antwort an Adressen außerhalb der Domäne oder der vertrauenswürdigen Domänen des Empfängers gesendet.</span><span class="sxs-lookup"><span data-stu-id="d6115-125">Contains the OOF response sent to addresses outside the recipient's domain or trusted domains.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d6115-126">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d6115-126">Parent elements</span></span>

|<span data-ttu-id="d6115-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="d6115-127">**Element**</span></span>|<span data-ttu-id="d6115-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6115-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d6115-129">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="d6115-129">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md) <br/> |<span data-ttu-id="d6115-130">Enthält die Antwort Ergebnisse und OOF-Einstellungen für einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="d6115-130">Contains the response results and the OOF settings for a user.</span></span>  <br/> <span data-ttu-id="d6115-131">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="d6115-131">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserOofSettingsResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6115-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d6115-132">Remarks</span></span>

<span data-ttu-id="d6115-133">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d6115-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d6115-134">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d6115-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d6115-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="d6115-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d6115-136">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d6115-136">Schema Name</span></span>  <br/> |<span data-ttu-id="d6115-137">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d6115-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d6115-138">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d6115-138">Validation File</span></span>  <br/> |<span data-ttu-id="d6115-139">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d6115-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d6115-140">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d6115-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="d6115-141">False</span><span class="sxs-lookup"><span data-stu-id="d6115-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d6115-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6115-142">See also</span></span>



[<span data-ttu-id="d6115-143">GetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d6115-143">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
  
[<span data-ttu-id="d6115-144">SetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d6115-144">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

