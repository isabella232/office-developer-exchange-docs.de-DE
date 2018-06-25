---
title: UnpinTeamMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1034b013-ef34-4e72-99b3-38bff475b3e8
description: Das UnpinTeamMailbox -Element enthält die Anforderung an ein websitepostfach vom Client zu lösen, entfernen Sie es aus der Autodiscover Antwort.
ms.openlocfilehash: d303b47f0796f9bec7e9f198afa81d2ecd9fd5cd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839319"
---
# <a name="unpinteammailbox"></a><span data-ttu-id="2a0b3-103">UnpinTeamMailbox</span><span class="sxs-lookup"><span data-stu-id="2a0b3-103">UnpinTeamMailbox</span></span>

<span data-ttu-id="2a0b3-104">Das **UnpinTeamMailbox** -Element enthält die Anforderung an ein websitepostfach vom Client zu lösen, entfernen Sie es aus der **Autodiscover** Antwort.</span><span class="sxs-lookup"><span data-stu-id="2a0b3-104">The **UnpinTeamMailbox** element contains the request to unpin a site mailbox from the client by removing it from the **Autodiscover** response.</span></span> 
  
```XML
<UnpinTeamMailbox>
   <EmailAddress/>
</UnpinTeamMailbox>
```

 <span data-ttu-id="2a0b3-105">**UnpinTeamMailboxRequestType**</span><span class="sxs-lookup"><span data-stu-id="2a0b3-105">**UnpinTeamMailboxRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2a0b3-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2a0b3-106">Attributes and elements</span></span>

<span data-ttu-id="2a0b3-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2a0b3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2a0b3-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2a0b3-108">Attributes</span></span>

<span data-ttu-id="2a0b3-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2a0b3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2a0b3-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2a0b3-110">Child elements</span></span>

[<span data-ttu-id="2a0b3-111">EmailAddress (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="2a0b3-111">EmailAddress (EmailAddressType)</span></span>](emailaddress-emailaddresstype.md)
  
### <a name="parent-elements"></a><span data-ttu-id="2a0b3-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2a0b3-112">Parent elements</span></span>

<span data-ttu-id="2a0b3-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="2a0b3-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2a0b3-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2a0b3-114">Remarks</span></span>

<span data-ttu-id="2a0b3-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2a0b3-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2a0b3-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="2a0b3-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2a0b3-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="2a0b3-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2a0b3-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="2a0b3-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2a0b3-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2a0b3-119">Schema name</span></span>  <br/> |<span data-ttu-id="2a0b3-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="2a0b3-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2a0b3-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2a0b3-121">Validation file</span></span>  <br/> |<span data-ttu-id="2a0b3-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2a0b3-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2a0b3-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="2a0b3-123">Can be empty</span></span>  <br/> ||
   

