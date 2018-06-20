---
title: IsPermanentFailure
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 18dc3a97-cc0a-4092-934e-a6e86f52e668
description: Das IsPermanentFailure-Element gibt an, ob es sich bei ein vorherigen Versuch zum Indizieren des Elements nicht erfolgreich war.
ms.openlocfilehash: 39592c15394a57e1c6aa1183ed0ccedeb085e6ea
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830085"
---
# <a name="ispermanentfailure"></a><span data-ttu-id="8134f-103">IsPermanentFailure</span><span class="sxs-lookup"><span data-stu-id="8134f-103">IsPermanentFailure</span></span>

<span data-ttu-id="8134f-104">Das **IsPermanentFailure** -Element gibt an, ob es sich bei ein vorherigen Versuch zum Indizieren des Elements nicht erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="8134f-104">The **IsPermanentFailure** element indicates whether a previous attempt to index the item was unsuccessful.</span></span> 
  
```XML
<IsPermanentFailure>true | false</IsPermanentFailure>
```

 <span data-ttu-id="8134f-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="8134f-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8134f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8134f-106">Attributes and elements</span></span>

<span data-ttu-id="8134f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8134f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8134f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8134f-108">Attributes</span></span>

<span data-ttu-id="8134f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="8134f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8134f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8134f-110">Child elements</span></span>

<span data-ttu-id="8134f-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="8134f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8134f-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8134f-112">Parent elements</span></span>

[<span data-ttu-id="8134f-113">NonIndexableItemDetail</span><span class="sxs-lookup"><span data-stu-id="8134f-113">NonIndexableItemDetail</span></span>](nonindexableitemdetail.md)
  
## <a name="text-value"></a><span data-ttu-id="8134f-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="8134f-114">Text value</span></span>

<span data-ttu-id="8134f-115">Der Textwert **true** für das **IsPermanentFailure** -Element gibt an, dass es sich bei ein vorherigen Versuch zum Indizieren des postfachelements nicht erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="8134f-115">A text value of **true** for the **IsPermanentFailure** element indicates that a previous attempt to index the mailbox item was unsuccessful.</span></span> <span data-ttu-id="8134f-116">Der Wert **false** gibt an, dass es sich bei ein vorherigen Versuch zum Indizieren des postfachelements erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="8134f-116">A value of **false** indicates that a previous attempt to index the mailbox item was successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8134f-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8134f-117">Remarks</span></span>

<span data-ttu-id="8134f-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8134f-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8134f-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="8134f-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8134f-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8134f-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8134f-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="8134f-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8134f-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8134f-122">Schema name</span></span>  <br/> |<span data-ttu-id="8134f-123">Schematypen</span><span class="sxs-lookup"><span data-stu-id="8134f-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="8134f-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8134f-124">Validation file</span></span>  <br/> |<span data-ttu-id="8134f-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8134f-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8134f-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="8134f-126">Can be empty</span></span>  <br/> |<span data-ttu-id="8134f-127">false</span><span class="sxs-lookup"><span data-stu-id="8134f-127">false</span></span>  <br/> |
   

