---
title: GetSearchableMailboxesResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0fcc2f53-742b-46ae-bbab-c3295a3d69e7
description: Das GetSearchableMailboxesResponse-Element enthält die Antwort auf eine GetSearchableMailboxes an.
ms.openlocfilehash: 35a671cd534d1b48b29ef836c24d97d7cbd52401
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758798"
---
# <a name="getsearchablemailboxesresponse"></a><span data-ttu-id="8b1f1-103">GetSearchableMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="8b1f1-103">GetSearchableMailboxesResponse</span></span>

<span data-ttu-id="8b1f1-104">Das **GetSearchableMailboxesResponse** -Element enthält die Antwort auf eine **GetSearchableMailboxes** an.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-104">The **GetSearchableMailboxesResponse** element contains the response to a **GetSearchableMailboxes** request.</span></span> 
  
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

 <span data-ttu-id="8b1f1-105">**GetSearchableMailboxesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="8b1f1-105">**GetSearchableMailboxesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8b1f1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8b1f1-106">Attributes and elements</span></span>

<span data-ttu-id="8b1f1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8b1f1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8b1f1-108">Attributes</span></span>

<span data-ttu-id="8b1f1-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8b1f1-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8b1f1-110">Child elements</span></span>

<span data-ttu-id="8b1f1-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [SearchableMailboxes](searchablemailboxes.md) | [FailedMailboxes](failedmailboxes.md)</span><span class="sxs-lookup"><span data-stu-id="8b1f1-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [SearchableMailboxes](searchablemailboxes.md) | [FailedMailboxes](failedmailboxes.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8b1f1-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8b1f1-112">Parent elements</span></span>

<span data-ttu-id="8b1f1-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8b1f1-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8b1f1-114">Remarks</span></span>

<span data-ttu-id="8b1f1-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8b1f1-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="8b1f1-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8b1f1-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8b1f1-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8b1f1-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="8b1f1-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8b1f1-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8b1f1-119">Schema name</span></span>  <br/> |<span data-ttu-id="8b1f1-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="8b1f1-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8b1f1-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8b1f1-121">Validation file</span></span>  <br/> |<span data-ttu-id="8b1f1-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8b1f1-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8b1f1-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="8b1f1-123">Can be empty</span></span>  <br/> |<span data-ttu-id="8b1f1-124">false</span><span class="sxs-lookup"><span data-stu-id="8b1f1-124">false</span></span>  <br/> |
   

