---
title: GetNonIndexableItemStatisticsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c969475a-238d-47ec-947a-fe3c53c8c1e9
description: Das GetNonIndexableItemStatisticsResponseMessage-Element gibt die Antwortnachricht für eine GetNonIndexableItemStatistics-Anforderung an.
ms.openlocfilehash: 351db85b16f8b0f5dd4bef0374ee0edb954a1083
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44452769"
---
# <a name="getnonindexableitemstatisticsresponsemessage"></a><span data-ttu-id="c2899-103">GetNonIndexableItemStatisticsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c2899-103">GetNonIndexableItemStatisticsResponseMessage</span></span>

<span data-ttu-id="c2899-104">Das **GetNonIndexableItemStatisticsResponseMessage** -Element gibt die Antwortnachricht für eine **GetNonIndexableItemStatistics** -Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="c2899-104">The **GetNonIndexableItemStatisticsResponseMessage** element specifies the response message for a **GetNonIndexableItemStatistics** request.</span></span> 
  
```XML
<GetNonIndexableItemStatisticsResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <NonIndexableItemStatistics/>
</GetNonIndexableItemStatisticsResponseMessage>
```

 <span data-ttu-id="c2899-105">**GetNonIndexableItemStatisticsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="c2899-105">**GetNonIndexableItemStatisticsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c2899-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c2899-106">Attributes and elements</span></span>

<span data-ttu-id="c2899-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c2899-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c2899-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c2899-108">Attributes</span></span>

<span data-ttu-id="c2899-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c2899-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c2899-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c2899-110">Child elements</span></span>

<span data-ttu-id="c2899-111">[MessageText](messagetext.md)  |  [Response Code](responsecode.md)  |  [DescriptiveLinkKey](descriptivelinkkey.md)  |  [Messagexml verwendet](messagexml.md)  |  [GetNonIndexableItemStatistics](getnonindexableitemstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="c2899-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [GetNonIndexableItemStatistics](getnonindexableitemstatistics.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c2899-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c2899-112">Parent elements</span></span>

[<span data-ttu-id="c2899-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c2899-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="c2899-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2899-114">Remarks</span></span>

<span data-ttu-id="c2899-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c2899-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c2899-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c2899-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c2899-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c2899-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c2899-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="c2899-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c2899-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c2899-119">Schema name</span></span>  <br/> |<span data-ttu-id="c2899-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="c2899-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c2899-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c2899-121">Validation file</span></span>  <br/> |<span data-ttu-id="c2899-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="c2899-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c2899-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="c2899-123">Can be empty</span></span>  <br/> |<span data-ttu-id="c2899-124">false</span><span class="sxs-lookup"><span data-stu-id="c2899-124">false</span></span>  <br/> |
   

