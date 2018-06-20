---
title: UserSettingError (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: abb175c5-4f38-4dcc-81e3-b511686862eb
description: Das Element UserSettingError stellt einen Fehler, der als Ergebnis beim Abrufen einer benutzereinstellung zurückgegeben wird.
ms.openlocfilehash: 886e0be0aa900ce3a00902c21cc115e866d0cd99
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839466"
---
# <a name="usersettingerror-soap"></a><span data-ttu-id="83094-103">UserSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="83094-103">UserSettingError (SOAP)</span></span>

<span data-ttu-id="83094-104">Das Element **UserSettingError** stellt einen Fehler, der als Ergebnis beim Abrufen einer benutzereinstellung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="83094-104">The **UserSettingError** element represents an error that is returned as a result of an attempt to get a user setting.</span></span> 
  
```XML
<UserSettingError>
    <ErrorCode/>
    <ErrorMessage/>
    <SettingName/>
</UserSettingError>
```

 <span data-ttu-id="83094-105">**UserSettingError**</span><span class="sxs-lookup"><span data-stu-id="83094-105">**UserSettingError**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="83094-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="83094-106">Attributes and elements</span></span>

<span data-ttu-id="83094-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="83094-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="83094-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="83094-108">Attributes</span></span>

<span data-ttu-id="83094-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="83094-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="83094-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="83094-110">Child elements</span></span>

|<span data-ttu-id="83094-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="83094-111">**Element**</span></span>|<span data-ttu-id="83094-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="83094-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83094-113">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="83094-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="83094-114">Stellt einen Fehlercode, der von den AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="83094-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="83094-115">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="83094-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="83094-116">Typ ein Fehlercode, der von den AutoErmittlungsdienst zurückgegeben wird eine Meldung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="83094-116">Respresents a message associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="83094-117">SettingName (SOAP)</span><span class="sxs-lookup"><span data-stu-id="83094-117">SettingName (SOAP)</span></span>](settingname-soap.md) <br/> |<span data-ttu-id="83094-118">Stellt den Namen einer Einstellung Benutzer dar.</span><span class="sxs-lookup"><span data-stu-id="83094-118">Represents the name of a user setting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="83094-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="83094-119">Parent elements</span></span>

|<span data-ttu-id="83094-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="83094-120">**Element**</span></span>|<span data-ttu-id="83094-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="83094-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83094-122">UserSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="83094-122">UserSettingErrors (SOAP)</span></span>](usersettingerrors-soap.md) <br/> |<span data-ttu-id="83094-123">Stellt eine Auflistung von Informationen zu Einstellungen, die nicht zurückgegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="83094-123">Represents a collection of information about settings that could not be returned.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="83094-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="83094-124">Text value</span></span>

<span data-ttu-id="83094-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="83094-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="83094-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="83094-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="83094-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="83094-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="83094-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="83094-128">Schema Name</span></span>  <br/> |<span data-ttu-id="83094-129">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="83094-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="83094-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="83094-130">Validation File</span></span>  <br/> |<span data-ttu-id="83094-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="83094-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="83094-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="83094-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="83094-133">True</span><span class="sxs-lookup"><span data-stu-id="83094-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="83094-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83094-134">See also</span></span>



[<span data-ttu-id="83094-135">SOAP-Autodiscover XML-Elemente für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="83094-135">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

