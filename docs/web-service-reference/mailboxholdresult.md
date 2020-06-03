---
title: MailboxHoldResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: da03b877-37c6-4ecb-8549-c639f140302e
description: Das MailboxHoldResult-Element enthält das Ergebnis der GetHoldOnMailboxes-Anforderung.
ms.openlocfilehash: 3895c1351587db45881c661809a19dad1929b4a9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466395"
---
# <a name="mailboxholdresult"></a><span data-ttu-id="06c48-103">MailboxHoldResult</span><span class="sxs-lookup"><span data-stu-id="06c48-103">MailboxHoldResult</span></span>

<span data-ttu-id="06c48-104">Das **MailboxHoldResult** -Element enthält das Ergebnis der **GetHoldOnMailboxes** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="06c48-104">The **MailboxHoldResult** element contains the result of the **GetHoldOnMailboxes** request.</span></span> 
  
```XML
<MailboxHoldResult>
   <HoldId/>
   <Query/>
   <MailboxHoldStatuses/>
</MailboxHoldResult>
```

<span data-ttu-id="06c48-105">**MailboxHoldResultType**</span><span class="sxs-lookup"><span data-stu-id="06c48-105">**MailboxHoldResultType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="06c48-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="06c48-106">Attributes and elements</span></span>

<span data-ttu-id="06c48-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="06c48-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="06c48-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="06c48-108">Attributes</span></span>

<span data-ttu-id="06c48-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="06c48-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="06c48-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="06c48-110">Child elements</span></span>

<span data-ttu-id="06c48-111">[Haltestatus](holdid.md)  |  [Abfrage](query.md)  |  [MailboxHoldStatuses](mailboxholdstatuses.md)</span><span class="sxs-lookup"><span data-stu-id="06c48-111">[HoldId](holdid.md) | [Query](query.md) | [MailboxHoldStatuses](mailboxholdstatuses.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="06c48-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="06c48-112">Parent elements</span></span>

<span data-ttu-id="06c48-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="06c48-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="06c48-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06c48-114">Remarks</span></span>

<span data-ttu-id="06c48-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="06c48-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="06c48-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="06c48-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="06c48-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="06c48-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="06c48-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="06c48-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="06c48-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="06c48-119">Schema name</span></span>  <br/> |<span data-ttu-id="06c48-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="06c48-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="06c48-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="06c48-121">Validation file</span></span>  <br/> |<span data-ttu-id="06c48-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="06c48-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="06c48-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="06c48-123">Can be empty</span></span>  <br/> ||
   

