---
title: ApplicationRoles
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 00003b9b-f8f1-4452-a0af-157f789f8892
description: Das ApplicationRoles-Element gibt die Anwendungsrollen an, die die aufrufende Partneranwendung für den aktuellen Anruf verwendet.
ms.openlocfilehash: 8dfe5c745896d02217cbf91375d355954a4e22eb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464700"
---
# <a name="applicationroles"></a><span data-ttu-id="7f588-103">ApplicationRoles</span><span class="sxs-lookup"><span data-stu-id="7f588-103">ApplicationRoles</span></span>

<span data-ttu-id="7f588-104">Das **ApplicationRoles** -Element gibt die Anwendungsrollen an, die die aufrufende Partneranwendung für den aktuellen Anruf verwendet.</span><span class="sxs-lookup"><span data-stu-id="7f588-104">The **ApplicationRoles** element specifies the application roles that the calling partner application uses for the current call.</span></span> 
  
```XML
<ApplicationRoles>
    <Role></Role>
</ApplicationRoles>
```

 <span data-ttu-id="7f588-105">**NonEmptyArrayOfRoleType**</span><span class="sxs-lookup"><span data-stu-id="7f588-105">**NonEmptyArrayOfRoleType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7f588-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7f588-106">Attributes and elements</span></span>

<span data-ttu-id="7f588-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7f588-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7f588-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7f588-108">Attributes</span></span>

<span data-ttu-id="7f588-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7f588-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7f588-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7f588-110">Child elements</span></span>

|<span data-ttu-id="7f588-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="7f588-111">**Element**</span></span>|<span data-ttu-id="7f588-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7f588-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7f588-113">Rolle</span><span class="sxs-lookup"><span data-stu-id="7f588-113">Role</span></span>](role.md) <br/> |<span data-ttu-id="7f588-114">Gibt eine Zeichenfolge an, die eine Verwaltungsrolle darstellt.</span><span class="sxs-lookup"><span data-stu-id="7f588-114">Specifies a string that represents a management role.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7f588-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7f588-115">Parent elements</span></span>

|<span data-ttu-id="7f588-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="7f588-116">**Element**</span></span>|<span data-ttu-id="7f588-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7f588-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7f588-118">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="7f588-118">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="7f588-119">Gibt die Verwaltungsrolle an.</span><span class="sxs-lookup"><span data-stu-id="7f588-119">Specifies the management role.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f588-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f588-120">Remarks</span></span>

<span data-ttu-id="7f588-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7f588-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7f588-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7f588-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7f588-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="7f588-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7f588-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="7f588-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7f588-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7f588-125">Schema Name</span></span>  <br/> |<span data-ttu-id="7f588-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="7f588-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="7f588-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7f588-127">Validation File</span></span>  <br/> |<span data-ttu-id="7f588-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="7f588-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="7f588-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="7f588-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="7f588-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f588-130">See also</span></span>

- [<span data-ttu-id="7f588-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7f588-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

