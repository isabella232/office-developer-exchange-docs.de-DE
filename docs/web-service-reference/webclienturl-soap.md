---
title: WebClientUrl (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 7f8cb6d6-4aac-4a1f-8bec-2dcb90fc1df6
description: Das WebClientUrl-Element stellt die URL eines Exchange-Webclients dar.
ms.openlocfilehash: bcf9c8d4fe80de8af4c9500e5e850558a8451d4e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464973"
---
# <a name="webclienturl-soap"></a><span data-ttu-id="7251f-103">WebClientUrl (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7251f-103">WebClientUrl (SOAP)</span></span>

<span data-ttu-id="7251f-104">Das **WebClientUrl** -Element stellt die URL eines Exchange-Webclients dar.</span><span class="sxs-lookup"><span data-stu-id="7251f-104">The **WebClientUrl** element represents the URL of an Exchange web client.</span></span> 
  
[<span data-ttu-id="7251f-105">UserSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7251f-105">UserSetting (SOAP)</span></span>](usersetting-soap.md)
  
[<span data-ttu-id="7251f-106">WebClientUrls (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7251f-106">WebClientUrls (SOAP)</span></span>](webclienturls-soap.md)
  
[<span data-ttu-id="7251f-107">WebClientUrl (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7251f-107">WebClientUrl (SOAP)</span></span>](webclienturl-soap.md)
  
```XML
<WebClientUrl>
    <AuthenticationMethods/>
    <Url/>
</WebClientUrl>
```

 <span data-ttu-id="7251f-108">**WebClientUrl**</span><span class="sxs-lookup"><span data-stu-id="7251f-108">**WebClientUrl**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7251f-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7251f-109">Attributes and elements</span></span>

<span data-ttu-id="7251f-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7251f-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7251f-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="7251f-111">Attributes</span></span>

<span data-ttu-id="7251f-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="7251f-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7251f-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7251f-113">Child elements</span></span>

|<span data-ttu-id="7251f-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="7251f-114">**Element**</span></span>|<span data-ttu-id="7251f-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7251f-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7251f-116">AuthenticationMethods (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7251f-116">AuthenticationMethods (SOAP)</span></span>](authenticationmethods-soap.md) <br/> |<span data-ttu-id="7251f-117">Stellt die Authentifizierungsmethode dar, die beim Zugriff auf die angegebene URL verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7251f-117">Represents the authentication method to use when accessing the specified URL.</span></span>  <br/> |
|[<span data-ttu-id="7251f-118">URL (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7251f-118">Url (SOAP)</span></span>](url-soap.md) <br/> |<span data-ttu-id="7251f-119">Stellt die Webadresse für die URL dar.</span><span class="sxs-lookup"><span data-stu-id="7251f-119">Represents the web address for the URL.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7251f-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7251f-120">Parent elements</span></span>

|<span data-ttu-id="7251f-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="7251f-121">**Element**</span></span>|<span data-ttu-id="7251f-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7251f-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7251f-123">WebClientUrls (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7251f-123">WebClientUrls (SOAP)</span></span>](webclienturls-soap.md) <br/> |<span data-ttu-id="7251f-124">Stellt eine Benutzereinstellung dar, die eine Auflistung von **WebClientUrl** -Elementen enthält.</span><span class="sxs-lookup"><span data-stu-id="7251f-124">Represents a user setting that contains a collection of **WebClientUrl** elements.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="7251f-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="7251f-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7251f-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="7251f-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="7251f-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7251f-127">Schema Name</span></span>  <br/> |<span data-ttu-id="7251f-128">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="7251f-128">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="7251f-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7251f-129">Validation File</span></span>  <br/> |<span data-ttu-id="7251f-130">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="7251f-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7251f-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7251f-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="7251f-132">True</span><span class="sxs-lookup"><span data-stu-id="7251f-132">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7251f-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7251f-133">See also</span></span>



[<span data-ttu-id="7251f-134">URL (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7251f-134">Url (SOAP)</span></span>](url-soap.md)
  
[<span data-ttu-id="7251f-135">WebClientUrls (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7251f-135">WebClientUrls (SOAP)</span></span>](webclienturls-soap.md)

