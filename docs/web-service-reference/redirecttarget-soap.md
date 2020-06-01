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
description: Das RedirectTarget (SOAP)-Element enthält das Ziel der Umleitungs-URL oder der e-Mail-Adresse.
ms.openlocfilehash: 092d575560379d43b12dd98a3efa155b59c31450
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462199"
---
# <a name="redirecttarget-soap"></a><span data-ttu-id="cab46-103">RedirectTarget (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cab46-103">RedirectTarget (SOAP)</span></span>

<span data-ttu-id="cab46-104">Das [RedirectTarget (SOAP)](redirecttarget-soap.md) -Element enthält das Ziel der Umleitungs-URL oder der e-Mail-Adresse.</span><span class="sxs-lookup"><span data-stu-id="cab46-104">The [RedirectTarget (SOAP)](redirecttarget-soap.md) element contains the target of the redirection URL or e-mail address.</span></span> 
  
```XML
<RedirectTarget/>
```

 <span data-ttu-id="cab46-105">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cab46-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cab46-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cab46-106">Attributes and elements</span></span>

<span data-ttu-id="cab46-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cab46-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cab46-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="cab46-108">Attributes</span></span>

<span data-ttu-id="cab46-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="cab46-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cab46-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cab46-110">Child elements</span></span>

<span data-ttu-id="cab46-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="cab46-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cab46-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cab46-112">Parent elements</span></span>

|<span data-ttu-id="cab46-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="cab46-113">**Element**</span></span>|<span data-ttu-id="cab46-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cab46-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cab46-115">User Response (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cab46-115">UserResponse (SOAP)</span></span>](userresponse-soap.md) <br/> |<span data-ttu-id="cab46-116">Stellt eine Antwort auf eine GetUserSettings-Anforderung für einen einzelnen Benutzer dar.</span><span class="sxs-lookup"><span data-stu-id="cab46-116">Represents a response to a GetUserSettings request for an individual user.</span></span>  <br/> |
|[<span data-ttu-id="cab46-117">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cab46-117">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="cab46-118">Enthält die angeforderten Einstellungen für die angegebene Domäne.</span><span class="sxs-lookup"><span data-stu-id="cab46-118">Contains the requested settings for the specified domain.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cab46-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="cab46-119">Text value</span></span>

<span data-ttu-id="cab46-120">Der Textwert enthält das Ziel der Umleitungs-URL oder e-Mail-Adresse, die für eine nachfolgende GetUserSettings-oder GetDomainSettings-Anforderung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cab46-120">The text value contains the target of the redirection URL or e-mail address that should be used for a subsequent GetUserSettings or GetDomainSettings request.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cab46-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="cab46-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cab46-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="cab46-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="cab46-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cab46-123">Schema Name</span></span>  <br/> |<span data-ttu-id="cab46-124">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="cab46-124">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="cab46-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cab46-125">Validation File</span></span>  <br/> |<span data-ttu-id="cab46-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="cab46-126">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cab46-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="cab46-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="cab46-128">True</span><span class="sxs-lookup"><span data-stu-id="cab46-128">True</span></span>  <br/> |
   

