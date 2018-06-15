---
title: UserResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd
description: Das Element UserResponse stellt eine Antwort auf eine Anforderung GetUserSettings für einen einzelnen Benutzer.
ms.openlocfilehash: 6fcd82e06916df5acdd317cb44161c1b69e58574
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19839460"
---
# <a name="userresponse-soap"></a><span data-ttu-id="b7cdf-103">UserResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b7cdf-103">UserResponse (SOAP)</span></span>

<span data-ttu-id="b7cdf-104">Das Element **UserResponse** stellt eine Antwort auf eine Anforderung GetUserSettings für einen einzelnen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="b7cdf-104">The **UserResponse** element represents a response to a GetUserSettings request for an individual user.</span></span> 
  
```XML
<UserResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <RedirectTarget/>
   <UserSettingErrors/>
   <UserSettings/>
</UserResponse>
```

 <span data-ttu-id="b7cdf-105">**UserResponse**</span><span class="sxs-lookup"><span data-stu-id="b7cdf-105">**UserResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b7cdf-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b7cdf-106">Attributes and elements</span></span>

<span data-ttu-id="b7cdf-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b7cdf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b7cdf-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b7cdf-108">Attributes</span></span>

<span data-ttu-id="b7cdf-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b7cdf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b7cdf-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b7cdf-110">Child elements</span></span>

|<span data-ttu-id="b7cdf-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b7cdf-111">**Element**</span></span>|<span data-ttu-id="b7cdf-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b7cdf-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7cdf-113">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b7cdf-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="b7cdf-114">Stellt einen Fehlercode, der von den AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b7cdf-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="b7cdf-115">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b7cdf-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="b7cdf-116">Stellt eine Nachricht, die ein Fehlercode zugeordnet ist, die von den AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b7cdf-116">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="b7cdf-117">RedirectTarget (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b7cdf-117">RedirectTarget (SOAP)</span></span>](redirecttarget-soap.md) <br/> |<span data-ttu-id="b7cdf-118">Das Ziel der Umleitung URL oder die e-Mail-Adresse enthält.</span><span class="sxs-lookup"><span data-stu-id="b7cdf-118">Contains the target of the redirection URL or email address.</span></span>  <br/> |
|[<span data-ttu-id="b7cdf-119">UserSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b7cdf-119">UserSettingErrors (SOAP)</span></span>](usersettingerrors-soap.md) <br/> |<span data-ttu-id="b7cdf-120">Stellt eine Auflistung von Informationen zu Einstellungen, die nicht zurückgegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="b7cdf-120">Represents a collection of information about settings that could not be returned.</span></span>  <br/> |
|[<span data-ttu-id="b7cdf-121">UserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b7cdf-121">UserSettings (SOAP)</span></span>](usersettings-soap.md) <br/> |<span data-ttu-id="b7cdf-122">Der angeforderten Einstellungen für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="b7cdf-122">The requested settings for the user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b7cdf-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b7cdf-123">Parent elements</span></span>

|<span data-ttu-id="b7cdf-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="b7cdf-124">**Element**</span></span>|<span data-ttu-id="b7cdf-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b7cdf-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7cdf-126">ArrayOfUserResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b7cdf-126">ArrayOfUserResponse (SOAP)</span></span>](arrayofuserresponse-soap.md) <br/> |<span data-ttu-id="b7cdf-127">Enthält ein Array der Benutzerantworten.</span><span class="sxs-lookup"><span data-stu-id="b7cdf-127">Contains an array of user responses.</span></span>  <br/> |
|[<span data-ttu-id="b7cdf-128">UserResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b7cdf-128">UserResponses (SOAP)</span></span>](userresponses-soap.md) <br/> |<span data-ttu-id="b7cdf-129">Enthält die Konfigurationseinstellungen für jeden angeforderten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="b7cdf-129">Contains the configuration settings for each requested user.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="b7cdf-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b7cdf-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7cdf-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="b7cdf-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="b7cdf-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b7cdf-132">Schema Name</span></span>  <br/> |<span data-ttu-id="b7cdf-133">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="b7cdf-133">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="b7cdf-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b7cdf-134">Validation File</span></span>  <br/> |<span data-ttu-id="b7cdf-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b7cdf-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b7cdf-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b7cdf-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="b7cdf-137">True</span><span class="sxs-lookup"><span data-stu-id="b7cdf-137">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b7cdf-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7cdf-138">See also</span></span>



[<span data-ttu-id="b7cdf-139">SOAP-Autodiscover XML-Elemente für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="b7cdf-139">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

