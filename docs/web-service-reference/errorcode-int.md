---
title: ErrorCode (Int)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 65537d96-edf9-41ee-9ad5-91ffe37e2269
description: Das ErrorCode-Element gibt den Fehlercode einer fehlgeschlagenen Suche an, die für ein Postfach ausgeführt wird.
ms.openlocfilehash: 24170a56e5fa23c3811fcbd27f0240e6ba3c87b7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460666"
---
# <a name="errorcode-int"></a><span data-ttu-id="1103c-103">ErrorCode (Int)</span><span class="sxs-lookup"><span data-stu-id="1103c-103">ErrorCode (int)</span></span>

<span data-ttu-id="1103c-104">Das **errorCode** -Element gibt den Fehlercode einer fehlgeschlagenen Suche an, die für ein Postfach ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1103c-104">The **ErrorCode** element specifies the error code of a failed search performed against a mailbox.</span></span> 
  
```XML
<ErrorCode></ErrorCode>
```

 <span data-ttu-id="1103c-105">**int**</span><span class="sxs-lookup"><span data-stu-id="1103c-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1103c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1103c-106">Attributes and elements</span></span>

<span data-ttu-id="1103c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1103c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1103c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1103c-108">Attributes</span></span>

<span data-ttu-id="1103c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1103c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1103c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1103c-110">Child elements</span></span>

<span data-ttu-id="1103c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="1103c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1103c-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1103c-112">Parent elements</span></span>

|<span data-ttu-id="1103c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1103c-113">**Element**</span></span>|<span data-ttu-id="1103c-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1103c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1103c-115">FailedMailbox</span><span class="sxs-lookup"><span data-stu-id="1103c-115">FailedMailbox</span></span>](failedmailbox.md) <br/> |<span data-ttu-id="1103c-116">Gibt den Aufbewahrungs Status des Postfachs an.</span><span class="sxs-lookup"><span data-stu-id="1103c-116">Specifies the hold status of the mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1103c-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="1103c-117">Text value</span></span>

<span data-ttu-id="1103c-118">Der Textwert des **errorCode** -Elements ist der Fehlercode, der für eine fehlerhafte Suche zurückgegeben wurde, die für ein Postfach ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="1103c-118">The text value of the **ErrorCode** element is the error code returned for a failed search performed against a mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1103c-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1103c-119">Remarks</span></span>

<span data-ttu-id="1103c-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1103c-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1103c-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1103c-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1103c-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="1103c-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1103c-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="1103c-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1103c-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1103c-124">Schema Name</span></span>  <br/> |<span data-ttu-id="1103c-125">Typschema</span><span class="sxs-lookup"><span data-stu-id="1103c-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="1103c-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1103c-126">Validation File</span></span>  <br/> |<span data-ttu-id="1103c-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="1103c-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="1103c-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="1103c-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="1103c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1103c-129">See also</span></span>



- [<span data-ttu-id="1103c-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1103c-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

