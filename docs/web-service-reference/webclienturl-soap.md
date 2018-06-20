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
description: Das WebClientUrl-Element darstellt, die URL eines Exchange Web-Clients.
ms.openlocfilehash: 649845018acee1706a96f9e37475a6d5c5fa0aa7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839526"
---
# <a name="webclienturl-soap"></a><span data-ttu-id="06dbd-103">WebClientUrl (SOAP)</span><span class="sxs-lookup"><span data-stu-id="06dbd-103">WebClientUrl (SOAP)</span></span>

<span data-ttu-id="06dbd-104">Das **WebClientUrl** -Element darstellt, die URL eines Exchange Web-Clients.</span><span class="sxs-lookup"><span data-stu-id="06dbd-104">The **WebClientUrl** element represents the URL of an Exchange web client.</span></span> 
  
[<span data-ttu-id="06dbd-105">UserSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="06dbd-105">UserSetting (SOAP)</span></span>](usersetting-soap.md)
  
[<span data-ttu-id="06dbd-106">WebClientUrls (SOAP)</span><span class="sxs-lookup"><span data-stu-id="06dbd-106">WebClientUrls (SOAP)</span></span>](webclienturls-soap.md)
  
[<span data-ttu-id="06dbd-107">WebClientUrl (SOAP)</span><span class="sxs-lookup"><span data-stu-id="06dbd-107">WebClientUrl (SOAP)</span></span>](webclienturl-soap.md)
  
```XML
<WebClientUrl>
    <AuthenticationMethods/>
    <Url/>
</WebClientUrl>
```

 <span data-ttu-id="06dbd-108">**WebClientUrl**</span><span class="sxs-lookup"><span data-stu-id="06dbd-108">**WebClientUrl**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="06dbd-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="06dbd-109">Attributes and elements</span></span>

<span data-ttu-id="06dbd-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="06dbd-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="06dbd-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="06dbd-111">Attributes</span></span>

<span data-ttu-id="06dbd-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="06dbd-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="06dbd-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="06dbd-113">Child elements</span></span>

|<span data-ttu-id="06dbd-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="06dbd-114">**Element**</span></span>|<span data-ttu-id="06dbd-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="06dbd-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="06dbd-116">AuthenticationMethods (SOAP)</span><span class="sxs-lookup"><span data-stu-id="06dbd-116">AuthenticationMethods (SOAP)</span></span>](authenticationmethods-soap.md) <br/> |<span data-ttu-id="06dbd-117">Stellt die Authentifizierungsmethode beim Zugriff auf die angegebene URL verwenden.</span><span class="sxs-lookup"><span data-stu-id="06dbd-117">Represents the authentication method to use when accessing the specified URL.</span></span>  <br/> |
|[<span data-ttu-id="06dbd-118">URL (SOAP)</span><span class="sxs-lookup"><span data-stu-id="06dbd-118">Url (SOAP)</span></span>](url-soap.md) <br/> |<span data-ttu-id="06dbd-119">Stellt die Webadresse für die URL an.</span><span class="sxs-lookup"><span data-stu-id="06dbd-119">Represents the web address for the URL.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="06dbd-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="06dbd-120">Parent elements</span></span>

|<span data-ttu-id="06dbd-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="06dbd-121">**Element**</span></span>|<span data-ttu-id="06dbd-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="06dbd-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="06dbd-123">WebClientUrls (SOAP)</span><span class="sxs-lookup"><span data-stu-id="06dbd-123">WebClientUrls (SOAP)</span></span>](webclienturls-soap.md) <br/> |<span data-ttu-id="06dbd-124">Stellt eine benutzereinstellung für, die eine Sammlung von **WebClientUrl** Elementen enthält.</span><span class="sxs-lookup"><span data-stu-id="06dbd-124">Represents a user setting that contains a collection of **WebClientUrl** elements.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="06dbd-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="06dbd-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="06dbd-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="06dbd-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="06dbd-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="06dbd-127">Schema Name</span></span>  <br/> |<span data-ttu-id="06dbd-128">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="06dbd-128">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="06dbd-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="06dbd-129">Validation File</span></span>  <br/> |<span data-ttu-id="06dbd-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="06dbd-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="06dbd-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="06dbd-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="06dbd-132">True</span><span class="sxs-lookup"><span data-stu-id="06dbd-132">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="06dbd-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06dbd-133">See also</span></span>



[<span data-ttu-id="06dbd-134">URL (SOAP)</span><span class="sxs-lookup"><span data-stu-id="06dbd-134">Url (SOAP)</span></span>](url-soap.md)
  
[<span data-ttu-id="06dbd-135">WebClientUrls (SOAP)</span><span class="sxs-lookup"><span data-stu-id="06dbd-135">WebClientUrls (SOAP)</span></span>](webclienturls-soap.md)

