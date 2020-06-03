---
title: GetSearchableMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 949871f7-0d10-498e-84aa-f0652f1193be
description: Das GetSearchableMailboxes-Element enthält eine Anforderung zum Abrufen einer Liste von Postfächern, für die der Client über die Berechtigung zum Ausführen einer eDiscovery-Suche verfügt.
ms.openlocfilehash: a327f8766e53e9f1fae6928179d5a4b8e3d044a8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530190"
---
# <a name="getsearchablemailboxes"></a><span data-ttu-id="a0156-103">GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="a0156-103">GetSearchableMailboxes</span></span>

<span data-ttu-id="a0156-104">Das **GetSearchableMailboxes** -Element enthält eine Anforderung zum Abrufen einer Liste von Postfächern, für die der Client über die Berechtigung zum Ausführen einer eDiscovery-Suche verfügt.</span><span class="sxs-lookup"><span data-stu-id="a0156-104">The **GetSearchableMailboxes** element contains a request to get a list of mailboxes that the client has permission to perform an eDiscovery search.</span></span> 
  
```XML
<GetSearchableMailboxes>
   <SearchFilter/>
   <ExpandGroupMembership/>
</GetSearchableMailboxes>
```

 <span data-ttu-id="a0156-105">**GetSearchableMailboxesType**</span><span class="sxs-lookup"><span data-stu-id="a0156-105">**GetSearchableMailboxesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a0156-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a0156-106">Attributes and elements</span></span>

<span data-ttu-id="a0156-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a0156-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a0156-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a0156-108">Attributes</span></span>

<span data-ttu-id="a0156-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a0156-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a0156-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a0156-110">Child elements</span></span>

<span data-ttu-id="a0156-111">[SearchFilter](searchfilter.md)  |  [ExpandGroupMembership](expandgroupmembership.md)</span><span class="sxs-lookup"><span data-stu-id="a0156-111">[SearchFilter](searchfilter.md) | [ExpandGroupMembership](expandgroupmembership.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a0156-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a0156-112">Parent elements</span></span>

<span data-ttu-id="a0156-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="a0156-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a0156-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0156-114">Remarks</span></span>

<span data-ttu-id="a0156-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a0156-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a0156-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a0156-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a0156-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a0156-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a0156-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="a0156-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a0156-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a0156-119">Schema name</span></span>  <br/> |<span data-ttu-id="a0156-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="a0156-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a0156-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a0156-121">Validation file</span></span>  <br/> |<span data-ttu-id="a0156-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="a0156-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a0156-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a0156-123">Can be empty</span></span>  <br/> ||
   

