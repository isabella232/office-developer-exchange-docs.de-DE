---
title: DomainSetting (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: bad5399c-0762-4979-9c15-58cf4b7b6278
description: Das DomainSetting-Element enthält Domäneneinstellungen, die von der Vorgangsanforderung des GetDomainSettings-Vorgangs (SOAP) zurückgegeben werden.
ms.openlocfilehash: 54441dd7cfcf7372807a1e6bfd8ea5d26805bffc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526298"
---
# <a name="domainsetting-soap"></a><span data-ttu-id="73be7-103">DomainSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="73be7-103">DomainSetting (SOAP)</span></span>

<span data-ttu-id="73be7-104">Das **DomainSetting** -Element enthält Domäneneinstellungen, die von der Vorgangsanforderung des [GetDomainSettings-Vorgangs (SOAP)](getdomainsettings-operation-soap.md) zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="73be7-104">The **DomainSetting** element contains domain settings that are returned by the [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) operation request.</span></span> 
  
```XML
<DomainSetting>
   <Name/>
</DomainSetting>
```

 <span data-ttu-id="73be7-105">**DomainSetting**</span><span class="sxs-lookup"><span data-stu-id="73be7-105">**DomainSetting**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="73be7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="73be7-106">Attributes and elements</span></span>

<span data-ttu-id="73be7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="73be7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="73be7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="73be7-108">Attributes</span></span>

<span data-ttu-id="73be7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="73be7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="73be7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="73be7-110">Child elements</span></span>

|<span data-ttu-id="73be7-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="73be7-111">**Element**</span></span>|<span data-ttu-id="73be7-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="73be7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="73be7-113">Name (SOAP)</span><span class="sxs-lookup"><span data-stu-id="73be7-113">Name (SOAP)</span></span>](name-soap.md) <br/> |<span data-ttu-id="73be7-114">Stellt den Namen einer Einstellung dar.</span><span class="sxs-lookup"><span data-stu-id="73be7-114">Represents the name of a setting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="73be7-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="73be7-115">Parent elements</span></span>

|<span data-ttu-id="73be7-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="73be7-116">**Element**</span></span>|<span data-ttu-id="73be7-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="73be7-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="73be7-118">DomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="73be7-118">DomainSettings (SOAP)</span></span>](domainsettings-soap.md) <br/> |<span data-ttu-id="73be7-119">Stellt die Domäneneinstellungen dar, die in einer Auto Ermittlungsanforderung übermittelt oder von einer Auto Ermittlungs Antwort zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="73be7-119">Represents the domain settings that were submitted in an Autodiscover request or returned by an Autodiscover response.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="73be7-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="73be7-120">Text value</span></span>

<span data-ttu-id="73be7-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="73be7-121">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="73be7-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="73be7-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="73be7-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="73be7-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="73be7-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="73be7-124">Schema Name</span></span>  <br/> |<span data-ttu-id="73be7-125">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="73be7-125">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="73be7-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="73be7-126">Validation File</span></span>  <br/> |<span data-ttu-id="73be7-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="73be7-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="73be7-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="73be7-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="73be7-129">True</span><span class="sxs-lookup"><span data-stu-id="73be7-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="73be7-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73be7-130">See also</span></span>

- [<span data-ttu-id="73be7-131">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="73be7-131">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

