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
description: Das UserSettingError-Element stellt einen Fehler dar, der als Ergebnis eines Versuchs zum Abrufen einer Benutzereinstellung zurückgegeben wird.
ms.openlocfilehash: 61603038ce93780f690d72226b1356b239d2002d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468607"
---
# <a name="usersettingerror-soap"></a><span data-ttu-id="a4003-103">UserSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a4003-103">UserSettingError (SOAP)</span></span>

<span data-ttu-id="a4003-104">Das **UserSettingError** -Element stellt einen Fehler dar, der als Ergebnis eines Versuchs zum Abrufen einer Benutzereinstellung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a4003-104">The **UserSettingError** element represents an error that is returned as a result of an attempt to get a user setting.</span></span> 
  
```XML
<UserSettingError>
    <ErrorCode/>
    <ErrorMessage/>
    <SettingName/>
</UserSettingError>
```

 <span data-ttu-id="a4003-105">**UserSettingError**</span><span class="sxs-lookup"><span data-stu-id="a4003-105">**UserSettingError**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a4003-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a4003-106">Attributes and elements</span></span>

<span data-ttu-id="a4003-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a4003-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a4003-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a4003-108">Attributes</span></span>

<span data-ttu-id="a4003-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a4003-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a4003-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a4003-110">Child elements</span></span>

|<span data-ttu-id="a4003-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a4003-111">**Element**</span></span>|<span data-ttu-id="a4003-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a4003-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a4003-113">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a4003-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="a4003-114">Stellt einen Fehlercode dar, der vom AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a4003-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="a4003-115">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a4003-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="a4003-116">Respresents eine Nachricht, die einem Fehlercode zugeordnet ist, der vom AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a4003-116">Respresents a message associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="a4003-117">SettingName (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a4003-117">SettingName (SOAP)</span></span>](settingname-soap.md) <br/> |<span data-ttu-id="a4003-118">Stellt den Namen einer Benutzereinstellung dar.</span><span class="sxs-lookup"><span data-stu-id="a4003-118">Represents the name of a user setting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a4003-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a4003-119">Parent elements</span></span>

|<span data-ttu-id="a4003-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="a4003-120">**Element**</span></span>|<span data-ttu-id="a4003-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a4003-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a4003-122">UserSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a4003-122">UserSettingErrors (SOAP)</span></span>](usersettingerrors-soap.md) <br/> |<span data-ttu-id="a4003-123">Stellt eine Sammlung von Informationen zu Einstellungen dar, die nicht zurückgegeben werden konnten.</span><span class="sxs-lookup"><span data-stu-id="a4003-123">Represents a collection of information about settings that could not be returned.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a4003-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="a4003-124">Text value</span></span>

<span data-ttu-id="a4003-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="a4003-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a4003-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a4003-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a4003-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="a4003-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="a4003-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a4003-128">Schema Name</span></span>  <br/> |<span data-ttu-id="a4003-129">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="a4003-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="a4003-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a4003-130">Validation File</span></span>  <br/> |<span data-ttu-id="a4003-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="a4003-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a4003-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a4003-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="a4003-133">True</span><span class="sxs-lookup"><span data-stu-id="a4003-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a4003-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4003-134">See also</span></span>



[<span data-ttu-id="a4003-135">XML-Elemente der SOAP-AutoErmittlung für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="a4003-135">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

