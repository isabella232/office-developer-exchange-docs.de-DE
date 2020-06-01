---
title: ResultType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 488ee828-343f-4382-a5e8-eed1005f5dbc
description: Das ResultType-Element enthält den Typ der durchzuführenden Suche. Bei der Art der Suche kann es sich nur um Statistik oder nur um eine Vorschau handeln.
ms.openlocfilehash: 6617c8b4b64cd9b6728317d7247bcc5378e488f0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465282"
---
# <a name="resulttype"></a><span data-ttu-id="c5dec-104">ResultType</span><span class="sxs-lookup"><span data-stu-id="c5dec-104">ResultType</span></span>

<span data-ttu-id="c5dec-105">Das **ResultType** -Element enthält den Typ der durchzuführenden Suche.</span><span class="sxs-lookup"><span data-stu-id="c5dec-105">The **ResultType** element contains the type of search to perform.</span></span> <span data-ttu-id="c5dec-106">Bei der Art der Suche kann es sich nur um Statistik oder nur um eine Vorschau handeln.</span><span class="sxs-lookup"><span data-stu-id="c5dec-106">The type of search can be statistics only or preview only.</span></span> 
  
```XML
<ResultType>StatisticsOnly | PreviewOnly</ResultType>
```

 <span data-ttu-id="c5dec-107">**Searchresulttype**</span><span class="sxs-lookup"><span data-stu-id="c5dec-107">**SearchResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c5dec-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c5dec-108">Attributes and elements</span></span>

<span data-ttu-id="c5dec-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c5dec-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c5dec-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="c5dec-110">Attributes</span></span>

<span data-ttu-id="c5dec-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="c5dec-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c5dec-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c5dec-112">Child elements</span></span>

<span data-ttu-id="c5dec-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="c5dec-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c5dec-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c5dec-114">Parent elements</span></span>

<span data-ttu-id="c5dec-115">[SearchMailboxesResult](searchmailboxesresult.md)  |  [SearchMailboxes](searchmailboxes.md)</span><span class="sxs-lookup"><span data-stu-id="c5dec-115">[SearchMailboxesResult](searchmailboxesresult.md) | [SearchMailboxes](searchmailboxes.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="c5dec-116">Textwert</span><span class="sxs-lookup"><span data-stu-id="c5dec-116">Text value</span></span>

<span data-ttu-id="c5dec-117">Der Textwert des **ResultType** -Elements ist der Typ des Ergebnisses, der für eine Ermittlungs Suche zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c5dec-117">The text value of the **ResultType** element is the type of result that is returned for a discovery search.</span></span> <span data-ttu-id="c5dec-118">Der Textwert **StatisticsOnly** gibt die Suchstatistik zurück.</span><span class="sxs-lookup"><span data-stu-id="c5dec-118">A text value of **StatisticsOnly** will return the search statistics.</span></span> <span data-ttu-id="c5dec-119">Ein Textwert von **PreviewOnly** gibt Informationen zur Elementvorschau zurück.</span><span class="sxs-lookup"><span data-stu-id="c5dec-119">A text value of **PreviewOnly** will return item preview information.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c5dec-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5dec-120">Remarks</span></span>

<span data-ttu-id="c5dec-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c5dec-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c5dec-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c5dec-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c5dec-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c5dec-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c5dec-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="c5dec-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c5dec-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c5dec-125">Schema name</span></span>  <br/> |<span data-ttu-id="c5dec-126">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="c5dec-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c5dec-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c5dec-127">Validation file</span></span>  <br/> |<span data-ttu-id="c5dec-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="c5dec-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c5dec-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="c5dec-129">Can be empty</span></span>  <br/> |<span data-ttu-id="c5dec-130">false</span><span class="sxs-lookup"><span data-stu-id="c5dec-130">false</span></span>  <br/> |
   

