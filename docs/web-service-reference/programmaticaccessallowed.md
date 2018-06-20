---
title: ProgrammaticAccessAllowed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a1fc7dff-a303-4809-b7f4-9672f86c183c
description: Das ProgrammaticAccessAllowed-Element gibt an, ob für die Verwaltung von Informationsrechten verwaltete Daten programmgesteuerter Zugriff aktiviert ist.
ms.openlocfilehash: 50bcce745bd94bf9c2e5ced93825722307e0a096
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830889"
---
# <a name="programmaticaccessallowed"></a><span data-ttu-id="ae258-103">ProgrammaticAccessAllowed</span><span class="sxs-lookup"><span data-stu-id="ae258-103">ProgrammaticAccessAllowed</span></span>

<span data-ttu-id="ae258-104">Das **ProgrammaticAccessAllowed** -Element gibt an, ob für die Verwaltung von Informationsrechten verwaltete Daten programmgesteuerter Zugriff aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ae258-104">The **ProgrammaticAccessAllowed** element specifies whether programmatic access is enabled for rights managed data.</span></span> 
  
```XML
<ProgrammaticAccessAllowed> true | false </ProgrammaticAccessAllowed>
```

 <span data-ttu-id="ae258-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="ae258-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ae258-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ae258-106">Attributes and elements</span></span>

<span data-ttu-id="ae258-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ae258-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ae258-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ae258-108">Attributes</span></span>

<span data-ttu-id="ae258-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ae258-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ae258-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ae258-110">Child elements</span></span>

<span data-ttu-id="ae258-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ae258-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ae258-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ae258-112">Parent elements</span></span>

[<span data-ttu-id="ae258-113">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="ae258-113">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md)
  
## <a name="text-value"></a><span data-ttu-id="ae258-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="ae258-114">Text value</span></span>

<span data-ttu-id="ae258-115">Der Textwert **true** für das **ProgrammaticAccessAllowed** -Element gibt an, dass die Daten programmgesteuert zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="ae258-115">A text value of **true** for the **ProgrammaticAccessAllowed** element indicates that the data is programmatically accessible.</span></span> <span data-ttu-id="ae258-116">Der Wert **false** gibt an, dass die Daten nicht programmgesteuert zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="ae258-116">A value of **false** indicates that the data is not programmatically accessible.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ae258-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ae258-117">Remarks</span></span>

<span data-ttu-id="ae258-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ae258-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ae258-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ae258-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ae258-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ae258-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae258-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="ae258-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ae258-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ae258-122">Schema name</span></span>  <br/> |<span data-ttu-id="ae258-123">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ae258-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="ae258-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ae258-124">Validation file</span></span>  <br/> |<span data-ttu-id="ae258-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ae258-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ae258-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="ae258-126">Can be empty</span></span>  <br/> |<span data-ttu-id="ae258-127">false</span><span class="sxs-lookup"><span data-stu-id="ae258-127">false</span></span>  <br/> |
   

