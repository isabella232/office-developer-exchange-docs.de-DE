---
title: GetNonIndexableItemStatisticsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f68b73c-d6b0-4bb5-b89a-fd398d09346c
description: Das GetNonIndexableItemStatisticsResponse-Element gibt die Antwort auf eine GetNonIndexableItemStatistics an.
ms.openlocfilehash: 95f59df251517cb76183f6f8bd6c2d4a68bd4cdb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758745"
---
# <a name="getnonindexableitemstatisticsresponse"></a><span data-ttu-id="9f85b-103">GetNonIndexableItemStatisticsResponse</span><span class="sxs-lookup"><span data-stu-id="9f85b-103">GetNonIndexableItemStatisticsResponse</span></span>

<span data-ttu-id="9f85b-104">Das **GetNonIndexableItemStatisticsResponse** -Element gibt die Antwort auf eine **GetNonIndexableItemStatistics** an.</span><span class="sxs-lookup"><span data-stu-id="9f85b-104">The **GetNonIndexableItemStatisticsResponse** element specifies the response to a **GetNonIndexableItemStatistics** request.</span></span> 
  
```XML
<GetNonIndexableItemStatisticsResponse>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <NonIndexableItemStatistics/>
</GetNonIndexableItemStatisticsResponse>
```

 <span data-ttu-id="9f85b-105">**GetNonIndexableItemStatisticsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="9f85b-105">**GetNonIndexableItemStatisticsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9f85b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9f85b-106">Attributes and elements</span></span>

<span data-ttu-id="9f85b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9f85b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9f85b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9f85b-108">Attributes</span></span>

<span data-ttu-id="9f85b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9f85b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9f85b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9f85b-110">Child elements</span></span>

<span data-ttu-id="9f85b-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [GetNonIndexableItemStatistics](getnonindexableitemstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="9f85b-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [GetNonIndexableItemStatistics](getnonindexableitemstatistics.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9f85b-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9f85b-112">Parent elements</span></span>

[<span data-ttu-id="9f85b-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9f85b-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="9f85b-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9f85b-114">Remarks</span></span>

<span data-ttu-id="9f85b-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="9f85b-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="9f85b-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="9f85b-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9f85b-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9f85b-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9f85b-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="9f85b-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9f85b-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9f85b-119">Schema name</span></span>  <br/> |<span data-ttu-id="9f85b-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="9f85b-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9f85b-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9f85b-121">Validation file</span></span>  <br/> |<span data-ttu-id="9f85b-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9f85b-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9f85b-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="9f85b-123">Can be empty</span></span>  <br/> |<span data-ttu-id="9f85b-124">false</span><span class="sxs-lookup"><span data-stu-id="9f85b-124">false</span></span>  <br/> |
   

