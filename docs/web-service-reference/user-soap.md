---
title: Benutzer (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: c6bc0031-bc1d-41bd-84e4-9074a5b77012
description: Das User-Element stellt die Identität eines einzelnen Benutzers dar.
ms.openlocfilehash: f151ffa8050a10cdbb4562471d815f8692596cc3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456346"
---
# <a name="user-soap"></a><span data-ttu-id="3a0a8-103">Benutzer (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3a0a8-103">User (SOAP)</span></span>

<span data-ttu-id="3a0a8-104">Das **User** -Element stellt die Identität eines einzelnen Benutzers dar.</span><span class="sxs-lookup"><span data-stu-id="3a0a8-104">The **User** element represents the identity of a single user.</span></span> 
  
```XML
<User>
    <LegacyDN/>
    <Mailbox/>
    <RequestedSettings/>
</User>
```

 <span data-ttu-id="3a0a8-105">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="3a0a8-105">**User**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3a0a8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3a0a8-106">Attributes and elements</span></span>

<span data-ttu-id="3a0a8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3a0a8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3a0a8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3a0a8-108">Attributes</span></span>

<span data-ttu-id="3a0a8-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3a0a8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3a0a8-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3a0a8-110">Child elements</span></span>

|<span data-ttu-id="3a0a8-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3a0a8-111">**Element**</span></span>|<span data-ttu-id="3a0a8-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3a0a8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a0a8-113">LegacyDN (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3a0a8-113">LegacyDN (SOAP)</span></span>](legacydn-soap.md) <br/> |<span data-ttu-id="3a0a8-114">Stellt den Distinguished Name des alternativen Post Fach Legacy dar.</span><span class="sxs-lookup"><span data-stu-id="3a0a8-114">Represents the alternate mailbox legacy distinguished name.</span></span>  <br/> |
|[<span data-ttu-id="3a0a8-115">Postfach (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3a0a8-115">Mailbox (SOAP)</span></span>](mailbox-soap.md) <br/> |<span data-ttu-id="3a0a8-116">Enthält die e-Mail-Adresse des Benutzers, der ermittelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3a0a8-116">Contains the e-mail address of the user to be discovered.</span></span>  <br/> |
|[<span data-ttu-id="3a0a8-117">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3a0a8-117">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="3a0a8-118">Enthält die Namen der angeforderten Konfigurationseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="3a0a8-118">Contains the names of the requested configuration settings.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3a0a8-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3a0a8-119">Parent elements</span></span>

|<span data-ttu-id="3a0a8-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="3a0a8-120">**Element**</span></span>|<span data-ttu-id="3a0a8-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3a0a8-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a0a8-122">Benutzer (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3a0a8-122">Users (SOAP)</span></span>](users-soap.md) <br/> |<span data-ttu-id="3a0a8-123">Stellt eine Auflistung von **User** -Elementen dar.</span><span class="sxs-lookup"><span data-stu-id="3a0a8-123">Represents a collection of **User** elements.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3a0a8-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="3a0a8-124">Text value</span></span>

<span data-ttu-id="3a0a8-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="3a0a8-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3a0a8-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3a0a8-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3a0a8-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="3a0a8-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="3a0a8-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3a0a8-128">Schema Name</span></span>  <br/> |<span data-ttu-id="3a0a8-129">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="3a0a8-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="3a0a8-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3a0a8-130">Validation File</span></span>  <br/> |<span data-ttu-id="3a0a8-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="3a0a8-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3a0a8-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3a0a8-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="3a0a8-133">True</span><span class="sxs-lookup"><span data-stu-id="3a0a8-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3a0a8-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a0a8-134">See also</span></span>



[<span data-ttu-id="3a0a8-135">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3a0a8-135">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="3a0a8-136">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3a0a8-136">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
  
[<span data-ttu-id="3a0a8-137">GetFederationInformation-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3a0a8-137">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

