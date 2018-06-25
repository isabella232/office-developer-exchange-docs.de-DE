---
title: ServerReplyWithMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ServerReplyWithMessage
api_type:
- schema
ms.assetid: 113c6ff2-9592-44f0-b542-54e4d5122ccb
description: Das ServerReplyWithMessage-Element gibt die ID der Vorlagennachricht, die als Antwort auf eingehende Nachrichten gesendet werden sollen.
ms.openlocfilehash: f2d927ae18ac68523d4cdd173f0474fbbeb36c98
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831390"
---
# <a name="serverreplywithmessage"></a><span data-ttu-id="f8012-103">ServerReplyWithMessage</span><span class="sxs-lookup"><span data-stu-id="f8012-103">ServerReplyWithMessage</span></span>

<span data-ttu-id="f8012-104">Das **ServerReplyWithMessage** -Element gibt die ID der Vorlagennachricht, die als Antwort auf eingehende Nachrichten gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f8012-104">The **ServerReplyWithMessage** element indicates the ID of the template message that is to be sent as a reply to incoming messages.</span></span> 
  
```XML
<ServerReplyWithMessage>
    <ItemId>
</ServerReplyWithMessage>
```

 <span data-ttu-id="f8012-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="f8012-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f8012-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f8012-106">Attributes and elements</span></span>

<span data-ttu-id="f8012-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f8012-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f8012-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f8012-108">Attributes</span></span>

<span data-ttu-id="f8012-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f8012-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f8012-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f8012-110">Child elements</span></span>

|<span data-ttu-id="f8012-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f8012-111">**Element**</span></span>|<span data-ttu-id="f8012-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f8012-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f8012-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="f8012-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="f8012-114">Den eindeutigen Bezeichner und ein Änderungsprotokoll Schlüssel eines Elements in der Exchange-Speicher darstellt.</span><span class="sxs-lookup"><span data-stu-id="f8012-114">Represents the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f8012-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f8012-115">Parent elements</span></span>

|<span data-ttu-id="f8012-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="f8012-116">**Element**</span></span>|<span data-ttu-id="f8012-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f8012-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f8012-118">Aktionen</span><span class="sxs-lookup"><span data-stu-id="f8012-118">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="f8012-119">Repräsentiert den Satz von Aktionen, die sind verfügbar, die auf eine Nachricht durchgeführt werden, wenn die Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="f8012-119">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f8012-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="f8012-120">Text value</span></span>

<span data-ttu-id="f8012-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="f8012-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f8012-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f8012-122">Remarks</span></span>

<span data-ttu-id="f8012-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f8012-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f8012-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f8012-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f8012-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="f8012-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f8012-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f8012-126">Schema Name</span></span>  <br/> |<span data-ttu-id="f8012-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="f8012-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f8012-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f8012-128">Validation File</span></span>  <br/> |<span data-ttu-id="f8012-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f8012-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f8012-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f8012-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="f8012-131">True</span><span class="sxs-lookup"><span data-stu-id="f8012-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f8012-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8012-132">See also</span></span>



- [<span data-ttu-id="f8012-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f8012-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

