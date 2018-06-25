---
title: GetUMPropertiesResponse (UM-Webdienst)
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
description: Das GetUMPropertiesResponse-Element definiert eine Antwort auf eine GetUMProperties-Vorgang (UM-Webdienst) an.
ms.openlocfilehash: c0df872ad6b8e6541fa750ab87f4c1e5f0118b00
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829685"
---
# <a name="getumpropertiesresponse-um-web-service"></a><span data-ttu-id="1dcdb-103">GetUMPropertiesResponse (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="1dcdb-103">GetUMPropertiesResponse (UM web service)</span></span>

<span data-ttu-id="1dcdb-104">Das **GetUMPropertiesResponse** -Element definiert eine Antwort auf eine [GetUMProperties-Vorgang (UM-Webdienst)](getumproperties-operation-um-web-service.md) an.</span><span class="sxs-lookup"><span data-stu-id="1dcdb-104">The **GetUMPropertiesResponse** element defines a response to a [GetUMProperties operation (UM web service)](getumproperties-operation-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="1dcdb-105">GetUMPropertiesResponse (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="1dcdb-105">GetUMPropertiesResponse (UM web service)</span></span>](getumpropertiesresponse-um-web-service.md)
  
```xml
<GetUMPropertiesResponse>
  <OofStatus/>
  <MissedCallNotificationEnabled/>
  <PlayOnPhoneDialString/>
  <TelephoneAccessNumbers/>
  <TelephoneAccessFolderEmail/>
</GetUMPropertiesResponse>
```

 <span data-ttu-id="1dcdb-106">**UMProperties**</span><span class="sxs-lookup"><span data-stu-id="1dcdb-106">**UMProperties**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1dcdb-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1dcdb-107">Attributes and elements</span></span>

<span data-ttu-id="1dcdb-108">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1dcdb-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1dcdb-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="1dcdb-109">Attributes</span></span>

<span data-ttu-id="1dcdb-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="1dcdb-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1dcdb-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1dcdb-111">Child elements</span></span>

|<span data-ttu-id="1dcdb-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="1dcdb-112">**Element**</span></span>|<span data-ttu-id="1dcdb-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1dcdb-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1dcdb-114">MissedCallNotificationEnabled (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="1dcdb-114">MissedCallNotificationEnabled (UM web service)</span></span>](missedcallnotificationenabled-um-web-service.md) <br/> |<span data-ttu-id="1dcdb-115">Gibt an, ob Benachrichtigungen über verpasste Anrufe aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="1dcdb-115">Indicates whether missed call notifications are enabled.</span></span>  <br/> |
|[<span data-ttu-id="1dcdb-116">PlayOnPhoneDialString (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="1dcdb-116">PlayOnPhoneDialString (UM web service)</span></span>](playonphonedialstring-um-web-service.md) <br/> |<span data-ttu-id="1dcdb-117">Enthält die Standardzeichenfolge Zugriffsnummern für den [PlayOnPhone Betrieb (UM-Webdienst)](playonphone-operation-um-web-service.md) und [PlayOnPhoneGreeting-Vorgang (UM-Webdienst)](playonphonegreeting-operation-um-web-service.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="1dcdb-117">Contains the default dial string to use for the [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md) and [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md).</span></span>  <br/> |
|[<span data-ttu-id="1dcdb-118">TelephoneAccessNumbers (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="1dcdb-118">TelephoneAccessNumbers (UM web service)</span></span>](telephoneaccessnumbers-um-web-service.md) <br/> |<span data-ttu-id="1dcdb-119">Enthält die Liste von Telefonnummern, mit denen der Benutzer über ein Telefon Zugriff auf Unified Messaging.</span><span class="sxs-lookup"><span data-stu-id="1dcdb-119">Contains the list of telephone numbers the user can use to access Unified Messaging via a telephone.</span></span>  <br/> |
|[<span data-ttu-id="1dcdb-120">TelephoneAccessFolderEmail (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="1dcdb-120">TelephoneAccessFolderEmail (UM web service)</span></span>](telephoneaccessfolderemail-um-web-service.md) <br/> |<span data-ttu-id="1dcdb-121">Enthält den Bezeichner für den e-Mail-Ordner aus dem Unified Messaging Nachrichten über das Telefon gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="1dcdb-121">Contains the identifier for the e-mail folder from which Unified Messaging will read messages over the telephone.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1dcdb-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1dcdb-122">Parent elements</span></span>

<span data-ttu-id="1dcdb-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="1dcdb-123">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="1dcdb-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="1dcdb-124">Text value</span></span>

<span data-ttu-id="1dcdb-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="1dcdb-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1dcdb-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1dcdb-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1dcdb-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="1dcdb-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1dcdb-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1dcdb-128">Schema Name</span></span>  <br/> |<span data-ttu-id="1dcdb-129">Nachrichten</span><span class="sxs-lookup"><span data-stu-id="1dcdb-129">Messages</span></span>  <br/> |
|<span data-ttu-id="1dcdb-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1dcdb-130">Validation File</span></span>  <br/> |<span data-ttu-id="1dcdb-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1dcdb-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1dcdb-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1dcdb-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="1dcdb-133">False</span><span class="sxs-lookup"><span data-stu-id="1dcdb-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1dcdb-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1dcdb-134">See also</span></span>



[<span data-ttu-id="1dcdb-135">GetUMProperties-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="1dcdb-135">GetUMProperties operation (UM web service)</span></span>](getumproperties-operation-um-web-service.md)

