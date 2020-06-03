---
title: MarkAsJunkResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3e2b7b53-ef3c-438e-93df-b08409dbab46
description: Das MarkAsJunkResponseMessage-Element gibt die Antwortnachricht für eine MarkAsJunk-Anforderung an.
ms.openlocfilehash: be03fc964b56c463320f09e68d143a0377300f5c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460099"
---
# <a name="markasjunkresponsemessage"></a><span data-ttu-id="ce19f-103">MarkAsJunkResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ce19f-103">MarkAsJunkResponseMessage</span></span>

<span data-ttu-id="ce19f-104">Das **MarkAsJunkResponseMessage** -Element gibt die Antwortnachricht für eine **MarkAsJunk** -Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="ce19f-104">The **MarkAsJunkResponseMessage** element specifies the response message for a **MarkAsJunk** request.</span></span> 
  
```XML
<MarkAsJunkResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <MovedItemId/>
</MarkAsJunkResponseMessage>
```

 <span data-ttu-id="ce19f-105">**MarkAsJunkResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ce19f-105">**MarkAsJunkResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ce19f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ce19f-106">Attributes and elements</span></span>

<span data-ttu-id="ce19f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ce19f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ce19f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ce19f-108">Attributes</span></span>

<span data-ttu-id="ce19f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ce19f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ce19f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ce19f-110">Child elements</span></span>

<span data-ttu-id="ce19f-111">[MessageText](messagetext.md)  |  [Response Code](responsecode.md)  |  [DescriptiveLinkKey](descriptivelinkkey.md)  |  [Messagexml verwendet](messagexml.md)  |  [MovedItemId](moveditemid.md)</span><span class="sxs-lookup"><span data-stu-id="ce19f-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [MovedItemId](moveditemid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ce19f-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ce19f-112">Parent elements</span></span>

[<span data-ttu-id="ce19f-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ce19f-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="ce19f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce19f-114">Remarks</span></span>

<span data-ttu-id="ce19f-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ce19f-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ce19f-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ce19f-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ce19f-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ce19f-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ce19f-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="ce19f-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ce19f-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ce19f-119">Schema name</span></span>  <br/> |<span data-ttu-id="ce19f-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ce19f-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ce19f-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ce19f-121">Validation file</span></span>  <br/> |<span data-ttu-id="ce19f-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ce19f-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ce19f-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="ce19f-123">Can be empty</span></span>  <br/> ||
   

