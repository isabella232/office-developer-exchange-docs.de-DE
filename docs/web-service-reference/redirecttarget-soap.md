---
title: RedirectTarget (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: f8162724-cf9a-4543-a1ad-5846c8b10bfa
description: Das RedirectTarget (SOAP)-Element enthält, die als Ziel für die Umleitung URL oder die E-mail-Adresse.
ms.openlocfilehash: 3a8a0c39c6889730c9d17778c6a26f84fcbcd4a7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831019"
---
# <a name="redirecttarget-soap"></a><span data-ttu-id="5097f-103">RedirectTarget (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5097f-103">RedirectTarget (SOAP)</span></span>

<span data-ttu-id="5097f-104">Das [RedirectTarget (SOAP)](redirecttarget-soap.md) -Element enthält, die als Ziel für die Umleitung URL oder die E-mail-Adresse.</span><span class="sxs-lookup"><span data-stu-id="5097f-104">The [RedirectTarget (SOAP)](redirecttarget-soap.md) element contains the target of the redirection URL or e-mail address.</span></span> 
  
```XML
<RedirectTarget/>
```

 <span data-ttu-id="5097f-105">**string**</span><span class="sxs-lookup"><span data-stu-id="5097f-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5097f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5097f-106">Attributes and elements</span></span>

<span data-ttu-id="5097f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5097f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5097f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5097f-108">Attributes</span></span>

<span data-ttu-id="5097f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5097f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5097f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5097f-110">Child elements</span></span>

<span data-ttu-id="5097f-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="5097f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5097f-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5097f-112">Parent elements</span></span>

|<span data-ttu-id="5097f-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5097f-113">**Element**</span></span>|<span data-ttu-id="5097f-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5097f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5097f-115">UserResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5097f-115">UserResponse (SOAP)</span></span>](userresponse-soap.md) <br/> |<span data-ttu-id="5097f-116">Stellt eine Antwort auf eine Anforderung GetUserSettings für einen einzelnen Benutzer dar.</span><span class="sxs-lookup"><span data-stu-id="5097f-116">Represents a response to a GetUserSettings request for an individual user.</span></span>  <br/> |
|[<span data-ttu-id="5097f-117">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5097f-117">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="5097f-118">Enthält die angeforderten Einstellungen für die angegebene Domäne.</span><span class="sxs-lookup"><span data-stu-id="5097f-118">Contains the requested settings for the specified domain.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5097f-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="5097f-119">Text value</span></span>

<span data-ttu-id="5097f-120">Der Textwert enthält, die als Ziel für die Umleitung URL oder die E-mail-Adresse, die für eine nachfolgende GetUserSettings verwendet werden soll, oder fordern Sie GetDomainSettings.</span><span class="sxs-lookup"><span data-stu-id="5097f-120">The text value contains the target of the redirection URL or e-mail address that should be used for a subsequent GetUserSettings or GetDomainSettings request.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5097f-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="5097f-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5097f-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="5097f-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="5097f-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5097f-123">Schema Name</span></span>  <br/> |<span data-ttu-id="5097f-124">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="5097f-124">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="5097f-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5097f-125">Validation File</span></span>  <br/> |<span data-ttu-id="5097f-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5097f-126">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5097f-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5097f-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="5097f-128">True</span><span class="sxs-lookup"><span data-stu-id="5097f-128">True</span></span>  <br/> |
   

