---
title: GetSearchableMailboxesResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0fcc2f53-742b-46ae-bbab-c3295a3d69e7
description: Das GetSearchableMailboxesResponse-Element enthält die Antwort auf eine GetSearchableMailboxes-Anforderung.
ms.openlocfilehash: 680fde9d9ad34dd0384e00da023796d004b66b1b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458264"
---
# <a name="getsearchablemailboxesresponse"></a><span data-ttu-id="86866-103">GetSearchableMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="86866-103">GetSearchableMailboxesResponse</span></span>

<span data-ttu-id="86866-104">Das **GetSearchableMailboxesResponse** -Element enthält die Antwort auf eine **GetSearchableMailboxes** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="86866-104">The **GetSearchableMailboxesResponse** element contains the response to a **GetSearchableMailboxes** request.</span></span> 
  
```XML
<GetSearchableMailboxesResponse>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <SearchableMailboxes/>
   <FailedMailboxes/>
</GetSearchableMailboxesResponse>
```

 <span data-ttu-id="86866-105">**GetSearchableMailboxesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="86866-105">**GetSearchableMailboxesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="86866-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="86866-106">Attributes and elements</span></span>

<span data-ttu-id="86866-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="86866-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="86866-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="86866-108">Attributes</span></span>

<span data-ttu-id="86866-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="86866-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="86866-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="86866-110">Child elements</span></span>

<span data-ttu-id="86866-111">[MessageText](messagetext.md)  |  [Response Code](responsecode.md)  |  [DescriptiveLinkKey](descriptivelinkkey.md)  |  [Messagexml verwendet](messagexml.md)  |  [SearchableMailboxes](searchablemailboxes.md)  |  [FailedMailboxes](failedmailboxes.md)</span><span class="sxs-lookup"><span data-stu-id="86866-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [SearchableMailboxes](searchablemailboxes.md) | [FailedMailboxes](failedmailboxes.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="86866-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="86866-112">Parent elements</span></span>

<span data-ttu-id="86866-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="86866-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="86866-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86866-114">Remarks</span></span>

<span data-ttu-id="86866-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="86866-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="86866-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="86866-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="86866-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="86866-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="86866-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="86866-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="86866-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="86866-119">Schema name</span></span>  <br/> |<span data-ttu-id="86866-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="86866-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="86866-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="86866-121">Validation file</span></span>  <br/> |<span data-ttu-id="86866-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="86866-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="86866-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="86866-123">Can be empty</span></span>  <br/> |<span data-ttu-id="86866-124">False</span><span class="sxs-lookup"><span data-stu-id="86866-124">false</span></span>  <br/> |
   

