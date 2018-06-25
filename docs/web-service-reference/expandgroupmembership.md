---
title: ExpandGroupMembership
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8989e96b-8fa1-4858-93b2-2cbdb30b9ca9
description: Das ExpandGroupMembership-Element gibt an, ob die Mitgliedschaft der Gruppe zurückgegeben, die aus einer Anforderung GetSearchableMailboxes erweitern.
ms.openlocfilehash: 11bfcf6893a147c726c94df77f7d9a9dfbaa773e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758317"
---
# <a name="expandgroupmembership"></a><span data-ttu-id="7bac7-103">ExpandGroupMembership</span><span class="sxs-lookup"><span data-stu-id="7bac7-103">ExpandGroupMembership</span></span>

<span data-ttu-id="7bac7-104">Das **ExpandGroupMembership** -Element gibt an, ob die Mitgliedschaft der Gruppe zurückgegeben, die aus einer Anforderung **GetSearchableMailboxes** erweitern.</span><span class="sxs-lookup"><span data-stu-id="7bac7-104">The **ExpandGroupMembership** element indicates whether to expand the membership of the group returned from a **GetSearchableMailboxes** request.</span></span> 
  
```XML
<ExpandGroupMembership>true | false</ExpandGroupMembership>
```

 <span data-ttu-id="7bac7-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7bac7-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7bac7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7bac7-106">Attributes and elements</span></span>

<span data-ttu-id="7bac7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7bac7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7bac7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7bac7-108">Attributes</span></span>

<span data-ttu-id="7bac7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7bac7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7bac7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7bac7-110">Child elements</span></span>

<span data-ttu-id="7bac7-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="7bac7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7bac7-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7bac7-112">Parent elements</span></span>

<span data-ttu-id="7bac7-113">[GetDiscoverySearchConfiguration](getdiscoverysearchconfiguration.md) | [GetSearchableMailboxes](getsearchablemailboxes.md)</span><span class="sxs-lookup"><span data-stu-id="7bac7-113">[GetDiscoverySearchConfiguration](getdiscoverysearchconfiguration.md) | [GetSearchableMailboxes](getsearchablemailboxes.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="7bac7-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="7bac7-114">Text value</span></span>

<span data-ttu-id="7bac7-115">Der Textwert **true** für das **ExpandGroupElement** -Element gibt an, dass die Gruppenmitgliedschaft erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="7bac7-115">A text value of **true** for the **ExpandGroupElement** element indicates that group membership is expanded.</span></span> <span data-ttu-id="7bac7-116">Der Wert **false** gibt an, dass die Gruppenmitgliedschaft nicht erweitert wird, damit die Mitglieder der Gruppe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7bac7-116">A value of **false** indicates that the group membership is not expanded to show the members of the group.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7bac7-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7bac7-117">Remarks</span></span>

<span data-ttu-id="7bac7-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7bac7-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7bac7-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7bac7-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7bac7-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7bac7-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7bac7-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="7bac7-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7bac7-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7bac7-122">Schema name</span></span>  <br/> |<span data-ttu-id="7bac7-123">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="7bac7-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7bac7-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7bac7-124">Validation file</span></span>  <br/> |<span data-ttu-id="7bac7-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7bac7-125">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7bac7-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="7bac7-126">Can be empty</span></span>  <br/> |<span data-ttu-id="7bac7-127">false</span><span class="sxs-lookup"><span data-stu-id="7bac7-127">false</span></span>  <br/> |
   

