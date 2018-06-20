---
title: ResultType-Wert
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 488ee828-343f-4382-a5e8-eed1005f5dbc
description: Das ResultType-Wert-Element enthält den Typ der auszuführenden Suche an. Der Typ der Suche kann werden nur Statistiken oder nur eine Vorschau anzeigen.
ms.openlocfilehash: 750f53ae05a7ad9f5aefc9396911a23ef32cdfc2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831211"
---
# <a name="resulttype"></a><span data-ttu-id="7e731-104">ResultType-Wert</span><span class="sxs-lookup"><span data-stu-id="7e731-104">ResultType</span></span>

<span data-ttu-id="7e731-105">Das **ResultType-Wert** -Element enthält den Typ der auszuführenden Suche an.</span><span class="sxs-lookup"><span data-stu-id="7e731-105">The **ResultType** element contains the type of search to perform.</span></span> <span data-ttu-id="7e731-106">Der Typ der Suche kann werden nur Statistiken oder nur eine Vorschau anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7e731-106">The type of search can be statistics only or preview only.</span></span> 
  
```XML
<ResultType>StatisticsOnly | PreviewOnly</ResultType>
```

 <span data-ttu-id="7e731-107">**SearchResultType**</span><span class="sxs-lookup"><span data-stu-id="7e731-107">**SearchResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7e731-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7e731-108">Attributes and elements</span></span>

<span data-ttu-id="7e731-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7e731-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7e731-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="7e731-110">Attributes</span></span>

<span data-ttu-id="7e731-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="7e731-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7e731-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7e731-112">Child elements</span></span>

<span data-ttu-id="7e731-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="7e731-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7e731-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7e731-114">Parent elements</span></span>

<span data-ttu-id="7e731-115">[SearchMailboxesResult](searchmailboxesresult.md) | [SearchMailboxes](searchmailboxes.md)</span><span class="sxs-lookup"><span data-stu-id="7e731-115">[SearchMailboxesResult](searchmailboxesresult.md) | [SearchMailboxes](searchmailboxes.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="7e731-116">Textwert</span><span class="sxs-lookup"><span data-stu-id="7e731-116">Text value</span></span>

<span data-ttu-id="7e731-117">Der Textwert des Elements **ResultType-Wert** ist der Typ des Ergebnisses, die für eine discoverysuche zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7e731-117">The text value of the **ResultType** element is the type of result that is returned for a discovery search.</span></span> <span data-ttu-id="7e731-118">Ein Textwert der **StatisticsOnly** gibt die Suchstatistik zurück.</span><span class="sxs-lookup"><span data-stu-id="7e731-118">A text value of **StatisticsOnly** will return the search statistics.</span></span> <span data-ttu-id="7e731-119">Ein Textwert der **PreviewOnly** gibt Element Vorschauinformationen zurück.</span><span class="sxs-lookup"><span data-stu-id="7e731-119">A text value of **PreviewOnly** will return item preview information.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7e731-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7e731-120">Remarks</span></span>

<span data-ttu-id="7e731-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7e731-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7e731-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7e731-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7e731-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7e731-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7e731-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="7e731-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7e731-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7e731-125">Schema name</span></span>  <br/> |<span data-ttu-id="7e731-126">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="7e731-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7e731-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7e731-127">Validation file</span></span>  <br/> |<span data-ttu-id="7e731-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7e731-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7e731-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="7e731-129">Can be empty</span></span>  <br/> |<span data-ttu-id="7e731-130">false</span><span class="sxs-lookup"><span data-stu-id="7e731-130">false</span></span>  <br/> |
   

