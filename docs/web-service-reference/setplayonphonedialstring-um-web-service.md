---
title: SetPlayOnPhoneDialString (um-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetPlayOnPhoneDialString
api_type:
- schema
ms.assetid: 513a5072-c3ac-405f-98c2-0ab982d0a360
description: Das SetPlayOnPhoneDialString-Element definiert eine Anforderung zum Festlegen der standardmäßigen Wählzeichenfolge für den PlayOnPhone-Vorgang (um-Webdienst) und für den PlayOnPhoneGreeting-Vorgang (um-Webdienstanforderungen).
ms.openlocfilehash: 40021e9dedafb5fafda91bf3612d8a6485dae8e7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458628"
---
# <a name="setplayonphonedialstring-um-web-service"></a><span data-ttu-id="e2533-103">SetPlayOnPhoneDialString (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="e2533-103">SetPlayOnPhoneDialString (UM web service)</span></span>

<span data-ttu-id="e2533-104">Das **SetPlayOnPhoneDialString** -Element definiert eine Anforderung zum Festlegen der standardmäßigen Wählzeichenfolge für den [PlayOnPhone-Vorgang (um-Webdienst)](playonphone-operation-um-web-service.md) und für den [PlayOnPhoneGreeting-Vorgang (um-Webdienstanforderungen)](playonphonegreeting-operation-um-web-service.md) .</span><span class="sxs-lookup"><span data-stu-id="e2533-104">The **SetPlayOnPhoneDialString** element defines a request to set the default dial string for [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md) and [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md) requests.</span></span> 
  
[<span data-ttu-id="e2533-105">SetPlayOnPhoneDialString (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="e2533-105">SetPlayOnPhoneDialString (UM web service)</span></span>](setplayonphonedialstring-um-web-service.md)
  
```xml
<SetPlayOnPhoneDialString>
  <dialString>   </dialString>
</SetPlayOnPhoneDialString>
```

 <span data-ttu-id="e2533-106">**complexType**</span><span class="sxs-lookup"><span data-stu-id="e2533-106">**complexType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e2533-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e2533-107">Attributes and elements</span></span>

<span data-ttu-id="e2533-108">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e2533-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e2533-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="e2533-109">Attributes</span></span>

<span data-ttu-id="e2533-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="e2533-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e2533-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e2533-111">Child elements</span></span>

|<span data-ttu-id="e2533-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="e2533-112">**Element**</span></span>|<span data-ttu-id="e2533-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e2533-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e2533-114">Wähl Dienst (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="e2533-114">dialString (UM web service)</span></span>](dialstring-um-web-service.md) <br/> |<span data-ttu-id="e2533-115">Die Telefonnummer, die als standardmäßige Wählzeichenfolge festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e2533-115">The telephone number to set as the default dial string.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e2533-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e2533-116">Parent elements</span></span>

<span data-ttu-id="e2533-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="e2533-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="e2533-118">Textwert</span><span class="sxs-lookup"><span data-stu-id="e2533-118">Text value</span></span>

<span data-ttu-id="e2533-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="e2533-119">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e2533-120">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e2533-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e2533-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="e2533-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e2533-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e2533-122">Schema Name</span></span>  <br/> |<span data-ttu-id="e2533-123">Nachrichten</span><span class="sxs-lookup"><span data-stu-id="e2533-123">Messages</span></span>  <br/> |
|<span data-ttu-id="e2533-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e2533-124">Validation File</span></span>  <br/> |<span data-ttu-id="e2533-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="e2533-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e2533-126">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e2533-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="e2533-127">False</span><span class="sxs-lookup"><span data-stu-id="e2533-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e2533-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2533-128">See also</span></span>



[<span data-ttu-id="e2533-129">SetPlayOnPhoneDialString-Vorgang (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="e2533-129">SetPlayOnPhoneDialString operation (UM web service)</span></span>](setplayonphonedialstring-operation-um-web-service.md)

