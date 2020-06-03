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
description: Das GetUserSettingsResponse-Element stellt eine Antwort auf eine GetUserSettings-Vorgang (SOAP)-Anforderung dar.
ms.openlocfilehash: a41a195a003789ddaef81f844e47aad689df0937
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530148"
---
# <a name="getusersettingsresponse-soap"></a><span data-ttu-id="41851-103">GetUserSettingsResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="41851-103">GetUserSettingsResponse (SOAP)</span></span>

<span data-ttu-id="41851-104">Das **GetUserSettingsResponse** -Element stellt eine Antwort auf eine [GetUserSettings-Vorgang (SOAP)-](getusersettings-operation-soap.md) Anforderung dar.</span><span class="sxs-lookup"><span data-stu-id="41851-104">The **GetUserSettingsResponse** element represents a response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request.</span></span> 
  
```XML
<GetUserSettingsResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <UserResponses/>
</GetUserSettingsResponse>
```

 <span data-ttu-id="41851-105">**GetUserSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="41851-105">**GetUserSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="41851-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="41851-106">Attributes and elements</span></span>

<span data-ttu-id="41851-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="41851-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="41851-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="41851-108">Attributes</span></span>

<span data-ttu-id="41851-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="41851-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="41851-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="41851-110">Child elements</span></span>

|<span data-ttu-id="41851-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="41851-111">**Element**</span></span>|<span data-ttu-id="41851-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="41851-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="41851-113">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="41851-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="41851-114">Stellt einen Fehlercode dar, der vom AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="41851-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="41851-115">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="41851-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="41851-116">Stellt eine Meldung dar, die einem Fehlercode zugeordnet ist, der vom AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="41851-116">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="41851-117">UserResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="41851-117">UserResponses (SOAP)</span></span>](userresponses-soap.md) <br/> |<span data-ttu-id="41851-118">Enthält die Konfigurationseinstellungen für jeden angeforderten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="41851-118">Contains the configuration settings for each requested user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="41851-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="41851-119">Parent elements</span></span>

<span data-ttu-id="41851-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="41851-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="41851-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="41851-121">Text value</span></span>

<span data-ttu-id="41851-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="41851-122">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="41851-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="41851-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="41851-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="41851-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="41851-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="41851-125">Schema Name</span></span>  <br/> |<span data-ttu-id="41851-126">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="41851-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="41851-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="41851-127">Validation File</span></span>  <br/> |<span data-ttu-id="41851-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="41851-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="41851-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="41851-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="41851-130">True</span><span class="sxs-lookup"><span data-stu-id="41851-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="41851-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41851-131">See also</span></span>



[<span data-ttu-id="41851-132">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="41851-132">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

