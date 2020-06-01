---
title: UpdateItemInRecoverableItemsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2f61b038-eba0-40fc-8af2-c3db5cc5a420
description: Das UpdateItemInRecoverableItemsResponse-Element gibt die Antwort auf eine UpdateItemInRecoverableItems-Anforderung an.
ms.openlocfilehash: 02e030774949e895bc89579cb9364d08c7844ce3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466556"
---
# <a name="updateiteminrecoverableitemsresponse"></a><span data-ttu-id="6ae75-103">UpdateItemInRecoverableItemsResponse</span><span class="sxs-lookup"><span data-stu-id="6ae75-103">UpdateItemInRecoverableItemsResponse</span></span>

<span data-ttu-id="6ae75-104">Das **UpdateItemInRecoverableItemsResponse** -Element gibt die Antwort auf eine **UpdateItemInRecoverableItems** -Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="6ae75-104">The **UpdateItemInRecoverableItemsResponse** element specifies the response to an **UpdateItemInRecoverableItems** request.</span></span> 
  
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

 <span data-ttu-id="6ae75-105">**UpdateItemInRecoverableItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="6ae75-105">**UpdateItemInRecoverableItemsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6ae75-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6ae75-106">Attributes and elements</span></span>

<span data-ttu-id="6ae75-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6ae75-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6ae75-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6ae75-108">Attributes</span></span>

<span data-ttu-id="6ae75-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6ae75-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6ae75-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6ae75-110">Child elements</span></span>

<span data-ttu-id="6ae75-111">[MessageText](messagetext.md)  |  [Response Code](responsecode.md)  |  [DescriptiveLinkKey](descriptivelinkkey.md)  |  [Messagexml verwendet](messagexml.md)  |  [Elemente](items.md)  |  [Anlagen](attachments-ex15websvcsotherref.md)  |  [ConflictResults](conflictresults.md)</span><span class="sxs-lookup"><span data-stu-id="6ae75-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [Items](items.md) | [Attachments](attachments-ex15websvcsotherref.md) | [ConflictResults](conflictresults.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6ae75-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6ae75-112">Parent elements</span></span>

<span data-ttu-id="6ae75-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="6ae75-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6ae75-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ae75-114">Remarks</span></span>

<span data-ttu-id="6ae75-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6ae75-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="6ae75-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="6ae75-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6ae75-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="6ae75-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6ae75-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="6ae75-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6ae75-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6ae75-119">Schema name</span></span>  <br/> |<span data-ttu-id="6ae75-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="6ae75-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6ae75-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6ae75-121">Validation file</span></span>  <br/> |<span data-ttu-id="6ae75-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="6ae75-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6ae75-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="6ae75-123">Can be empty</span></span>  <br/> |<span data-ttu-id="6ae75-124">false</span><span class="sxs-lookup"><span data-stu-id="6ae75-124">false</span></span>  <br/> |
   

