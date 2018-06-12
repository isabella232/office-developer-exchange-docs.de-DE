---
title: GetNonIndexableItemDetailsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 00566965-6cbd-4f31-9fa9-85b3e5559c0c
description: Das GetNonIndexableItemDetailsResponseMessage-Element gibt die Antwortnachricht für eine Anforderung GetNonIndexableItemDetails.
ms.openlocfilehash: 8df67294c17f9c9b786e73647878ad5b3586d788
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758739"
---
# <a name="getnonindexableitemdetailsresponsemessage"></a><span data-ttu-id="1b9de-103">GetNonIndexableItemDetailsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1b9de-103">GetNonIndexableItemDetailsResponseMessage</span></span>

<span data-ttu-id="1b9de-104">Das **GetNonIndexableItemDetailsResponseMessage** -Element gibt die Antwortnachricht für eine Anforderung **GetNonIndexableItemDetails** .</span><span class="sxs-lookup"><span data-stu-id="1b9de-104">The **GetNonIndexableItemDetailsResponseMessage** element specifies the response message for a **GetNonIndexableItemDetails** request.</span></span> 
  
```XML
<GetNonIndexableItemDetailsResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <NonIndexableItemDetailsResult/>
</GetNonIndexableItemDetailsResponseMessage>
```

 <span data-ttu-id="1b9de-105">**GetNonIndexableItemDetailsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="1b9de-105">**GetNonIndexableItemDetailsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1b9de-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1b9de-106">Attributes and elements</span></span>

<span data-ttu-id="1b9de-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1b9de-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1b9de-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1b9de-108">Attributes</span></span>

<span data-ttu-id="1b9de-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1b9de-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1b9de-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1b9de-110">Child elements</span></span>

<span data-ttu-id="1b9de-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [NonIndexableItemDetailsResult](nonindexableitemdetailsresult.md)</span><span class="sxs-lookup"><span data-stu-id="1b9de-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [NonIndexableItemDetailsResult](nonindexableitemdetailsresult.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1b9de-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1b9de-112">Parent elements</span></span>

[<span data-ttu-id="1b9de-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="1b9de-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="1b9de-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1b9de-114">Remarks</span></span>

<span data-ttu-id="1b9de-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1b9de-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1b9de-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1b9de-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1b9de-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1b9de-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1b9de-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="1b9de-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1b9de-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1b9de-119">Schema name</span></span>  <br/> |<span data-ttu-id="1b9de-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="1b9de-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1b9de-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1b9de-121">Validation file</span></span>  <br/> |<span data-ttu-id="1b9de-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1b9de-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1b9de-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="1b9de-123">Can be empty</span></span>  <br/> |<span data-ttu-id="1b9de-124">false</span><span class="sxs-lookup"><span data-stu-id="1b9de-124">false</span></span>  <br/> |
   

