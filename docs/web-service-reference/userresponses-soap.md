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
ms.openlocfilehash: bee7f3c9a95c1facfe0adc990516dfa323d9c8cf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839459"
---
# <a name="userresponses-soap"></a><span data-ttu-id="a3bca-103">UserResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a3bca-103">UserResponses (SOAP)</span></span>

<span data-ttu-id="a3bca-104">Das **UserResponses** -Element enthält die Konfigurationseinstellungen für jeden angeforderten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="a3bca-104">The **UserResponses** element contains the configuration settings for each requested user.</span></span> 
  
```XML
<UserResponses>
   <UserResponse/>
</UserResponses>
```

 <span data-ttu-id="a3bca-105">**ArrayOfUserResponse**</span><span class="sxs-lookup"><span data-stu-id="a3bca-105">**ArrayOfUserResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a3bca-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a3bca-106">Attributes and elements</span></span>

<span data-ttu-id="a3bca-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a3bca-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a3bca-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a3bca-108">Attributes</span></span>

<span data-ttu-id="a3bca-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a3bca-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a3bca-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a3bca-110">Child elements</span></span>

|<span data-ttu-id="a3bca-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a3bca-111">**Element**</span></span>|<span data-ttu-id="a3bca-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a3bca-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a3bca-113">UserResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a3bca-113">UserResponse (SOAP)</span></span>](userresponse-soap.md) <br/> |<span data-ttu-id="a3bca-114">Stellt eine Antwort auf eine Anforderung [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md) für einen einzelnen Benutzer dar.</span><span class="sxs-lookup"><span data-stu-id="a3bca-114">Represents a response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request for an individual user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a3bca-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a3bca-115">Parent elements</span></span>

|<span data-ttu-id="a3bca-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="a3bca-116">**Element**</span></span>|<span data-ttu-id="a3bca-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a3bca-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a3bca-118">Antwort (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a3bca-118">Response (SOAP)</span></span>](response-soap.md) <br/> |<span data-ttu-id="a3bca-119">Enthält die Antwort auf eine Anforderung [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="a3bca-119">Contains the response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="a3bca-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a3bca-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a3bca-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="a3bca-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="a3bca-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a3bca-122">Schema Name</span></span>  <br/> |<span data-ttu-id="a3bca-123">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="a3bca-123">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="a3bca-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a3bca-124">Validation File</span></span>  <br/> |<span data-ttu-id="a3bca-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a3bca-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a3bca-126">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a3bca-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="a3bca-127">True</span><span class="sxs-lookup"><span data-stu-id="a3bca-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a3bca-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3bca-128">See also</span></span>



[<span data-ttu-id="a3bca-129">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a3bca-129">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

