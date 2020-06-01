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
ms.openlocfilehash: a6b01bfa9c5908765ff04ef7f5edbef0b99a9be2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467242"
---
# <a name="unpinteammailbox"></a><span data-ttu-id="8a834-103">UnpinTeamMailbox</span><span class="sxs-lookup"><span data-stu-id="8a834-103">UnpinTeamMailbox</span></span>

<span data-ttu-id="8a834-104">Das **UnpinTeamMailbox** -Element enthält die Anforderung an ein websitepostfach vom Client zu lösen, entfernen Sie es aus der **Autodiscover** Antwort.</span><span class="sxs-lookup"><span data-stu-id="8a834-104">The **UnpinTeamMailbox** element contains the request to unpin a site mailbox from the client by removing it from the **Autodiscover** response.</span></span> 
  
```XML
<UnpinTeamMailbox>
   <EmailAddress/>
</UnpinTeamMailbox>
```

 <span data-ttu-id="8a834-105">**UnpinTeamMailboxRequestType**</span><span class="sxs-lookup"><span data-stu-id="8a834-105">**UnpinTeamMailboxRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8a834-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8a834-106">Attributes and elements</span></span>

<span data-ttu-id="8a834-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8a834-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8a834-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8a834-108">Attributes</span></span>

<span data-ttu-id="8a834-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="8a834-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8a834-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8a834-110">Child elements</span></span>

[<span data-ttu-id="8a834-111">E-mailemail (e-)</span><span class="sxs-lookup"><span data-stu-id="8a834-111">EmailAddress (EmailAddressType)</span></span>](emailaddress-emailaddresstype.md)
  
### <a name="parent-elements"></a><span data-ttu-id="8a834-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8a834-112">Parent elements</span></span>

<span data-ttu-id="8a834-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="8a834-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8a834-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a834-114">Remarks</span></span>

<span data-ttu-id="8a834-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8a834-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8a834-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="8a834-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8a834-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="8a834-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8a834-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="8a834-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8a834-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8a834-119">Schema name</span></span>  <br/> |<span data-ttu-id="8a834-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="8a834-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8a834-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8a834-121">Validation file</span></span>  <br/> |<span data-ttu-id="8a834-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="8a834-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8a834-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="8a834-123">Can be empty</span></span>  <br/> ||
   

