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
description: Das Element stellt die Identität eines einzelnen Benutzers.
ms.openlocfilehash: a8dcb22f5c74a9622f978f34e48146115351fe82
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839435"
---
# <a name="user-soap"></a><span data-ttu-id="b6bba-103">Benutzer (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b6bba-103">User (SOAP)</span></span>

<span data-ttu-id="b6bba-104">**Das Element** stellt die Identität eines einzelnen Benutzers.</span><span class="sxs-lookup"><span data-stu-id="b6bba-104">The **User** element represents the identity of a single user.</span></span> 
  
```XML
<User>
    <LegacyDN/>
    <Mailbox/>
    <RequestedSettings/>
</User>
```

 <span data-ttu-id="b6bba-105">**User**</span><span class="sxs-lookup"><span data-stu-id="b6bba-105">**User**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b6bba-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b6bba-106">Attributes and elements</span></span>

<span data-ttu-id="b6bba-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b6bba-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b6bba-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b6bba-108">Attributes</span></span>

<span data-ttu-id="b6bba-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b6bba-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b6bba-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b6bba-110">Child elements</span></span>

|<span data-ttu-id="b6bba-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b6bba-111">**Element**</span></span>|<span data-ttu-id="b6bba-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b6bba-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b6bba-113">LegacyDN (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b6bba-113">LegacyDN (SOAP)</span></span>](legacydn-soap.md) <br/> |<span data-ttu-id="b6bba-114">Alternative Postfach legacy-DN darstellt.</span><span class="sxs-lookup"><span data-stu-id="b6bba-114">Represents the alternate mailbox legacy distinguished name.</span></span>  <br/> |
|[<span data-ttu-id="b6bba-115">Postfach (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b6bba-115">Mailbox (SOAP)</span></span>](mailbox-soap.md) <br/> |<span data-ttu-id="b6bba-116">Enthält die e-Mail-Adresse des Benutzers an, der ermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="b6bba-116">Contains the e-mail address of the user to be discovered.</span></span>  <br/> |
|[<span data-ttu-id="b6bba-117">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b6bba-117">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="b6bba-118">Enthält die Namen der angeforderten Konfigurationseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="b6bba-118">Contains the names of the requested configuration settings.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b6bba-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b6bba-119">Parent elements</span></span>

|<span data-ttu-id="b6bba-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="b6bba-120">**Element**</span></span>|<span data-ttu-id="b6bba-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b6bba-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b6bba-122">Benutzer (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b6bba-122">Users (SOAP)</span></span>](users-soap.md) <br/> |<span data-ttu-id="b6bba-123">Stellt eine Auflistung von **Elementen** .</span><span class="sxs-lookup"><span data-stu-id="b6bba-123">Represents a collection of **User** elements.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b6bba-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="b6bba-124">Text value</span></span>

<span data-ttu-id="b6bba-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="b6bba-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b6bba-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b6bba-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b6bba-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="b6bba-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="b6bba-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b6bba-128">Schema Name</span></span>  <br/> |<span data-ttu-id="b6bba-129">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="b6bba-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="b6bba-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b6bba-130">Validation File</span></span>  <br/> |<span data-ttu-id="b6bba-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b6bba-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b6bba-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b6bba-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="b6bba-133">True</span><span class="sxs-lookup"><span data-stu-id="b6bba-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b6bba-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6bba-134">See also</span></span>



[<span data-ttu-id="b6bba-135">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b6bba-135">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="b6bba-136">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b6bba-136">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
  
[<span data-ttu-id="b6bba-137">GetFederationInformation-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b6bba-137">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

