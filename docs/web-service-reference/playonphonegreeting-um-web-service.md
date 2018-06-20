---
title: PlayOnPhoneGreeting (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- PlayOnPhoneGreeting
api_type:
- schema
ms.assetid: 43eda596-3609-4e1b-8502-1db2636535cf
description: Das PlayOnPhoneGreeting-Element definiert eine Anforderung an einen Unified Messaging Begrüßung auf ein Telefon wiedergegeben werden sollen.
ms.openlocfilehash: c30140fc60b9e902517b4cc18deb9b61efa61e0c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830836"
---
# <a name="playonphonegreeting-um-web-service"></a><span data-ttu-id="83fe6-103">PlayOnPhoneGreeting (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="83fe6-103">PlayOnPhoneGreeting (UM web service)</span></span>

<span data-ttu-id="83fe6-104">Das **PlayOnPhoneGreeting** -Element definiert eine Anforderung an einen Unified Messaging Begrüßung auf ein Telefon wiedergegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="83fe6-104">The **PlayOnPhoneGreeting** element defines a request to play a Unified Messaging greeting on a telephone.</span></span> 
  
[<span data-ttu-id="83fe6-105">PlayOnPhoneGreeting (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="83fe6-105">PlayOnPhoneGreeting (UM web service)</span></span>](playonphonegreeting-um-web-service.md)
  
```xml
<PlayOnPhoneGreeting>
  <GreetingType/>
  <DialString/>
</PlayOnPhoneGreeting>
```

 <span data-ttu-id="83fe6-106">**complexType**</span><span class="sxs-lookup"><span data-stu-id="83fe6-106">**complexType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="83fe6-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="83fe6-107">Attributes and elements</span></span>

<span data-ttu-id="83fe6-108">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="83fe6-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="83fe6-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="83fe6-109">Attributes</span></span>

<span data-ttu-id="83fe6-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="83fe6-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="83fe6-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="83fe6-111">Child elements</span></span>

|<span data-ttu-id="83fe6-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="83fe6-112">**Element**</span></span>|<span data-ttu-id="83fe6-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="83fe6-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83fe6-114">GreetingType (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="83fe6-114">GreetingType (UM web service)</span></span>](greetingtype-um-web-service.md) <br/> |<span data-ttu-id="83fe6-115">Definiert den Typ der Grußformel aus, die in einer Anforderung [PlayOnPhoneGreeting-Vorgang (UM-Webdienst)](playonphonegreeting-operation-um-web-service.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="83fe6-115">Defines the type of greeting to use in a [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md) request.</span></span>  <br/> |
|[<span data-ttu-id="83fe6-116">DialString (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="83fe6-116">dialString (UM web service)</span></span>](dialstring-um-web-service.md) <br/> |<span data-ttu-id="83fe6-117">Enthält den Wert für die Rufnummer gewählt.</span><span class="sxs-lookup"><span data-stu-id="83fe6-117">Contains the value for the telephone number to dial.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="83fe6-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="83fe6-118">Parent elements</span></span>

<span data-ttu-id="83fe6-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="83fe6-119">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="83fe6-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="83fe6-120">Text value</span></span>

<span data-ttu-id="83fe6-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="83fe6-121">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="83fe6-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="83fe6-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="83fe6-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="83fe6-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="83fe6-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="83fe6-124">Schema Name</span></span>  <br/> |<span data-ttu-id="83fe6-125">Nachrichten</span><span class="sxs-lookup"><span data-stu-id="83fe6-125">Messages</span></span>  <br/> |
|<span data-ttu-id="83fe6-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="83fe6-126">Validation File</span></span>  <br/> |<span data-ttu-id="83fe6-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="83fe6-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="83fe6-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="83fe6-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="83fe6-129">False</span><span class="sxs-lookup"><span data-stu-id="83fe6-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="83fe6-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83fe6-130">See also</span></span>



[<span data-ttu-id="83fe6-131">PlayOnPhoneGreeting-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="83fe6-131">PlayOnPhoneGreeting operation (UM web service)</span></span>](playonphonegreeting-operation-um-web-service.md)

