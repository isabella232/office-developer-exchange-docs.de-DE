---
title: Domäne (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 849629a0-0467-422f-88f6-3b8a95c17bba
description: Das Domäne-Element enthält eine verbunddomäne in einer Antwort GetFederationInformation oder eine Domäne, die Konfigurationseinstellungen für die in einer Anforderung GetDomainSettings angefordert werden.
ms.openlocfilehash: 411ca866800322ef06eeecc2ab92adc6f711917c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758087"
---
# <a name="domain-soap"></a><span data-ttu-id="b5dff-103">Domäne (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b5dff-103">Domain (SOAP)</span></span>

<span data-ttu-id="b5dff-104">Das **Domäne** -Element enthält eine verbunddomäne in einer Antwort **GetFederationInformation** oder eine Domäne, die Konfigurationseinstellungen für die in einer Anforderung **GetDomainSettings** angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="b5dff-104">The **Domain** element contains a federated domain in a **GetFederationInformation** response or contains a domain the configuration settings for which are requested in a **GetDomainSettings** request.</span></span> 
  
```XML
<Domain/> 
```

 <span data-ttu-id="b5dff-105">**string**</span><span class="sxs-lookup"><span data-stu-id="b5dff-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b5dff-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b5dff-106">Attributes and elements</span></span>

<span data-ttu-id="b5dff-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b5dff-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b5dff-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b5dff-108">Attributes</span></span>

<span data-ttu-id="b5dff-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b5dff-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b5dff-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b5dff-110">Child elements</span></span>

<span data-ttu-id="b5dff-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b5dff-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b5dff-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b5dff-112">Parent elements</span></span>

|<span data-ttu-id="b5dff-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b5dff-113">**Element**</span></span>|<span data-ttu-id="b5dff-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b5dff-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b5dff-115">Domänen (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b5dff-115">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="b5dff-116">Stellt die Domänen, die Konfigurationseinstellungen für die in einem Vorgang **GetDomainSettings** zurückgegeben werden, oder die Domänen, die die Organisation in einem Vorgang **GetFederationInformation** federated hat.</span><span class="sxs-lookup"><span data-stu-id="b5dff-116">Represents the domains the configuration settings for which are returned in a **GetDomainSettings** operation or the domains that the organization has federated in a **GetFederationInformation** operation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b5dff-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="b5dff-117">Text value</span></span>

<span data-ttu-id="b5dff-118">Der Textwert der **Domäne** -Element stellt einen Domänennamen ein.</span><span class="sxs-lookup"><span data-stu-id="b5dff-118">The text value of the **Domain** element represents a domain name.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="b5dff-119">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b5dff-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5dff-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="b5dff-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="b5dff-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b5dff-121">Schema Name</span></span>  <br/> |<span data-ttu-id="b5dff-122">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="b5dff-122">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="b5dff-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b5dff-123">Validation File</span></span>  <br/> |<span data-ttu-id="b5dff-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b5dff-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b5dff-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b5dff-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="b5dff-126">True</span><span class="sxs-lookup"><span data-stu-id="b5dff-126">True</span></span>  <br/> |
   

