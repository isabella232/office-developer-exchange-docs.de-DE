---
title: Request (GetFederationInformation) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: beeb5371-f57b-4346-9753-035dd42c6bee
description: Das Request-Element stellt eine GetFederationInformationRequest (SOAP)-Anforderung dar.
ms.openlocfilehash: dbd88537d03f6325cf0025d08c63ae486544d705
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459581"
---
# <a name="request-getfederationinformation-soap"></a><span data-ttu-id="aee09-103">Request (GetFederationInformation) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="aee09-103">Request (GetFederationInformation) (SOAP)</span></span>

<span data-ttu-id="aee09-104">Das **Request** -Element stellt eine [GetFederationInformationRequest (SOAP)-](getfederationinformationrequest-soap.md) Anforderung dar.</span><span class="sxs-lookup"><span data-stu-id="aee09-104">The **Request** element represents a [GetFederationInformationRequest (SOAP)](getfederationinformationrequest-soap.md) request.</span></span> 
  
```XML
<Request>
   <Domain/>
</Request>
```

 <span data-ttu-id="aee09-105">**GetFederationInformationRequest**</span><span class="sxs-lookup"><span data-stu-id="aee09-105">**GetFederationInformationRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aee09-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="aee09-106">Attributes and elements</span></span>

<span data-ttu-id="aee09-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="aee09-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aee09-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="aee09-108">Attributes</span></span>

<span data-ttu-id="aee09-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="aee09-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aee09-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aee09-110">Child elements</span></span>

|<span data-ttu-id="aee09-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="aee09-111">**Element**</span></span>|<span data-ttu-id="aee09-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aee09-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aee09-113">Domäne (GetFederationInformation) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="aee09-113">Domain (GetFederationInformation) (SOAP)</span></span>](domain-getfederationinformationsoap.md) <br/> |<span data-ttu-id="aee09-114">Identifiziert die Domäne, die über eine Verbundvertrauensstellung verfügt.</span><span class="sxs-lookup"><span data-stu-id="aee09-114">Identifies the domain that has a federation trust.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="aee09-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aee09-115">Parent elements</span></span>

|<span data-ttu-id="aee09-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="aee09-116">**Element**</span></span>|<span data-ttu-id="aee09-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aee09-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aee09-118">GetFederationInformationRequestMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="aee09-118">GetFederationInformationRequestMessage (SOAP)</span></span>](getfederationinformationrequestmessage-soap.md) <br/> |<span data-ttu-id="aee09-119">Bereitet einen Aufruf an den Server vor, um Konfigurationsdaten für den Sicherheitstokendienst (Security Token Service, STS) anzufordern.</span><span class="sxs-lookup"><span data-stu-id="aee09-119">Prepares a call to the server to request configuration data for the security token service (STS).</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="aee09-120">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="aee09-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aee09-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="aee09-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="aee09-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="aee09-122">Schema Name</span></span>  <br/> |<span data-ttu-id="aee09-123">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="aee09-123">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="aee09-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="aee09-124">Validation File</span></span>  <br/> |<span data-ttu-id="aee09-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="aee09-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="aee09-126">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="aee09-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="aee09-127">True</span><span class="sxs-lookup"><span data-stu-id="aee09-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aee09-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aee09-128">See also</span></span>



[<span data-ttu-id="aee09-129">Arbeiten mit der AutoErmittlung</span><span class="sxs-lookup"><span data-stu-id="aee09-129">Working with Autodiscover</span></span>](https://msdn.microsoft.com/library/39726b67-2eb2-451b-9307-cfd0b518b55c%28Office.15%29.aspx)

