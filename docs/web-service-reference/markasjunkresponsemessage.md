---
title: MarkAsJunkResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3e2b7b53-ef3c-438e-93df-b08409dbab46
description: Das MarkAsJunkResponseMessage-Element gibt die Antwortnachricht für eine Anforderung MarkAsJunk.
ms.openlocfilehash: 146ece430436c60fced53d4dfbfd7d92c0e42e98
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830352"
---
# <a name="markasjunkresponsemessage"></a><span data-ttu-id="23c3a-103">MarkAsJunkResponseMessage</span><span class="sxs-lookup"><span data-stu-id="23c3a-103">MarkAsJunkResponseMessage</span></span>

<span data-ttu-id="23c3a-104">Das **MarkAsJunkResponseMessage** -Element gibt die Antwortnachricht für eine Anforderung **MarkAsJunk** .</span><span class="sxs-lookup"><span data-stu-id="23c3a-104">The **MarkAsJunkResponseMessage** element specifies the response message for a **MarkAsJunk** request.</span></span> 
  
```XML
<MarkAsJunkResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <MovedItemId/>
</MarkAsJunkResponseMessage>
```

 <span data-ttu-id="23c3a-105">**MarkAsJunkResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="23c3a-105">**MarkAsJunkResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="23c3a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="23c3a-106">Attributes and elements</span></span>

<span data-ttu-id="23c3a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="23c3a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="23c3a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="23c3a-108">Attributes</span></span>

<span data-ttu-id="23c3a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="23c3a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="23c3a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="23c3a-110">Child elements</span></span>

<span data-ttu-id="23c3a-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [MovedItemId](moveditemid.md)</span><span class="sxs-lookup"><span data-stu-id="23c3a-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [MovedItemId](moveditemid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="23c3a-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="23c3a-112">Parent elements</span></span>

[<span data-ttu-id="23c3a-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="23c3a-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="23c3a-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="23c3a-114">Remarks</span></span>

<span data-ttu-id="23c3a-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="23c3a-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="23c3a-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="23c3a-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="23c3a-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="23c3a-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="23c3a-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="23c3a-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="23c3a-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="23c3a-119">Schema name</span></span>  <br/> |<span data-ttu-id="23c3a-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="23c3a-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="23c3a-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="23c3a-121">Validation file</span></span>  <br/> |<span data-ttu-id="23c3a-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="23c3a-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="23c3a-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="23c3a-123">Can be empty</span></span>  <br/> ||
   

