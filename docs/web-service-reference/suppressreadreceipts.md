---
title: SuppressReadReceipts
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f0805560-7a2f-455b-94d2-ec4f1e3652c3
description: Die SuppressReadReceipts, die Element gibt an, ob Lese-Empfangsbestätigungen sollten unterdrückt werden.
ms.openlocfilehash: 794252da6b3e6b6e6f36181c1811a2a001bfaf53
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839142"
---
# <a name="suppressreadreceipts"></a><span data-ttu-id="af226-103">SuppressReadReceipts</span><span class="sxs-lookup"><span data-stu-id="af226-103">SuppressReadReceipts</span></span>

<span data-ttu-id="af226-104">Das Element **SuppressReadReceipts** gibt an, ob Lese-Empfangsbestätigungen unterdrückt werden soll.</span><span class="sxs-lookup"><span data-stu-id="af226-104">The **SuppressReadReceipts** element indicates whether read receipts should be suppressed.</span></span> 
  
```XML
<SuppressReadReceipts>true | false</SuppressReadReceipts>
```

 <span data-ttu-id="af226-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="af226-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="af226-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="af226-106">Attributes and elements</span></span>

<span data-ttu-id="af226-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="af226-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="af226-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="af226-108">Attributes</span></span>

<span data-ttu-id="af226-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="af226-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="af226-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="af226-110">Child elements</span></span>

<span data-ttu-id="af226-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="af226-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="af226-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="af226-112">Parent elements</span></span>

<span data-ttu-id="af226-113">[ConversationAction](conversationaction.md) | [MarkAllItemsAsRead](markallitemsasread.md)</span><span class="sxs-lookup"><span data-stu-id="af226-113">[ConversationAction](conversationaction.md) | [MarkAllItemsAsRead](markallitemsasread.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="af226-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="af226-114">Text value</span></span>

<span data-ttu-id="af226-115">Der Textwert **true** für das **SuppressReadReciepts** -Element gibt an, dass das Read, Empfangsbestätigungen unterdrückt werden.</span><span class="sxs-lookup"><span data-stu-id="af226-115">A text value of **true** for the **SuppressReadReciepts** element indicates that read receipts are suppressed.</span></span> <span data-ttu-id="af226-116">Der Wert **false** gibt an, dass das Read, die Bestätigung an den Absender gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="af226-116">A value of **false** indicates that read receipts will be sent to the sender.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="af226-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="af226-117">Remarks</span></span>

<span data-ttu-id="af226-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="af226-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="af226-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="af226-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="af226-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="af226-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="af226-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="af226-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="af226-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="af226-122">Schema name</span></span>  <br/> |<span data-ttu-id="af226-123">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="af226-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="af226-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="af226-124">Validation file</span></span>  <br/> |<span data-ttu-id="af226-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="af226-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="af226-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="af226-126">Can be empty</span></span>  <br/> ||
   

