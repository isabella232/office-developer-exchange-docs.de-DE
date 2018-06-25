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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831019"
---
# <a name="redirecttarget-soap"></a><span data-ttu-id="0c2f9-103">RedirectTarget (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0c2f9-103">RedirectTarget (SOAP)</span></span>

<span data-ttu-id="0c2f9-104">Das [RedirectTarget (SOAP)](redirecttarget-soap.md) -Element enthält, die als Ziel für die Umleitung URL oder die E-mail-Adresse.</span><span class="sxs-lookup"><span data-stu-id="0c2f9-104">The [RedirectTarget (SOAP)](redirecttarget-soap.md) element contains the target of the redirection URL or e-mail address.</span></span> 
  
```XML
<RedirectTarget/>
```

 <span data-ttu-id="0c2f9-105">**string**</span><span class="sxs-lookup"><span data-stu-id="0c2f9-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0c2f9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0c2f9-106">Attributes and elements</span></span>

<span data-ttu-id="0c2f9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0c2f9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0c2f9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="0c2f9-108">Attributes</span></span>

<span data-ttu-id="0c2f9-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="0c2f9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0c2f9-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0c2f9-110">Child elements</span></span>

<span data-ttu-id="0c2f9-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="0c2f9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0c2f9-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0c2f9-112">Parent elements</span></span>

|<span data-ttu-id="0c2f9-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0c2f9-113">**Element**</span></span>|<span data-ttu-id="0c2f9-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0c2f9-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0c2f9-115">UserResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0c2f9-115">UserResponse (SOAP)</span></span>](userresponse-soap.md) <br/> |<span data-ttu-id="0c2f9-116">Stellt eine Antwort auf eine Anforderung GetUserSettings für einen einzelnen Benutzer dar.</span><span class="sxs-lookup"><span data-stu-id="0c2f9-116">Represents a response to a GetUserSettings request for an individual user.</span></span>  <br/> |
|[<span data-ttu-id="0c2f9-117">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0c2f9-117">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="0c2f9-118">Enthält die angeforderten Einstellungen für die angegebene Domäne.</span><span class="sxs-lookup"><span data-stu-id="0c2f9-118">Contains the requested settings for the specified domain.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0c2f9-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="0c2f9-119">Text value</span></span>

<span data-ttu-id="0c2f9-120">Der Textwert enthält, die als Ziel für die Umleitung URL oder die E-mail-Adresse, die für eine nachfolgende GetUserSettings verwendet werden soll, oder fordern Sie GetDomainSettings.</span><span class="sxs-lookup"><span data-stu-id="0c2f9-120">The text value contains the target of the redirection URL or e-mail address that should be used for a subsequent GetUserSettings or GetDomainSettings request.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0c2f9-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0c2f9-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0c2f9-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="0c2f9-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="0c2f9-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0c2f9-123">Schema Name</span></span>  <br/> |<span data-ttu-id="0c2f9-124">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="0c2f9-124">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="0c2f9-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0c2f9-125">Validation File</span></span>  <br/> |<span data-ttu-id="0c2f9-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0c2f9-126">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0c2f9-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0c2f9-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="0c2f9-128">True</span><span class="sxs-lookup"><span data-stu-id="0c2f9-128">True</span></span>  <br/> |
   

