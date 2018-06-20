---
title: GetUserSettingsResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: e7cd470d-5861-41e7-9e66-73ef7a59700b
description: Das Element GetUserSettingsResponse stellt eine Antwort auf eine GetUserSettings-Vorgang (SOAP) an.
ms.openlocfilehash: 24dbfb1582f628fd0130aa82ea5f1beedd31b156
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829705"
---
# <a name="getusersettingsresponse-soap"></a><span data-ttu-id="10a0e-103">GetUserSettingsResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="10a0e-103">GetUserSettingsResponse (SOAP)</span></span>

<span data-ttu-id="10a0e-104">Das Element **GetUserSettingsResponse** stellt eine Antwort auf eine Anforderung [(SOAP) GetUserSettings-Vorgang](getusersettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="10a0e-104">The **GetUserSettingsResponse** element represents a response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request.</span></span> 
  
```XML
<GetUserSettingsResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <UserResponses/>
</GetUserSettingsResponse>
```

 <span data-ttu-id="10a0e-105">**GetUserSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="10a0e-105">**GetUserSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="10a0e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="10a0e-106">Attributes and elements</span></span>

<span data-ttu-id="10a0e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="10a0e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="10a0e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="10a0e-108">Attributes</span></span>

<span data-ttu-id="10a0e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="10a0e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="10a0e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="10a0e-110">Child elements</span></span>

|<span data-ttu-id="10a0e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="10a0e-111">**Element**</span></span>|<span data-ttu-id="10a0e-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="10a0e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="10a0e-113">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="10a0e-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="10a0e-114">Stellt einen Fehlercode, der von den AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="10a0e-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="10a0e-115">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="10a0e-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="10a0e-116">Stellt eine Nachricht, die ein Fehlercode zugeordnet ist, die von den AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="10a0e-116">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="10a0e-117">UserResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="10a0e-117">UserResponses (SOAP)</span></span>](userresponses-soap.md) <br/> |<span data-ttu-id="10a0e-118">Enthält die Konfigurationseinstellungen für jeden angeforderten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="10a0e-118">Contains the configuration settings for each requested user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="10a0e-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="10a0e-119">Parent elements</span></span>

<span data-ttu-id="10a0e-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="10a0e-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="10a0e-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="10a0e-121">Text value</span></span>

<span data-ttu-id="10a0e-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="10a0e-122">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="10a0e-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="10a0e-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="10a0e-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="10a0e-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="10a0e-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="10a0e-125">Schema Name</span></span>  <br/> |<span data-ttu-id="10a0e-126">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="10a0e-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="10a0e-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="10a0e-127">Validation File</span></span>  <br/> |<span data-ttu-id="10a0e-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="10a0e-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="10a0e-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="10a0e-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="10a0e-130">True</span><span class="sxs-lookup"><span data-stu-id="10a0e-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="10a0e-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10a0e-131">See also</span></span>



[<span data-ttu-id="10a0e-132">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="10a0e-132">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

