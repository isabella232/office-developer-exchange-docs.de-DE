---
title: SearchDumpster
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ddb62dce-c87a-4714-8023-a6b697a29699
description: Das SearchDumpster-Element gibt an, ob im Exchange-Papierkorb gesucht werden soll.
ms.openlocfilehash: 067bf8ea3e589aa392c6b8ba6d4dc10b430c1f28
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460491"
---
# <a name="searchdumpster"></a><span data-ttu-id="43bad-103">SearchDumpster</span><span class="sxs-lookup"><span data-stu-id="43bad-103">SearchDumpster</span></span>

<span data-ttu-id="43bad-104">Das **SearchDumpster** -Element gibt an, ob im Exchange-Papierkorb gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="43bad-104">The **SearchDumpster** element specifies whether to search in the Exchange Dumpster.</span></span> 
  
```XML
<SearchDumpster> true | false </SearchDumpster>
```

 ****
## <a name="attributes-and-elements"></a><span data-ttu-id="43bad-105">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="43bad-105">Attributes and elements</span></span>

<span data-ttu-id="43bad-106">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="43bad-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="43bad-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="43bad-107">Attributes</span></span>

<span data-ttu-id="43bad-108">Keine.</span><span class="sxs-lookup"><span data-stu-id="43bad-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="43bad-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="43bad-109">Child elements</span></span>

<span data-ttu-id="43bad-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="43bad-110">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="43bad-111">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="43bad-111">Parent elements</span></span>

[<span data-ttu-id="43bad-112">FindMailboxStatisticsByKeywords</span><span class="sxs-lookup"><span data-stu-id="43bad-112">FindMailboxStatisticsByKeywords</span></span>](findmailboxstatisticsbykeywords.md)
  
## <a name="text-value"></a><span data-ttu-id="43bad-113">Textwert</span><span class="sxs-lookup"><span data-stu-id="43bad-113">Text value</span></span>

<span data-ttu-id="43bad-114">Der Textwert **true** für das **SearchDumpster** -Element gibt an, dass die Postfachstatistik-Suche den Exchange-Papierkorb enthält.</span><span class="sxs-lookup"><span data-stu-id="43bad-114">A text value of **true** for the **SearchDumpster** element indicates that the mailbox statistics search includes the Exchange Dumpster.</span></span> <span data-ttu-id="43bad-115">Der Wert **false** gibt an, dass der Exchange-Papierkorb nicht durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="43bad-115">A value of **false** indicates that the Exchange Dumpster is not searched.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="43bad-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43bad-116">Remarks</span></span>

<span data-ttu-id="43bad-117">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="43bad-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="43bad-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="43bad-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="43bad-119">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="43bad-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="43bad-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="43bad-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="43bad-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="43bad-121">Schema name</span></span>  <br/> |<span data-ttu-id="43bad-122">Schematypen</span><span class="sxs-lookup"><span data-stu-id="43bad-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="43bad-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="43bad-123">Validation file</span></span>  <br/> |<span data-ttu-id="43bad-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="43bad-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="43bad-125">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="43bad-125">Can be empty</span></span>  <br/> ||
   

