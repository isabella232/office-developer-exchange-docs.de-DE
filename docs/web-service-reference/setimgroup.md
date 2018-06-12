---
title: SetImGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3c107b8d-714b-4cd5-ad1b-97b7cbcb90d6
description: Das Element SetImGroup stellt eine Anforderung an den Anzeigenamen einer instant messaging-Gruppe ändern.
ms.openlocfilehash: 67fd8188e3436d5042a2867fe54e673348cba807
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831422"
---
# <a name="setimgroup"></a><span data-ttu-id="b9bc6-103">SetImGroup</span><span class="sxs-lookup"><span data-stu-id="b9bc6-103">SetImGroup</span></span>

<span data-ttu-id="b9bc6-104">Das Element **SetImGroup** stellt eine Anforderung an den Anzeigenamen einer instant messaging-Gruppe ändern.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-104">The **SetImGroup** element represents a request to change the display name of an instant messaging group.</span></span> 
  
```XML
<SetImGroup>
   <GroupId/>
   <NewDisplayName/>
</SetImGroup>
```

 <span data-ttu-id="b9bc6-105">**SetImGroupType**</span><span class="sxs-lookup"><span data-stu-id="b9bc6-105">**SetImGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b9bc6-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b9bc6-106">Attributes and elements</span></span>

<span data-ttu-id="b9bc6-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b9bc6-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b9bc6-108">Attributes</span></span>

<span data-ttu-id="b9bc6-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b9bc6-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b9bc6-110">Child elements</span></span>

<span data-ttu-id="b9bc6-111">[GroupId](groupid.md) | [NewDisplayName](newdisplayname.md)</span><span class="sxs-lookup"><span data-stu-id="b9bc6-111">[GroupId](groupid.md) | [NewDisplayName](newdisplayname.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b9bc6-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b9bc6-112">Parent elements</span></span>

<span data-ttu-id="b9bc6-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b9bc6-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b9bc6-114">Remarks</span></span>

<span data-ttu-id="b9bc6-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b9bc6-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b9bc6-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b9bc6-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b9bc6-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="b9bc6-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b9bc6-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b9bc6-119">Schema name</span></span>  <br/> |<span data-ttu-id="b9bc6-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="b9bc6-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b9bc6-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b9bc6-121">Validation file</span></span>  <br/> |<span data-ttu-id="b9bc6-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b9bc6-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b9bc6-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b9bc6-123">Can be empty</span></span>  <br/> ||
   

