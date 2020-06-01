---
title: User Response (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd
description: Das User Response-Element stellt eine Antwort auf eine GetUserSettings-Anforderung für einen einzelnen Benutzer dar.
ms.openlocfilehash: 73848cb19d9c859e07216f354965ac4051d0d20c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "44468901"
---
# <a name="userresponse-soap"></a><span data-ttu-id="507aa-103">User Response (SOAP)</span><span class="sxs-lookup"><span data-stu-id="507aa-103">UserResponse (SOAP)</span></span>

<span data-ttu-id="507aa-104">Das **User Response** -Element stellt eine Antwort auf eine GetUserSettings-Anforderung für einen einzelnen Benutzer dar.</span><span class="sxs-lookup"><span data-stu-id="507aa-104">The **UserResponse** element represents a response to a GetUserSettings request for an individual user.</span></span> 
  
```XML
<UserResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <RedirectTarget/>
   <UserSettingErrors/>
   <UserSettings/>
</UserResponse>
```

 <span data-ttu-id="507aa-105">**User Response**</span><span class="sxs-lookup"><span data-stu-id="507aa-105">**UserResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="507aa-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="507aa-106">Attributes and elements</span></span>

<span data-ttu-id="507aa-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="507aa-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="507aa-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="507aa-108">Attributes</span></span>

<span data-ttu-id="507aa-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="507aa-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="507aa-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="507aa-110">Child elements</span></span>

|<span data-ttu-id="507aa-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="507aa-111">**Element**</span></span>|<span data-ttu-id="507aa-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="507aa-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="507aa-113">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="507aa-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="507aa-114">Stellt einen Fehlercode dar, der vom AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="507aa-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="507aa-115">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="507aa-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="507aa-116">Stellt eine Meldung dar, die einem Fehlercode zugeordnet ist, der vom AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="507aa-116">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="507aa-117">RedirectTarget (SOAP)</span><span class="sxs-lookup"><span data-stu-id="507aa-117">RedirectTarget (SOAP)</span></span>](redirecttarget-soap.md) <br/> |<span data-ttu-id="507aa-118">Enthält das Ziel der Umleitungs-URL oder e-Mail-Adresse.</span><span class="sxs-lookup"><span data-stu-id="507aa-118">Contains the target of the redirection URL or email address.</span></span>  <br/> |
|[<span data-ttu-id="507aa-119">UserSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="507aa-119">UserSettingErrors (SOAP)</span></span>](usersettingerrors-soap.md) <br/> |<span data-ttu-id="507aa-120">Stellt eine Sammlung von Informationen zu Einstellungen dar, die nicht zurückgegeben werden konnten.</span><span class="sxs-lookup"><span data-stu-id="507aa-120">Represents a collection of information about settings that could not be returned.</span></span>  <br/> |
|[<span data-ttu-id="507aa-121">UserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="507aa-121">UserSettings (SOAP)</span></span>](usersettings-soap.md) <br/> |<span data-ttu-id="507aa-122">Die angeforderten Einstellungen für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="507aa-122">The requested settings for the user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="507aa-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="507aa-123">Parent elements</span></span>

|<span data-ttu-id="507aa-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="507aa-124">**Element**</span></span>|<span data-ttu-id="507aa-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="507aa-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="507aa-126">ArrayOfUserResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="507aa-126">ArrayOfUserResponse (SOAP)</span></span>](arrayofuserresponse-soap.md) <br/> |<span data-ttu-id="507aa-127">Enthält ein Array von Benutzer Antworten.</span><span class="sxs-lookup"><span data-stu-id="507aa-127">Contains an array of user responses.</span></span>  <br/> |
|[<span data-ttu-id="507aa-128">UserResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="507aa-128">UserResponses (SOAP)</span></span>](userresponses-soap.md) <br/> |<span data-ttu-id="507aa-129">Enthält die Konfigurationseinstellungen für jeden angeforderten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="507aa-129">Contains the configuration settings for each requested user.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="507aa-130">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="507aa-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="507aa-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="507aa-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="507aa-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="507aa-132">Schema Name</span></span>  <br/> |<span data-ttu-id="507aa-133">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="507aa-133">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="507aa-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="507aa-134">Validation File</span></span>  <br/> |<span data-ttu-id="507aa-135">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="507aa-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="507aa-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="507aa-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="507aa-137">True</span><span class="sxs-lookup"><span data-stu-id="507aa-137">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="507aa-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="507aa-138">See also</span></span>



[<span data-ttu-id="507aa-139">XML-Elemente der SOAP-AutoErmittlung für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="507aa-139">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

