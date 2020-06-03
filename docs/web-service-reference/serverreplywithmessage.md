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
description: Das ServerReplyWithMessage-Element gibt die ID der Vorlagen Nachricht an, die als Antwort auf eingehende Nachrichten gesendet werden soll.
ms.openlocfilehash: faaa054018a17be3ff59b9fc385b3d846d39c3f1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461975"
---
# <a name="serverreplywithmessage"></a><span data-ttu-id="32585-103">ServerReplyWithMessage</span><span class="sxs-lookup"><span data-stu-id="32585-103">ServerReplyWithMessage</span></span>

<span data-ttu-id="32585-104">Das **ServerReplyWithMessage** -Element gibt die ID der Vorlagen Nachricht an, die als Antwort auf eingehende Nachrichten gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="32585-104">The **ServerReplyWithMessage** element indicates the ID of the template message that is to be sent as a reply to incoming messages.</span></span> 
  
```XML
<ServerReplyWithMessage>
    <ItemId>
</ServerReplyWithMessage>
```

 <span data-ttu-id="32585-105">**Itemidtype**</span><span class="sxs-lookup"><span data-stu-id="32585-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="32585-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="32585-106">Attributes and elements</span></span>

<span data-ttu-id="32585-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="32585-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="32585-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="32585-108">Attributes</span></span>

<span data-ttu-id="32585-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="32585-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="32585-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="32585-110">Child elements</span></span>

|<span data-ttu-id="32585-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="32585-111">**Element**</span></span>|<span data-ttu-id="32585-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="32585-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="32585-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="32585-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="32585-114">Stellt den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements in der Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="32585-114">Represents the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="32585-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="32585-115">Parent elements</span></span>

|<span data-ttu-id="32585-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="32585-116">**Element**</span></span>|<span data-ttu-id="32585-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="32585-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="32585-118">Aktionen</span><span class="sxs-lookup"><span data-stu-id="32585-118">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="32585-119">Repräsentiert den Satz von Aktionen, die sind verfügbar, die auf eine Nachricht durchgeführt werden, wenn die Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="32585-119">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="32585-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="32585-120">Text value</span></span>

<span data-ttu-id="32585-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="32585-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="32585-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32585-122">Remarks</span></span>

<span data-ttu-id="32585-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="32585-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="32585-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="32585-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="32585-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="32585-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="32585-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="32585-126">Schema Name</span></span>  <br/> |<span data-ttu-id="32585-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="32585-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="32585-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="32585-128">Validation File</span></span>  <br/> |<span data-ttu-id="32585-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="32585-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="32585-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="32585-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="32585-131">True</span><span class="sxs-lookup"><span data-stu-id="32585-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="32585-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32585-132">See also</span></span>



- [<span data-ttu-id="32585-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="32585-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

