---
title: IsPermanentFailure
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 18dc3a97-cc0a-4092-934e-a6e86f52e668
description: Das IsPermanentFailure-Element gibt an, ob ein vorheriger Versuch, das Element zu indizieren, nicht erfolgreich war.
ms.openlocfilehash: 48a13eebfa16c538c1b10d92f080d51f1b318d12
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460393"
---
# <a name="ispermanentfailure"></a><span data-ttu-id="b4a2e-103">IsPermanentFailure</span><span class="sxs-lookup"><span data-stu-id="b4a2e-103">IsPermanentFailure</span></span>

<span data-ttu-id="b4a2e-104">Das **IsPermanentFailure** -Element gibt an, ob ein vorheriger Versuch, das Element zu indizieren, nicht erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="b4a2e-104">The **IsPermanentFailure** element indicates whether a previous attempt to index the item was unsuccessful.</span></span> 
  
```XML
<IsPermanentFailure>true | false</IsPermanentFailure>
```

 <span data-ttu-id="b4a2e-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="b4a2e-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b4a2e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b4a2e-106">Attributes and elements</span></span>

<span data-ttu-id="b4a2e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b4a2e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b4a2e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b4a2e-108">Attributes</span></span>

<span data-ttu-id="b4a2e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b4a2e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b4a2e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b4a2e-110">Child elements</span></span>

<span data-ttu-id="b4a2e-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b4a2e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b4a2e-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b4a2e-112">Parent elements</span></span>

[<span data-ttu-id="b4a2e-113">NonIndexableItemDetail</span><span class="sxs-lookup"><span data-stu-id="b4a2e-113">NonIndexableItemDetail</span></span>](nonindexableitemdetail.md)
  
## <a name="text-value"></a><span data-ttu-id="b4a2e-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="b4a2e-114">Text value</span></span>

<span data-ttu-id="b4a2e-115">Der Textwert **true** für das **IsPermanentFailure** -Element gibt an, dass ein vorheriger Versuch zum Indizieren des Post Fach Elements nicht erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="b4a2e-115">A text value of **true** for the **IsPermanentFailure** element indicates that a previous attempt to index the mailbox item was unsuccessful.</span></span> <span data-ttu-id="b4a2e-116">Der Wert **false** gibt an, dass ein vorheriger Versuch, das Postfachelement zu indizieren, erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="b4a2e-116">A value of **false** indicates that a previous attempt to index the mailbox item was successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b4a2e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4a2e-117">Remarks</span></span>

<span data-ttu-id="b4a2e-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b4a2e-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b4a2e-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b4a2e-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b4a2e-120">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b4a2e-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b4a2e-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="b4a2e-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b4a2e-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b4a2e-122">Schema name</span></span>  <br/> |<span data-ttu-id="b4a2e-123">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b4a2e-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="b4a2e-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b4a2e-124">Validation file</span></span>  <br/> |<span data-ttu-id="b4a2e-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b4a2e-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b4a2e-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b4a2e-126">Can be empty</span></span>  <br/> |<span data-ttu-id="b4a2e-127">false</span><span class="sxs-lookup"><span data-stu-id="b4a2e-127">false</span></span>  <br/> |
   

