---
title: Benutzer (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 4e051617-4eea-47d0-871a-ea1f17a0f711
description: Das users-Element stellt eine Auflistung von e-Mail-Adressen der Benutzer dar, für die Einstellungen abgerufen werden sollen.
ms.openlocfilehash: 851447a2918e365b7c5d8812a61c9d425d26ffa2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461898"
---
# <a name="users-soap"></a><span data-ttu-id="5602a-103">Benutzer (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5602a-103">Users (SOAP)</span></span>

<span data-ttu-id="5602a-104">Das **Users** -Element stellt eine Auflistung von e-Mail-Adressen der Benutzer dar, für die Einstellungen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5602a-104">The **Users** element represents a collection of e-mail addresses of the users for whom settings should be retrieved.</span></span> 
  
```XML
<Users>
   <User/>
</Users>
```

 <span data-ttu-id="5602a-105">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="5602a-105">**Users**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5602a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5602a-106">Attributes and elements</span></span>

<span data-ttu-id="5602a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5602a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5602a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5602a-108">Attributes</span></span>

<span data-ttu-id="5602a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5602a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5602a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5602a-110">Child elements</span></span>

|<span data-ttu-id="5602a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="5602a-111">**Element**</span></span>|<span data-ttu-id="5602a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5602a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5602a-113">Benutzer (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5602a-113">User (SOAP)</span></span>](user-soap.md) <br/> |<span data-ttu-id="5602a-114">Stellt die e-Mail-Adresse eines Benutzers dar.</span><span class="sxs-lookup"><span data-stu-id="5602a-114">Represents the e-mail address of a user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5602a-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5602a-115">Parent elements</span></span>

|<span data-ttu-id="5602a-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="5602a-116">**Element**</span></span>|<span data-ttu-id="5602a-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5602a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5602a-118">GetUserSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5602a-118">GetUserSettingsRequest (SOAP)</span></span>](getusersettingsrequest-soap.md) <br/> |<span data-ttu-id="5602a-119">Stellt eine Anforderung zum Abrufen der angegebenen Einstellungen für einen oder mehrere Benutzer dar.</span><span class="sxs-lookup"><span data-stu-id="5602a-119">Represents a request to retrieve specified settings for one or more users.</span></span>  <br/> |
|[<span data-ttu-id="5602a-120">Request (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5602a-120">Request (SOAP)</span></span>](request-soap.md) <br/> |<span data-ttu-id="5602a-121">Enthält die angeforderten Konfigurationseinstellungen und die Zielbenutzer.</span><span class="sxs-lookup"><span data-stu-id="5602a-121">Contains the requested configuration settings and the target users.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5602a-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="5602a-122">Text value</span></span>

<span data-ttu-id="5602a-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="5602a-123">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5602a-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="5602a-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5602a-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="5602a-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="5602a-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5602a-126">Schema Name</span></span>  <br/> |<span data-ttu-id="5602a-127">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="5602a-127">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="5602a-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5602a-128">Validation File</span></span>  <br/> |<span data-ttu-id="5602a-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="5602a-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5602a-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5602a-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="5602a-131">True</span><span class="sxs-lookup"><span data-stu-id="5602a-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5602a-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5602a-132">See also</span></span>



[<span data-ttu-id="5602a-133">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5602a-133">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

