---
title: Anforderung (GetFederationInformation) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: beeb5371-f57b-4346-9753-035dd42c6bee
description: Das angeforderte Element stellt eine Anforderung GetFederationInformationRequest (SOAP).
ms.openlocfilehash: 0fb9301c2f318aa2c27155675dd3c43b41aabecd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831119"
---
# <a name="request-getfederationinformation-soap"></a><span data-ttu-id="63136-103">Anforderung (GetFederationInformation) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="63136-103">Request (GetFederationInformation) (SOAP)</span></span>

<span data-ttu-id="63136-104">Das **angeforderte** Element stellt eine Anforderung [GetFederationInformationRequest (SOAP)](getfederationinformationrequest-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="63136-104">The **Request** element represents a [GetFederationInformationRequest (SOAP)](getfederationinformationrequest-soap.md) request.</span></span> 
  
```XML
<Request>
   <Domain/>
</Request>
```

 <span data-ttu-id="63136-105">**GetFederationInformationRequest**</span><span class="sxs-lookup"><span data-stu-id="63136-105">**GetFederationInformationRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="63136-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="63136-106">Attributes and elements</span></span>

<span data-ttu-id="63136-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="63136-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="63136-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="63136-108">Attributes</span></span>

<span data-ttu-id="63136-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="63136-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="63136-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="63136-110">Child elements</span></span>

|<span data-ttu-id="63136-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="63136-111">**Element**</span></span>|<span data-ttu-id="63136-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="63136-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="63136-113">Domäne (GetFederationInformation) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="63136-113">Domain (GetFederationInformation) (SOAP)</span></span>](domain-getfederationinformationsoap.md) <br/> |<span data-ttu-id="63136-114">Identifiziert die Domäne, die eine verbundvertrauensstellung hat.</span><span class="sxs-lookup"><span data-stu-id="63136-114">Identifies the domain that has a federation trust.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="63136-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="63136-115">Parent elements</span></span>

|<span data-ttu-id="63136-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="63136-116">**Element**</span></span>|<span data-ttu-id="63136-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="63136-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="63136-118">GetFederationInformationRequestMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="63136-118">GetFederationInformationRequestMessage (SOAP)</span></span>](getfederationinformationrequestmessage-soap.md) <br/> |<span data-ttu-id="63136-119">Bereitet einen Aufruf an den Server auf Anforderung Konfigurationsdaten für den Sicherheitstokendienst (STS).</span><span class="sxs-lookup"><span data-stu-id="63136-119">Prepares a call to the server to request configuration data for the security token service (STS).</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="63136-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="63136-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="63136-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="63136-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="63136-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="63136-122">Schema Name</span></span>  <br/> |<span data-ttu-id="63136-123">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="63136-123">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="63136-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="63136-124">Validation File</span></span>  <br/> |<span data-ttu-id="63136-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="63136-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="63136-126">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="63136-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="63136-127">True</span><span class="sxs-lookup"><span data-stu-id="63136-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="63136-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63136-128">See also</span></span>



[<span data-ttu-id="63136-129">Arbeiten mit der AutoErmittlung</span><span class="sxs-lookup"><span data-stu-id="63136-129">Working with Autodiscover</span></span>](http://msdn.microsoft.com/library/39726b67-2eb2-451b-9307-cfd0b518b55c%28Office.15%29.aspx)

