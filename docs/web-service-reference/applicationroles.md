---
title: ApplicationRoles
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 00003b9b-f8f1-4452-a0af-157f789f8892
description: Das ApplicationRoles-Element gibt die Rollen der Anwendung, die die aufrufende partneranwendung für den aktuellen Anruf verwendet.
ms.openlocfilehash: ff32b693dae573416263bcb7c0fbb552a933b8d6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757276"
---
# <a name="applicationroles"></a><span data-ttu-id="30266-103">ApplicationRoles</span><span class="sxs-lookup"><span data-stu-id="30266-103">ApplicationRoles</span></span>

<span data-ttu-id="30266-104">Das **ApplicationRoles** -Element gibt die Rollen der Anwendung, die die aufrufende partneranwendung für den aktuellen Anruf verwendet.</span><span class="sxs-lookup"><span data-stu-id="30266-104">The **ApplicationRoles** element specifies the application roles that the calling partner application uses for the current call.</span></span> 
  
```XML
<ApplicationRoles>
    <Role></Role>
</ApplicationRoles>
```

 <span data-ttu-id="30266-105">**NonEmptyArrayOfRoleType**</span><span class="sxs-lookup"><span data-stu-id="30266-105">**NonEmptyArrayOfRoleType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="30266-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="30266-106">Attributes and elements</span></span>

<span data-ttu-id="30266-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="30266-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="30266-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="30266-108">Attributes</span></span>

<span data-ttu-id="30266-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="30266-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="30266-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="30266-110">Child elements</span></span>

|<span data-ttu-id="30266-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="30266-111">**Element**</span></span>|<span data-ttu-id="30266-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="30266-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="30266-113">Role</span><span class="sxs-lookup"><span data-stu-id="30266-113">Role</span></span>](role.md) <br/> |<span data-ttu-id="30266-114">Gibt eine Zeichenfolge, die eine Verwaltungsrolle darstellt.</span><span class="sxs-lookup"><span data-stu-id="30266-114">Specifies a string that represents a management role.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="30266-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="30266-115">Parent elements</span></span>

|<span data-ttu-id="30266-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="30266-116">**Element**</span></span>|<span data-ttu-id="30266-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="30266-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="30266-118">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="30266-118">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="30266-119">Gibt die Verwaltungsrolle an.</span><span class="sxs-lookup"><span data-stu-id="30266-119">Specifies the management role.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30266-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="30266-120">Remarks</span></span>

<span data-ttu-id="30266-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="30266-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="30266-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="30266-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="30266-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="30266-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="30266-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="30266-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="30266-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="30266-125">Schema Name</span></span>  <br/> |<span data-ttu-id="30266-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="30266-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="30266-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="30266-127">Validation File</span></span>  <br/> |<span data-ttu-id="30266-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="30266-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="30266-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="30266-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="30266-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30266-130">See also</span></span>

- [<span data-ttu-id="30266-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="30266-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

