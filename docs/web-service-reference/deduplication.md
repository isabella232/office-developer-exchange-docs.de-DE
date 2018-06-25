---
title: Datendeduplizierung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a38acc3d-29a8-4466-81a4-73cb30fe5e80
description: Das Deduplizierung-Element gibt an, ob das Suchergebnis Duplikate entfernt werden soll.
ms.openlocfilehash: 3f06bb1dccd0677b7fd43c4ad82eda54a0c3f812
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757891"
---
# <a name="deduplication"></a><span data-ttu-id="d76a0-103">Datendeduplizierung</span><span class="sxs-lookup"><span data-stu-id="d76a0-103">Deduplication</span></span>

<span data-ttu-id="d76a0-104">Das **Deduplizierung** -Element gibt an, ob das Suchergebnis Duplikate entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d76a0-104">The **Deduplication** element indicates whether the search result should remove duplicate items.</span></span> 
  
```XML
<Deduplication> true | false </Deduplication>
```

<span data-ttu-id="d76a0-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="d76a0-105">**Boolean**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d76a0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d76a0-106">Attributes and elements</span></span>

<span data-ttu-id="d76a0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d76a0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d76a0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d76a0-108">Attributes</span></span>

<span data-ttu-id="d76a0-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d76a0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d76a0-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d76a0-110">Child elements</span></span>

<span data-ttu-id="d76a0-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d76a0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d76a0-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d76a0-112">Parent elements</span></span>

<span data-ttu-id="d76a0-113">[SearchMailboxes](searchmailboxes.md) | [SetHoldOnMailboxes](setholdonmailboxes.md)</span><span class="sxs-lookup"><span data-stu-id="d76a0-113">[SearchMailboxes](searchmailboxes.md) | [SetHoldOnMailboxes](setholdonmailboxes.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="d76a0-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="d76a0-114">Text value</span></span>

<span data-ttu-id="d76a0-115">Der Textwert **true** für das Deduplizierung-Element gibt an, dass die Suchergebnisse möglicherweise keine Duplikate enthalten.</span><span class="sxs-lookup"><span data-stu-id="d76a0-115">A text value of **true** for the Deduplication element indicates that search results may not contain duplicate items.</span></span> <span data-ttu-id="d76a0-116">Der Wert **false** gibt an, dass Suchergebnisse doppelte Elemente enthalten können.</span><span class="sxs-lookup"><span data-stu-id="d76a0-116">A value of **false** indicates that search results may contain duplicate items.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d76a0-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d76a0-117">Remarks</span></span>

<span data-ttu-id="d76a0-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d76a0-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d76a0-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d76a0-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d76a0-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d76a0-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d76a0-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="d76a0-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d76a0-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d76a0-122">Schema name</span></span>  <br/> |<span data-ttu-id="d76a0-123">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d76a0-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="d76a0-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d76a0-124">Validation file</span></span>  <br/> |<span data-ttu-id="d76a0-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d76a0-125">types.xsd</span></span>  <br/> |
|<span data-ttu-id="d76a0-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="d76a0-126">Can be empty</span></span>  <br/> |<span data-ttu-id="d76a0-127">false</span><span class="sxs-lookup"><span data-stu-id="d76a0-127">false</span></span>  <br/> |
   

