---
title: IsManagedFoldersRoot
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsManagedFoldersRoot
api_type:
- schema
ms.assetid: 00823fb9-bf8b-49bb-8e1b-d698c6d4063f
description: Das IsManagedFoldersRoot-Element gibt an, ob der verwaltete Ordner der Stamm für alle verwalteten Ordner ist.
ms.openlocfilehash: 4373dba9dce92de8e175948d889f0806e100fa6c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466024"
---
# <a name="ismanagedfoldersroot"></a><span data-ttu-id="8260c-103">IsManagedFoldersRoot</span><span class="sxs-lookup"><span data-stu-id="8260c-103">IsManagedFoldersRoot</span></span>

<span data-ttu-id="8260c-104">Das **IsManagedFoldersRoot** -Element gibt an, ob der verwaltete Ordner der Stamm für alle verwalteten Ordner ist.</span><span class="sxs-lookup"><span data-stu-id="8260c-104">The **IsManagedFoldersRoot** element indicates whether the managed folder is the root for all managed folders.</span></span> 
  
```xml
<IsManagedFoldersRoot/>
```

 <span data-ttu-id="8260c-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="8260c-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8260c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8260c-106">Attributes and elements</span></span>

<span data-ttu-id="8260c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8260c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8260c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8260c-108">Attributes</span></span>

<span data-ttu-id="8260c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="8260c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8260c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8260c-110">Child elements</span></span>

<span data-ttu-id="8260c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="8260c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8260c-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8260c-112">Parent elements</span></span>

|<span data-ttu-id="8260c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="8260c-113">**Element**</span></span>|<span data-ttu-id="8260c-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8260c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8260c-115">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="8260c-115">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="8260c-116">Enthält Informationen zu einem verwalteten Ordner.</span><span class="sxs-lookup"><span data-stu-id="8260c-116">Contains information about a managed folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8260c-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="8260c-117">Text value</span></span>

<span data-ttu-id="8260c-118">Ein Textwert, der einen booleschen Wert darstellt, ist erforderlich, wenn dieses Element vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="8260c-118">A text value that represents a Boolean value is required if this element is present.</span></span> <span data-ttu-id="8260c-119">Der Wert **true** gibt an, dass der Ordner der Stammordner des verwalteten Ordners ist. der Wert **false** gibt an, dass der Ordner nicht der Stammordner des verwalteten Ordners ist.</span><span class="sxs-lookup"><span data-stu-id="8260c-119">A value of **true** indicates that the folder is the root folder of the managed folder; a value of **false** indicates that the folder is not the root folder of the managed folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8260c-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8260c-120">Remarks</span></span>

<span data-ttu-id="8260c-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="8260c-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8260c-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="8260c-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8260c-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="8260c-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8260c-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8260c-124">Schema name</span></span>  <br/> |<span data-ttu-id="8260c-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="8260c-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="8260c-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8260c-126">Validation file</span></span>  <br/> |<span data-ttu-id="8260c-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8260c-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8260c-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="8260c-128">Can be empty</span></span>  <br/> |<span data-ttu-id="8260c-129">False</span><span class="sxs-lookup"><span data-stu-id="8260c-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8260c-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8260c-130">See also</span></span>



- [<span data-ttu-id="8260c-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8260c-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

