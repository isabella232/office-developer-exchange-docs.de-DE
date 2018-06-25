---
title: GetSearchableMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 949871f7-0d10-498e-84aa-f0652f1193be
description: Das GetSearchableMailboxes-Element enthält eine Anforderung an einer Liste der Postfächer erhalten möchten, dass der Client über die Berechtigung zum Ausführen einer eDiscovery-Suche verfügt.
ms.openlocfilehash: 8cce18bb62d3840cb9883d20a380cc4f2193303e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758790"
---
# <a name="getsearchablemailboxes"></a><span data-ttu-id="9a6c0-103">GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="9a6c0-103">GetSearchableMailboxes</span></span>

<span data-ttu-id="9a6c0-104">Das **GetSearchableMailboxes** -Element enthält eine Anforderung an einer Liste der Postfächer erhalten möchten, dass der Client über die Berechtigung zum Ausführen einer eDiscovery-Suche verfügt.</span><span class="sxs-lookup"><span data-stu-id="9a6c0-104">The **GetSearchableMailboxes** element contains a request to get a list of mailboxes that the client has permission to perform an eDiscovery search.</span></span> 
  
```XML
<GetSearchableMailboxes>
   <SearchFilter/>
   <ExpandGroupMembership/>
</GetSearchableMailboxes>
```

 <span data-ttu-id="9a6c0-105">**GetSearchableMailboxesType**</span><span class="sxs-lookup"><span data-stu-id="9a6c0-105">**GetSearchableMailboxesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9a6c0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9a6c0-106">Attributes and elements</span></span>

<span data-ttu-id="9a6c0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9a6c0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9a6c0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9a6c0-108">Attributes</span></span>

<span data-ttu-id="9a6c0-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9a6c0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9a6c0-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9a6c0-110">Child elements</span></span>

<span data-ttu-id="9a6c0-111">[SearchFilter](searchfilter.md) | [ExpandGroupMembership](expandgroupmembership.md)</span><span class="sxs-lookup"><span data-stu-id="9a6c0-111">[SearchFilter](searchfilter.md) | [ExpandGroupMembership](expandgroupmembership.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9a6c0-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9a6c0-112">Parent elements</span></span>

<span data-ttu-id="9a6c0-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="9a6c0-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9a6c0-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9a6c0-114">Remarks</span></span>

<span data-ttu-id="9a6c0-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="9a6c0-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="9a6c0-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="9a6c0-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9a6c0-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9a6c0-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9a6c0-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="9a6c0-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9a6c0-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9a6c0-119">Schema name</span></span>  <br/> |<span data-ttu-id="9a6c0-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="9a6c0-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9a6c0-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9a6c0-121">Validation file</span></span>  <br/> |<span data-ttu-id="9a6c0-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9a6c0-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9a6c0-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="9a6c0-123">Can be empty</span></span>  <br/> ||
   

