---
title: SearchScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4a53989e-eca6-45c4-afac-4d6ac19597d2
description: Das SearchScope-Element gibt den Bereich einer Suche an.
ms.openlocfilehash: df11c8db418ac90d1166030aeed3672c0b810052
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466864"
---
# <a name="searchscope"></a><span data-ttu-id="580eb-103">SearchScope</span><span class="sxs-lookup"><span data-stu-id="580eb-103">SearchScope</span></span>

<span data-ttu-id="580eb-104">Das **SearchScope** -Element gibt den Bereich einer Suche an.</span><span class="sxs-lookup"><span data-stu-id="580eb-104">The **SearchScope** element specifies the scope of a search.</span></span> 
  
```XML
<SearchScope> PrimaryOnly | ArchiveOnly | All </SearchScope>
```

 <span data-ttu-id="580eb-105">**MailboxSearchLocationType**</span><span class="sxs-lookup"><span data-stu-id="580eb-105">**MailboxSearchLocationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="580eb-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="580eb-106">Attributes and elements</span></span>

<span data-ttu-id="580eb-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="580eb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="580eb-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="580eb-108">Attributes</span></span>

<span data-ttu-id="580eb-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="580eb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="580eb-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="580eb-110">Child elements</span></span>

<span data-ttu-id="580eb-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="580eb-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="580eb-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="580eb-112">Parent elements</span></span>

[<span data-ttu-id="580eb-113">MailboxSearchScope</span><span class="sxs-lookup"><span data-stu-id="580eb-113">MailboxSearchScope</span></span>](mailboxsearchscope.md)
  
## <a name="text-value"></a><span data-ttu-id="580eb-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="580eb-114">Text value</span></span>

<span data-ttu-id="580eb-115">Der Textwert des **SearchScope** -Elements gibt den Postfachtyp an, der für eine Ermittlungs Suche durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="580eb-115">The text value of the **SearchScope** element indicates the mailbox type that is searched for a discovery search.</span></span> <span data-ttu-id="580eb-116">Der Textwert **Switch primaryonly** gibt an, dass das primäre Postfach durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="580eb-116">A text value of **PrimaryOnly** indicates that the primary mailbox is searched.</span></span> <span data-ttu-id="580eb-117">Der Textwert **Switch archiveonly** gibt an, dass das Archivpostfach durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="580eb-117">A text value of **ArchiveOnly** indicates that the archive mailbox is searched.</span></span> <span data-ttu-id="580eb-118">Ein Textwert von **all** gibt an, dass sowohl die primären als auch die Archivpostfächer durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="580eb-118">A text value of **All** indicates that both the primary and archive mailboxes are searched.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="580eb-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="580eb-119">Remarks</span></span>

<span data-ttu-id="580eb-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="580eb-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="580eb-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="580eb-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="580eb-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="580eb-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="580eb-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="580eb-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="580eb-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="580eb-124">Schema name</span></span>  <br/> |<span data-ttu-id="580eb-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="580eb-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="580eb-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="580eb-126">Validation file</span></span>  <br/> |<span data-ttu-id="580eb-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="580eb-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="580eb-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="580eb-128">Can be empty</span></span>  <br/> ||
   

