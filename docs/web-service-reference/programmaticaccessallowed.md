---
title: ProgrammaticAccessAllowed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a1fc7dff-a303-4809-b7f4-9672f86c183c
description: Das ProgrammaticAccessAllowed-Element gibt an, ob der programmgesteuerte Zugriff für rechteverwaltete Daten aktiviert ist.
ms.openlocfilehash: 8a5cf4e57a97807e5940a0402768d7123b9912d2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465639"
---
# <a name="programmaticaccessallowed"></a><span data-ttu-id="2891b-103">ProgrammaticAccessAllowed</span><span class="sxs-lookup"><span data-stu-id="2891b-103">ProgrammaticAccessAllowed</span></span>

<span data-ttu-id="2891b-104">Das **ProgrammaticAccessAllowed** -Element gibt an, ob der programmgesteuerte Zugriff für rechteverwaltete Daten aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2891b-104">The **ProgrammaticAccessAllowed** element specifies whether programmatic access is enabled for rights managed data.</span></span> 
  
```XML
<ProgrammaticAccessAllowed> true | false </ProgrammaticAccessAllowed>
```

 <span data-ttu-id="2891b-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="2891b-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2891b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2891b-106">Attributes and elements</span></span>

<span data-ttu-id="2891b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2891b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2891b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2891b-108">Attributes</span></span>

<span data-ttu-id="2891b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2891b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2891b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2891b-110">Child elements</span></span>

<span data-ttu-id="2891b-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="2891b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2891b-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2891b-112">Parent elements</span></span>

[<span data-ttu-id="2891b-113">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="2891b-113">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md)
  
## <a name="text-value"></a><span data-ttu-id="2891b-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="2891b-114">Text value</span></span>

<span data-ttu-id="2891b-115">Der Textwert **true** für das **ProgrammaticAccessAllowed** -Element gibt an, dass auf die Daten programmgesteuert zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="2891b-115">A text value of **true** for the **ProgrammaticAccessAllowed** element indicates that the data is programmatically accessible.</span></span> <span data-ttu-id="2891b-116">Der Wert **false** gibt an, dass auf die Daten nicht programmgesteuert zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="2891b-116">A value of **false** indicates that the data is not programmatically accessible.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2891b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2891b-117">Remarks</span></span>

<span data-ttu-id="2891b-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2891b-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2891b-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="2891b-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2891b-120">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="2891b-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2891b-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="2891b-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2891b-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2891b-122">Schema name</span></span>  <br/> |<span data-ttu-id="2891b-123">Schematypen</span><span class="sxs-lookup"><span data-stu-id="2891b-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="2891b-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2891b-124">Validation file</span></span>  <br/> |<span data-ttu-id="2891b-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2891b-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2891b-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="2891b-126">Can be empty</span></span>  <br/> |<span data-ttu-id="2891b-127">false</span><span class="sxs-lookup"><span data-stu-id="2891b-127">false</span></span>  <br/> |
   

