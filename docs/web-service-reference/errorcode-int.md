---
title: ErrorCode (Int)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 65537d96-edf9-41ee-9ad5-91ffe37e2269
description: ErrorCode-Element gibt den Fehlercode des einer fehlerhaften Suche für ein Postfach an.
ms.openlocfilehash: ed8a7771376f921303ea093f4be727c4146faa76
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758261"
---
# <a name="errorcode-int"></a><span data-ttu-id="c832b-103">ErrorCode (Int)</span><span class="sxs-lookup"><span data-stu-id="c832b-103">ErrorCode (int)</span></span>

<span data-ttu-id="c832b-104">**ErrorCode** -Element gibt den Fehlercode des einer fehlerhaften Suche für ein Postfach an.</span><span class="sxs-lookup"><span data-stu-id="c832b-104">The **ErrorCode** element specifies the error code of a failed search performed against a mailbox.</span></span> 
  
```XML
<ErrorCode></ErrorCode>
```

 <span data-ttu-id="c832b-105">**int**</span><span class="sxs-lookup"><span data-stu-id="c832b-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c832b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c832b-106">Attributes and elements</span></span>

<span data-ttu-id="c832b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c832b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c832b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c832b-108">Attributes</span></span>

<span data-ttu-id="c832b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c832b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c832b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c832b-110">Child elements</span></span>

<span data-ttu-id="c832b-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="c832b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c832b-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c832b-112">Parent elements</span></span>

|<span data-ttu-id="c832b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c832b-113">**Element**</span></span>|<span data-ttu-id="c832b-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c832b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c832b-115">FailedMailbox</span><span class="sxs-lookup"><span data-stu-id="c832b-115">FailedMailbox</span></span>](failedmailbox.md) <br/> |<span data-ttu-id="c832b-116">Gibt den Sperrstatus des Postfachs an.</span><span class="sxs-lookup"><span data-stu-id="c832b-116">Specifies the hold status of the mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c832b-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="c832b-117">Text value</span></span>

<span data-ttu-id="c832b-118">Der Textwert des **ErrorCode** -Elements ist die bei einer fehlgeschlagenen Suche für ein Postfach zurückgegebenen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="c832b-118">The text value of the **ErrorCode** element is the error code returned for a failed search performed against a mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c832b-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c832b-119">Remarks</span></span>

<span data-ttu-id="c832b-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c832b-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c832b-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c832b-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c832b-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c832b-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c832b-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="c832b-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c832b-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c832b-124">Schema Name</span></span>  <br/> |<span data-ttu-id="c832b-125">Typschema</span><span class="sxs-lookup"><span data-stu-id="c832b-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="c832b-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c832b-126">Validation File</span></span>  <br/> |<span data-ttu-id="c832b-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c832b-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="c832b-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="c832b-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="c832b-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c832b-129">See also</span></span>



- [<span data-ttu-id="c832b-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c832b-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

