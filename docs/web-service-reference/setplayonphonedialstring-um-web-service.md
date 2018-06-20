---
title: SetPlayOnPhoneDialString (UM-Webdienst)
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
description: Das SetPlayOnPhoneDialString-Element definiert eine Anforderung an die Standardzeichenfolge Zugriffsnummern für PlayOnPhone-Vorgang (UM-Webdienst) festgelegt und PlayOnPhoneGreeting-Vorgang (UM-Webdienst) Anfragen.
ms.openlocfilehash: fd82dc6ef0dd90a2318da93191f657005b7a5c87
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831450"
---
# <a name="setplayonphonedialstring-um-web-service"></a><span data-ttu-id="89c47-103">SetPlayOnPhoneDialString (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="89c47-103">SetPlayOnPhoneDialString (UM web service)</span></span>

<span data-ttu-id="89c47-104">Das **SetPlayOnPhoneDialString** -Element definiert eine Anforderung an die Standardzeichenfolge Zugriffsnummern für [PlayOnPhone-Vorgang (UM-Webdienst)](playonphone-operation-um-web-service.md) und einen optimalen [Betrieb der PlayOnPhoneGreeting (UM-Webdienst)](playonphonegreeting-operation-um-web-service.md) Anforderungen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="89c47-104">The **SetPlayOnPhoneDialString** element defines a request to set the default dial string for [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md) and [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md) requests.</span></span> 
  
[<span data-ttu-id="89c47-105">SetPlayOnPhoneDialString (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="89c47-105">SetPlayOnPhoneDialString (UM web service)</span></span>](setplayonphonedialstring-um-web-service.md)
  
```xml
<SetPlayOnPhoneDialString>
  <dialString>   </dialString>
</SetPlayOnPhoneDialString>
```

 <span data-ttu-id="89c47-106">**complexType**</span><span class="sxs-lookup"><span data-stu-id="89c47-106">**complexType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="89c47-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="89c47-107">Attributes and elements</span></span>

<span data-ttu-id="89c47-108">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="89c47-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="89c47-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="89c47-109">Attributes</span></span>

<span data-ttu-id="89c47-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="89c47-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="89c47-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="89c47-111">Child elements</span></span>

|<span data-ttu-id="89c47-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="89c47-112">**Element**</span></span>|<span data-ttu-id="89c47-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="89c47-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="89c47-114">DialString (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="89c47-114">dialString (UM web service)</span></span>](dialstring-um-web-service.md) <br/> |<span data-ttu-id="89c47-115">Die Telefonnummer ein, die als Zeichenfolge für den Wählplan festgelegt.</span><span class="sxs-lookup"><span data-stu-id="89c47-115">The telephone number to set as the default dial string.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="89c47-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="89c47-116">Parent elements</span></span>

<span data-ttu-id="89c47-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="89c47-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="89c47-118">Textwert</span><span class="sxs-lookup"><span data-stu-id="89c47-118">Text value</span></span>

<span data-ttu-id="89c47-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="89c47-119">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="89c47-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="89c47-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="89c47-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="89c47-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="89c47-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="89c47-122">Schema Name</span></span>  <br/> |<span data-ttu-id="89c47-123">Nachrichten</span><span class="sxs-lookup"><span data-stu-id="89c47-123">Messages</span></span>  <br/> |
|<span data-ttu-id="89c47-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="89c47-124">Validation File</span></span>  <br/> |<span data-ttu-id="89c47-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="89c47-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="89c47-126">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="89c47-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="89c47-127">False</span><span class="sxs-lookup"><span data-stu-id="89c47-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="89c47-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89c47-128">See also</span></span>



[<span data-ttu-id="89c47-129">SetPlayOnPhoneDialString-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="89c47-129">SetPlayOnPhoneDialString operation (UM web service)</span></span>](setplayonphonedialstring-operation-um-web-service.md)

