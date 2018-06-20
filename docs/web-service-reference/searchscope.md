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
ms.openlocfilehash: 352292952c735e7d3893790a660096c6b6966536
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831315"
---
# <a name="searchscope"></a><span data-ttu-id="bad77-103">SearchScope</span><span class="sxs-lookup"><span data-stu-id="bad77-103">SearchScope</span></span>

<span data-ttu-id="bad77-104">Das **SearchScope** -Element gibt den Bereich einer Suche an.</span><span class="sxs-lookup"><span data-stu-id="bad77-104">The **SearchScope** element specifies the scope of a search.</span></span> 
  
```XML
<SearchScope> PrimaryOnly | ArchiveOnly | All </SearchScope>
```

 <span data-ttu-id="bad77-105">**MailboxSearchLocationType**</span><span class="sxs-lookup"><span data-stu-id="bad77-105">**MailboxSearchLocationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bad77-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bad77-106">Attributes and elements</span></span>

<span data-ttu-id="bad77-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bad77-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bad77-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="bad77-108">Attributes</span></span>

<span data-ttu-id="bad77-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="bad77-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bad77-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bad77-110">Child elements</span></span>

<span data-ttu-id="bad77-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="bad77-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bad77-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bad77-112">Parent elements</span></span>

[<span data-ttu-id="bad77-113">MailboxSearchScope</span><span class="sxs-lookup"><span data-stu-id="bad77-113">MailboxSearchScope</span></span>](mailboxsearchscope.md)
  
## <a name="text-value"></a><span data-ttu-id="bad77-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="bad77-114">Text value</span></span>

<span data-ttu-id="bad77-115">Der Textwert des **SearchScope** -Elements gibt den Postfach an, die für eine discoverysuche durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="bad77-115">The text value of the **SearchScope** element indicates the mailbox type that is searched for a discovery search.</span></span> <span data-ttu-id="bad77-116">Der Textwert **PrimaryOnly** gibt an, dass das primäre Postfach gesucht wird.</span><span class="sxs-lookup"><span data-stu-id="bad77-116">A text value of **PrimaryOnly** indicates that the primary mailbox is searched.</span></span> <span data-ttu-id="bad77-117">Der Textwert **ArchiveOnly** gibt an, dass das Archivpostfach durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="bad77-117">A text value of **ArchiveOnly** indicates that the archive mailbox is searched.</span></span> <span data-ttu-id="bad77-118">Ein Text **Alle** gibt an, dass sowohl die primäre und archivpostfächer durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="bad77-118">A text value of **All** indicates that both the primary and archive mailboxes are searched.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bad77-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bad77-119">Remarks</span></span>

<span data-ttu-id="bad77-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="bad77-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="bad77-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="bad77-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bad77-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="bad77-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bad77-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="bad77-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bad77-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="bad77-124">Schema name</span></span>  <br/> |<span data-ttu-id="bad77-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="bad77-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="bad77-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="bad77-126">Validation file</span></span>  <br/> |<span data-ttu-id="bad77-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bad77-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bad77-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="bad77-128">Can be empty</span></span>  <br/> ||
   

