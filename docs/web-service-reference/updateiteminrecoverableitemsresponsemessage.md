---
title: UpdateItemInRecoverableItemsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 96259756-322e-4c24-ac76-0cd9c32e0d6d
description: Das UpdateItemInRecoverableItemsResponseMessage-Element gibt die Antwort auf eine UpdateItemInRecoverableItems-Anforderung an.
ms.openlocfilehash: 021631f5c30eebbf4d7ae0aad35a85b99a23925f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466535"
---
# <a name="updateiteminrecoverableitemsresponsemessage"></a><span data-ttu-id="93ebb-103">UpdateItemInRecoverableItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="93ebb-103">UpdateItemInRecoverableItemsResponseMessage</span></span>

<span data-ttu-id="93ebb-104">Das **UpdateItemInRecoverableItemsResponseMessage** -Element gibt die Antwort auf eine **UpdateItemInRecoverableItems** -Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="93ebb-104">The **UpdateItemInRecoverableItemsResponseMessage** element specifies the response to an **UpdateItemInRecoverableItems** request.</span></span> 
  
```XML
<UpdateItemInRecoverableItemsResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKet/>
   <MessageXml/>
   <Items/>
   <Attachments/>
   <ConflictResults/>
</UpdateItemInRecoverableItemsResponseMessage>
```

 <span data-ttu-id="93ebb-105">**UpdateItemInRecoverableItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="93ebb-105">**UpdateItemInRecoverableItemsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="93ebb-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="93ebb-106">Attributes and elements</span></span>

<span data-ttu-id="93ebb-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="93ebb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="93ebb-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="93ebb-108">Attributes</span></span>

<span data-ttu-id="93ebb-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="93ebb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="93ebb-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="93ebb-110">Child elements</span></span>

<span data-ttu-id="93ebb-111">[MessageText](messagetext.md)  |  [Response Code](responsecode.md)  |  [DescriptiveLinkKey](descriptivelinkkey.md)  |  [Messagexml verwendet](messagexml.md)  |  [Elemente](items.md)  |  [Anlagen](attachments-ex15websvcsotherref.md)  |  [ConflictResults](conflictresults.md)</span><span class="sxs-lookup"><span data-stu-id="93ebb-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [Items](items.md) | [Attachments](attachments-ex15websvcsotherref.md) | [ConflictResults](conflictresults.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="93ebb-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="93ebb-112">Parent elements</span></span>

<span data-ttu-id="93ebb-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="93ebb-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="93ebb-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="93ebb-114">Remarks</span></span>

<span data-ttu-id="93ebb-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="93ebb-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="93ebb-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="93ebb-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="93ebb-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="93ebb-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="93ebb-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="93ebb-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/message  <br/> |
|<span data-ttu-id="93ebb-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="93ebb-119">Schema name</span></span>  <br/> |<span data-ttu-id="93ebb-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="93ebb-120">Message schema</span></span>  <br/> |
|<span data-ttu-id="93ebb-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="93ebb-121">Validation file</span></span>  <br/> |<span data-ttu-id="93ebb-122">Message. xsd</span><span class="sxs-lookup"><span data-stu-id="93ebb-122">Message.xsd</span></span>  <br/> |
|<span data-ttu-id="93ebb-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="93ebb-123">Can be empty</span></span>  <br/> |<span data-ttu-id="93ebb-124">False</span><span class="sxs-lookup"><span data-stu-id="93ebb-124">false</span></span>  <br/> |
   

