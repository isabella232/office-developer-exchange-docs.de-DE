---
title: StringSetting (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: bf7096d8-42d4-4bf5-bbdd-851af2754000
description: Das StringSetting-Element darstellt, dessen Wert vom Typ String ist, eine benutzereinstellung für den.
ms.openlocfilehash: af2c8ed243182e3491723be172ae162554250951
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831606"
---
# <a name="stringsetting-soap"></a><span data-ttu-id="17399-103">StringSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="17399-103">StringSetting (SOAP)</span></span>

<span data-ttu-id="17399-104">Das **StringSetting** -Element darstellt, dessen Wert vom Typ String ist, eine benutzereinstellung für den.</span><span class="sxs-lookup"><span data-stu-id="17399-104">The **StringSetting** element represents a user setting the value of which is of type string.</span></span> 
  
```XML
<StringSetting>
   <Name/>
   <Value/>
</StringSetting>
```

 <span data-ttu-id="17399-105">**StringSetting**</span><span class="sxs-lookup"><span data-stu-id="17399-105">**StringSetting**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="17399-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="17399-106">Attributes and elements</span></span>

<span data-ttu-id="17399-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="17399-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="17399-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="17399-108">Attributes</span></span>

<span data-ttu-id="17399-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="17399-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="17399-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="17399-110">Child elements</span></span>

|<span data-ttu-id="17399-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="17399-111">**Element**</span></span>|<span data-ttu-id="17399-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="17399-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="17399-113">Name (SOAP)</span><span class="sxs-lookup"><span data-stu-id="17399-113">Name (SOAP)</span></span>](name-soap.md) <br/> |<span data-ttu-id="17399-114">Stellt einen Einstellung Benutzernamen an.</span><span class="sxs-lookup"><span data-stu-id="17399-114">Represents a user setting name.</span></span>  <br/> |
|[<span data-ttu-id="17399-115">Wert (SOAP)</span><span class="sxs-lookup"><span data-stu-id="17399-115">Value (SOAP)</span></span>](value-soap.md) <br/> |<span data-ttu-id="17399-116">Stellt einen Benutzer Einstellung-Wert.</span><span class="sxs-lookup"><span data-stu-id="17399-116">Represents a user setting value.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="17399-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="17399-117">Parent elements</span></span>

<span data-ttu-id="17399-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="17399-118">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="17399-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="17399-119">Text value</span></span>

<span data-ttu-id="17399-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="17399-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="17399-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="17399-121">Remarks</span></span>

<span data-ttu-id="17399-122">Der Typ **StringSetting** erweitert den **UserSetting** -Typ.</span><span class="sxs-lookup"><span data-stu-id="17399-122">The **StringSetting** type extends the **UserSetting** type.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="17399-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="17399-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="17399-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="17399-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="17399-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="17399-125">Schema Name</span></span>  <br/> |<span data-ttu-id="17399-126">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="17399-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="17399-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="17399-127">Validation File</span></span>  <br/> |<span data-ttu-id="17399-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="17399-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="17399-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="17399-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="17399-130">True</span><span class="sxs-lookup"><span data-stu-id="17399-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="17399-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17399-131">See also</span></span>



[<span data-ttu-id="17399-132">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="17399-132">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="17399-133">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="17399-133">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
  
[<span data-ttu-id="17399-134">GetFederationInformation-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="17399-134">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

