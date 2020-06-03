---
title: UserResponses (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a48766df-4cc8-47c2-a8c1-826daec94e5a
description: Das UserResponses-Element enthält die Konfigurationseinstellungen für jeden angeforderten Benutzer.
ms.openlocfilehash: db2bab16334b90395d29dc03353dce05b0e45357
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526746"
---
# <a name="userresponses-soap"></a><span data-ttu-id="f57da-103">UserResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f57da-103">UserResponses (SOAP)</span></span>

<span data-ttu-id="f57da-104">Das **UserResponses** -Element enthält die Konfigurationseinstellungen für jeden angeforderten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="f57da-104">The **UserResponses** element contains the configuration settings for each requested user.</span></span> 
  
```XML
<UserResponses>
   <UserResponse/>
</UserResponses>
```

 <span data-ttu-id="f57da-105">**ArrayOfUserResponse**</span><span class="sxs-lookup"><span data-stu-id="f57da-105">**ArrayOfUserResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f57da-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f57da-106">Attributes and elements</span></span>

<span data-ttu-id="f57da-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f57da-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f57da-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f57da-108">Attributes</span></span>

<span data-ttu-id="f57da-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f57da-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f57da-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f57da-110">Child elements</span></span>

|<span data-ttu-id="f57da-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f57da-111">**Element**</span></span>|<span data-ttu-id="f57da-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f57da-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f57da-113">User Response (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f57da-113">UserResponse (SOAP)</span></span>](userresponse-soap.md) <br/> |<span data-ttu-id="f57da-114">Stellt eine Antwort auf eine [GetUserSettings-Vorgang (SOAP)-](getusersettings-operation-soap.md) Anforderung für einen einzelnen Benutzer dar.</span><span class="sxs-lookup"><span data-stu-id="f57da-114">Represents a response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request for an individual user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f57da-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f57da-115">Parent elements</span></span>

|<span data-ttu-id="f57da-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="f57da-116">**Element**</span></span>|<span data-ttu-id="f57da-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f57da-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f57da-118">Antwort (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f57da-118">Response (SOAP)</span></span>](response-soap.md) <br/> |<span data-ttu-id="f57da-119">Enthält die Antwort auf eine [GetUserSettings-Vorgang (SOAP)-](getusersettings-operation-soap.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f57da-119">Contains the response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="f57da-120">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f57da-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f57da-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="f57da-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="f57da-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f57da-122">Schema Name</span></span>  <br/> |<span data-ttu-id="f57da-123">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="f57da-123">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="f57da-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f57da-124">Validation File</span></span>  <br/> |<span data-ttu-id="f57da-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="f57da-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f57da-126">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f57da-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="f57da-127">True</span><span class="sxs-lookup"><span data-stu-id="f57da-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f57da-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f57da-128">See also</span></span>



[<span data-ttu-id="f57da-129">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f57da-129">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

