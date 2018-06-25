---
title: SetTeamMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5d6ee7cc-8f88-4de2-ae5c-cabf2f2193d0
description: Das SetTeamMailbox -Element enthält eine Anforderung an ein websitepostfach festlegen.
ms.openlocfilehash: 708863168f4e89775deee8c5d66427df41515089
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831455"
---
# <a name="setteammailbox"></a><span data-ttu-id="95d8c-103">SetTeamMailbox</span><span class="sxs-lookup"><span data-stu-id="95d8c-103">SetTeamMailbox</span></span>

<span data-ttu-id="95d8c-104">Das **SetTeamMailbox** -Element enthält eine Anforderung an ein websitepostfach festlegen.</span><span class="sxs-lookup"><span data-stu-id="95d8c-104">The **SetTeamMailbox** element contains a request to set a site mailbox.</span></span> 
  
```XML
<SetTeamMailbox>
   <EmailAddress/>
   <SharePointSiteUrl/>
   <State/>
</SetTeamMailbox>
```

 <span data-ttu-id="95d8c-105">**SetTeamMailboxRequestType**</span><span class="sxs-lookup"><span data-stu-id="95d8c-105">**SetTeamMailboxRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="95d8c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="95d8c-106">Attributes and elements</span></span>

<span data-ttu-id="95d8c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="95d8c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="95d8c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="95d8c-108">Attributes</span></span>

<span data-ttu-id="95d8c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="95d8c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="95d8c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="95d8c-110">Child elements</span></span>

<span data-ttu-id="95d8c-111">[EmailAddress (EmailAddressType)](emailaddress-emailaddresstype.md) | [SharePointSiteUrl](sharepointsiteurl.md) | [Status (TeamMailboxLifecycleStateType)](state-teammailboxlifecyclestatetype.md)</span><span class="sxs-lookup"><span data-stu-id="95d8c-111">[EmailAddress (EmailAddressType)](emailaddress-emailaddresstype.md) | [SharePointSiteUrl](sharepointsiteurl.md) | [State (TeamMailboxLifecycleStateType)](state-teammailboxlifecyclestatetype.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="95d8c-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="95d8c-112">Parent elements</span></span>

<span data-ttu-id="95d8c-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="95d8c-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="95d8c-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="95d8c-114">Remarks</span></span>

<span data-ttu-id="95d8c-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="95d8c-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="95d8c-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="95d8c-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="95d8c-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="95d8c-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95d8c-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="95d8c-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="95d8c-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="95d8c-119">Schema name</span></span>  <br/> |<span data-ttu-id="95d8c-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="95d8c-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="95d8c-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="95d8c-121">Validation file</span></span>  <br/> |<span data-ttu-id="95d8c-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="95d8c-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="95d8c-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="95d8c-123">Can be empty</span></span>  <br/> ||
   

