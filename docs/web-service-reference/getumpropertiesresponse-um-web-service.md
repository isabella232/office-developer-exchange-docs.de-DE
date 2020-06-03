---
title: GetUMPropertiesResponse (um-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- GetUMPropertiesResponse
api_type:
- schema
ms.assetid: fcd93ce5-7403-46a9-b46e-56d2ebdd2f79
description: Das GetUMPropertiesResponse-Element definiert eine Antwort auf eine Anforderung des GetUMProperties-Vorgangs (um-Webdienst).
ms.openlocfilehash: 3247489a305c694c10764d7a0c6f02b1fad51ebf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459125"
---
# <a name="getumpropertiesresponse-um-web-service"></a><span data-ttu-id="45a6f-103">GetUMPropertiesResponse (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="45a6f-103">GetUMPropertiesResponse (UM web service)</span></span>

<span data-ttu-id="45a6f-104">Das **GetUMPropertiesResponse** -Element definiert eine Antwort auf eine Anforderung des [GetUMProperties-Vorgangs (um-Webdienst)](getumproperties-operation-um-web-service.md) .</span><span class="sxs-lookup"><span data-stu-id="45a6f-104">The **GetUMPropertiesResponse** element defines a response to a [GetUMProperties operation (UM web service)](getumproperties-operation-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="45a6f-105">GetUMPropertiesResponse (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="45a6f-105">GetUMPropertiesResponse (UM web service)</span></span>](getumpropertiesresponse-um-web-service.md)
  
```xml
<GetUMPropertiesResponse>
  <OofStatus/>
  <MissedCallNotificationEnabled/>
  <PlayOnPhoneDialString/>
  <TelephoneAccessNumbers/>
  <TelephoneAccessFolderEmail/>
</GetUMPropertiesResponse>
```

 <span data-ttu-id="45a6f-106">**UMProperties**</span><span class="sxs-lookup"><span data-stu-id="45a6f-106">**UMProperties**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="45a6f-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="45a6f-107">Attributes and elements</span></span>

<span data-ttu-id="45a6f-108">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="45a6f-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="45a6f-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="45a6f-109">Attributes</span></span>

<span data-ttu-id="45a6f-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="45a6f-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="45a6f-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="45a6f-111">Child elements</span></span>

|<span data-ttu-id="45a6f-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="45a6f-112">**Element**</span></span>|<span data-ttu-id="45a6f-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="45a6f-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="45a6f-114">MissedCallNotificationEnabled (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="45a6f-114">MissedCallNotificationEnabled (UM web service)</span></span>](missedcallnotificationenabled-um-web-service.md) <br/> |<span data-ttu-id="45a6f-115">Gibt an, ob Benachrichtigungen über verpasste Anrufe aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="45a6f-115">Indicates whether missed call notifications are enabled.</span></span>  <br/> |
|[<span data-ttu-id="45a6f-116">PlayOnPhoneDialString (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="45a6f-116">PlayOnPhoneDialString (UM web service)</span></span>](playonphonedialstring-um-web-service.md) <br/> |<span data-ttu-id="45a6f-117">Enthält die standardmäßige Wählzeichenfolge, die für den [PlayOnPhone-Vorgang (um-Webdienst)](playonphone-operation-um-web-service.md) und den [PlayOnPhoneGreeting-Vorgang (um-Webdienst)](playonphonegreeting-operation-um-web-service.md)verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="45a6f-117">Contains the default dial string to use for the [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md) and [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md).</span></span>  <br/> |
|[<span data-ttu-id="45a6f-118">TelephoneAccessNumbers (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="45a6f-118">TelephoneAccessNumbers (UM web service)</span></span>](telephoneaccessnumbers-um-web-service.md) <br/> |<span data-ttu-id="45a6f-119">Enthält die Liste der Telefonnummern, die der Benutzer für den Zugriff auf Unified Messaging über ein Telefon verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="45a6f-119">Contains the list of telephone numbers the user can use to access Unified Messaging via a telephone.</span></span>  <br/> |
|[<span data-ttu-id="45a6f-120">TelephoneAccessFolderEmail (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="45a6f-120">TelephoneAccessFolderEmail (UM web service)</span></span>](telephoneaccessfolderemail-um-web-service.md) <br/> |<span data-ttu-id="45a6f-121">Enthält den Bezeichner für den e-Mail-Ordner, aus dem Unified Messaging Nachrichten über das Telefon lesen kann.</span><span class="sxs-lookup"><span data-stu-id="45a6f-121">Contains the identifier for the e-mail folder from which Unified Messaging will read messages over the telephone.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="45a6f-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="45a6f-122">Parent elements</span></span>

<span data-ttu-id="45a6f-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="45a6f-123">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="45a6f-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="45a6f-124">Text value</span></span>

<span data-ttu-id="45a6f-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="45a6f-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="45a6f-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="45a6f-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="45a6f-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="45a6f-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="45a6f-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="45a6f-128">Schema Name</span></span>  <br/> |<span data-ttu-id="45a6f-129">Nachrichten</span><span class="sxs-lookup"><span data-stu-id="45a6f-129">Messages</span></span>  <br/> |
|<span data-ttu-id="45a6f-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="45a6f-130">Validation File</span></span>  <br/> |<span data-ttu-id="45a6f-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="45a6f-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="45a6f-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="45a6f-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="45a6f-133">False</span><span class="sxs-lookup"><span data-stu-id="45a6f-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="45a6f-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45a6f-134">See also</span></span>



[<span data-ttu-id="45a6f-135">GetUMProperties-Vorgang (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="45a6f-135">GetUMProperties operation (UM web service)</span></span>](getumproperties-operation-um-web-service.md)

