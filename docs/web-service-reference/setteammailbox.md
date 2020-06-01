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
ms.openlocfilehash: e4b7ebd308f4b58b6b6491289f24b9176c5dcf15
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465261"
---
# <a name="setteammailbox"></a><span data-ttu-id="daa1e-103">SetTeamMailbox</span><span class="sxs-lookup"><span data-stu-id="daa1e-103">SetTeamMailbox</span></span>

<span data-ttu-id="daa1e-104">Das **SetTeamMailbox** -Element enthält eine Anforderung an ein websitepostfach festlegen.</span><span class="sxs-lookup"><span data-stu-id="daa1e-104">The **SetTeamMailbox** element contains a request to set a site mailbox.</span></span> 
  
```XML
<SetTeamMailbox>
   <EmailAddress/>
   <SharePointSiteUrl/>
   <State/>
</SetTeamMailbox>
```

 <span data-ttu-id="daa1e-105">**SetTeamMailboxRequestType**</span><span class="sxs-lookup"><span data-stu-id="daa1e-105">**SetTeamMailboxRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="daa1e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="daa1e-106">Attributes and elements</span></span>

<span data-ttu-id="daa1e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="daa1e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="daa1e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="daa1e-108">Attributes</span></span>

<span data-ttu-id="daa1e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="daa1e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="daa1e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="daa1e-110">Child elements</span></span>

<span data-ttu-id="daa1e-111">[EmailAddress (EmailAddressType)](emailaddress-emailaddresstype.md) | [SharePointSiteUrl](sharepointsiteurl.md) | [Status (TeamMailboxLifecycleStateType)](state-teammailboxlifecyclestatetype.md)</span><span class="sxs-lookup"><span data-stu-id="daa1e-111">[EmailAddress (EmailAddressType)](emailaddress-emailaddresstype.md) | [SharePointSiteUrl](sharepointsiteurl.md) | [State (TeamMailboxLifecycleStateType)](state-teammailboxlifecyclestatetype.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="daa1e-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="daa1e-112">Parent elements</span></span>

<span data-ttu-id="daa1e-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="daa1e-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="daa1e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="daa1e-114">Remarks</span></span>

<span data-ttu-id="daa1e-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="daa1e-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="daa1e-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="daa1e-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="daa1e-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="daa1e-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="daa1e-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="daa1e-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="daa1e-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="daa1e-119">Schema name</span></span>  <br/> |<span data-ttu-id="daa1e-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="daa1e-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="daa1e-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="daa1e-121">Validation file</span></span>  <br/> |<span data-ttu-id="daa1e-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="daa1e-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="daa1e-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="daa1e-123">Can be empty</span></span>  <br/> ||
   

