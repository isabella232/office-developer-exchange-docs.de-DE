---
title: SuppressReadReceipts
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f0805560-7a2f-455b-94d2-ec4f1e3652c3
description: Das SuppressReadReceipts-Element gibt an, ob Lesebestätigungen unterdrückt werden sollen.
ms.openlocfilehash: aa604d4907582bd73727ba664958a589a222f9cb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455933"
---
# <a name="suppressreadreceipts"></a><span data-ttu-id="c9857-103">SuppressReadReceipts</span><span class="sxs-lookup"><span data-stu-id="c9857-103">SuppressReadReceipts</span></span>

<span data-ttu-id="c9857-104">Das **SuppressReadReceipts** -Element gibt an, ob Lesebestätigungen unterdrückt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c9857-104">The **SuppressReadReceipts** element indicates whether read receipts should be suppressed.</span></span> 
  
```XML
<SuppressReadReceipts>true | false</SuppressReadReceipts>
```

 <span data-ttu-id="c9857-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="c9857-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c9857-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c9857-106">Attributes and elements</span></span>

<span data-ttu-id="c9857-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c9857-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c9857-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c9857-108">Attributes</span></span>

<span data-ttu-id="c9857-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c9857-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c9857-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c9857-110">Child elements</span></span>

<span data-ttu-id="c9857-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="c9857-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c9857-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c9857-112">Parent elements</span></span>

<span data-ttu-id="c9857-113">[Unterhaltung](conversationaction.md)  |  [MarkAllItemsAsRead](markallitemsasread.md)</span><span class="sxs-lookup"><span data-stu-id="c9857-113">[ConversationAction](conversationaction.md) | [MarkAllItemsAsRead](markallitemsasread.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="c9857-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="c9857-114">Text value</span></span>

<span data-ttu-id="c9857-115">Der Textwert **true** für das **SuppressReadReciepts** -Element gibt an, dass Lesebestätigungen unterdrückt werden.</span><span class="sxs-lookup"><span data-stu-id="c9857-115">A text value of **true** for the **SuppressReadReciepts** element indicates that read receipts are suppressed.</span></span> <span data-ttu-id="c9857-116">Der Wert **false** gibt an, dass Lesebestätigungen an den Absender gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="c9857-116">A value of **false** indicates that read receipts will be sent to the sender.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c9857-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9857-117">Remarks</span></span>

<span data-ttu-id="c9857-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c9857-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c9857-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c9857-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c9857-120">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c9857-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c9857-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="c9857-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c9857-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c9857-122">Schema name</span></span>  <br/> |<span data-ttu-id="c9857-123">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="c9857-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c9857-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c9857-124">Validation file</span></span>  <br/> |<span data-ttu-id="c9857-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="c9857-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c9857-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="c9857-126">Can be empty</span></span>  <br/> ||
   

