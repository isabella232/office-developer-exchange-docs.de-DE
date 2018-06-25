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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831450"
---
# <a name="setplayonphonedialstring-um-web-service"></a><span data-ttu-id="ac91a-103">SetPlayOnPhoneDialString (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="ac91a-103">SetPlayOnPhoneDialString (UM web service)</span></span>

<span data-ttu-id="ac91a-104">Das **SetPlayOnPhoneDialString** -Element definiert eine Anforderung an die Standardzeichenfolge Zugriffsnummern für [PlayOnPhone-Vorgang (UM-Webdienst)](playonphone-operation-um-web-service.md) und einen optimalen [Betrieb der PlayOnPhoneGreeting (UM-Webdienst)](playonphonegreeting-operation-um-web-service.md) Anforderungen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ac91a-104">The **SetPlayOnPhoneDialString** element defines a request to set the default dial string for [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md) and [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md) requests.</span></span> 
  
[<span data-ttu-id="ac91a-105">SetPlayOnPhoneDialString (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="ac91a-105">SetPlayOnPhoneDialString (UM web service)</span></span>](setplayonphonedialstring-um-web-service.md)
  
```xml
<SetPlayOnPhoneDialString>
  <dialString>   </dialString>
</SetPlayOnPhoneDialString>
```

 <span data-ttu-id="ac91a-106">**complexType**</span><span class="sxs-lookup"><span data-stu-id="ac91a-106">**complexType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ac91a-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ac91a-107">Attributes and elements</span></span>

<span data-ttu-id="ac91a-108">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ac91a-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ac91a-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="ac91a-109">Attributes</span></span>

<span data-ttu-id="ac91a-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="ac91a-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ac91a-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac91a-111">Child elements</span></span>

|<span data-ttu-id="ac91a-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="ac91a-112">**Element**</span></span>|<span data-ttu-id="ac91a-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ac91a-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ac91a-114">DialString (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="ac91a-114">dialString (UM web service)</span></span>](dialstring-um-web-service.md) <br/> |<span data-ttu-id="ac91a-115">Die Telefonnummer ein, die als Zeichenfolge für den Wählplan festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ac91a-115">The telephone number to set as the default dial string.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ac91a-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac91a-116">Parent elements</span></span>

<span data-ttu-id="ac91a-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="ac91a-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="ac91a-118">Textwert</span><span class="sxs-lookup"><span data-stu-id="ac91a-118">Text value</span></span>

<span data-ttu-id="ac91a-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="ac91a-119">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ac91a-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ac91a-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ac91a-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac91a-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ac91a-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ac91a-122">Schema Name</span></span>  <br/> |<span data-ttu-id="ac91a-123">Nachrichten</span><span class="sxs-lookup"><span data-stu-id="ac91a-123">Messages</span></span>  <br/> |
|<span data-ttu-id="ac91a-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ac91a-124">Validation File</span></span>  <br/> |<span data-ttu-id="ac91a-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ac91a-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ac91a-126">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ac91a-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="ac91a-127">False</span><span class="sxs-lookup"><span data-stu-id="ac91a-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ac91a-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac91a-128">See also</span></span>



[<span data-ttu-id="ac91a-129">SetPlayOnPhoneDialString-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="ac91a-129">SetPlayOnPhoneDialString operation (UM web service)</span></span>](setplayonphonedialstring-operation-um-web-service.md)

