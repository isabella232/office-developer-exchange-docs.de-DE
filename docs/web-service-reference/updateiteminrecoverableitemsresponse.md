---
title: UpdateItemInRecoverableItemsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2f61b038-eba0-40fc-8af2-c3db5cc5a420
description: Das UpdateItemInRecoverableItemsResponse-Element gibt die Antwort auf eine Anforderung UpdateItemInRecoverableItems.
ms.openlocfilehash: 2cb9bcb2752599a546c1391d6ea306735b3b0c78
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839378"
---
# <a name="updateiteminrecoverableitemsresponse"></a><span data-ttu-id="2a30b-103">UpdateItemInRecoverableItemsResponse</span><span class="sxs-lookup"><span data-stu-id="2a30b-103">UpdateItemInRecoverableItemsResponse</span></span>

<span data-ttu-id="2a30b-104">Das **UpdateItemInRecoverableItemsResponse** -Element gibt die Antwort auf eine Anforderung **UpdateItemInRecoverableItems** .</span><span class="sxs-lookup"><span data-stu-id="2a30b-104">The **UpdateItemInRecoverableItemsResponse** element specifies the response to an **UpdateItemInRecoverableItems** request.</span></span> 
  
```XML
<UpdateItemInRecoverableItemsResponse>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
   <Attachments/>
   <ConflictResults/>
</UpdateItemInRecoverableItemsResponse>
```

 <span data-ttu-id="2a30b-105">**UpdateItemInRecoverableItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2a30b-105">**UpdateItemInRecoverableItemsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2a30b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2a30b-106">Attributes and elements</span></span>

<span data-ttu-id="2a30b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2a30b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2a30b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2a30b-108">Attributes</span></span>

<span data-ttu-id="2a30b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2a30b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2a30b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2a30b-110">Child elements</span></span>

<span data-ttu-id="2a30b-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [Elemente](items.md) | [Anlagen](attachments-ex15websvcsotherref.md) | [ConflictResults](conflictresults.md)</span><span class="sxs-lookup"><span data-stu-id="2a30b-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [Items](items.md) | [Attachments](attachments-ex15websvcsotherref.md) | [ConflictResults](conflictresults.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2a30b-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2a30b-112">Parent elements</span></span>

<span data-ttu-id="2a30b-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="2a30b-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2a30b-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2a30b-114">Remarks</span></span>

<span data-ttu-id="2a30b-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2a30b-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2a30b-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="2a30b-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2a30b-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="2a30b-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2a30b-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="2a30b-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2a30b-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2a30b-119">Schema name</span></span>  <br/> |<span data-ttu-id="2a30b-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="2a30b-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2a30b-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2a30b-121">Validation file</span></span>  <br/> |<span data-ttu-id="2a30b-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2a30b-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2a30b-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="2a30b-123">Can be empty</span></span>  <br/> |<span data-ttu-id="2a30b-124">false</span><span class="sxs-lookup"><span data-stu-id="2a30b-124">false</span></span>  <br/> |
   

