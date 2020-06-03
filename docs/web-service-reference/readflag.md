---
title: ReadFlag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9d91aa89-9f9f-4877-846d-aaf48bbeec7c
description: Das ReadFlag-Element gibt den Lesestatus an, der für Elemente in einem Ordner festgelegt werden soll.
ms.openlocfilehash: 1d3b9f3fe199ed2e63bdb632135120a5f89f4d1f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529896"
---
# <a name="readflag"></a><span data-ttu-id="f4685-103">ReadFlag</span><span class="sxs-lookup"><span data-stu-id="f4685-103">ReadFlag</span></span>

<span data-ttu-id="f4685-104">Das **ReadFlag** -Element gibt den Lesestatus an, der für Elemente in einem Ordner festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4685-104">The **ReadFlag** element indicates the read state to set on items in a folder.</span></span> 
  
```XML
<ReadFlag>true | false</ReadFlag>
```

 <span data-ttu-id="f4685-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="f4685-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f4685-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f4685-106">Attributes and elements</span></span>

<span data-ttu-id="f4685-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f4685-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f4685-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f4685-108">Attributes</span></span>

<span data-ttu-id="f4685-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f4685-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f4685-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f4685-110">Child elements</span></span>

<span data-ttu-id="f4685-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="f4685-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f4685-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f4685-112">Parent elements</span></span>

[<span data-ttu-id="f4685-113">MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="f4685-113">MarkAllItemsAsRead</span></span>](markallitemsasread.md)
  
## <a name="text-value"></a><span data-ttu-id="f4685-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="f4685-114">Text value</span></span>

<span data-ttu-id="f4685-115">Der Textwert **true** für das **ReadFlag** -Element gibt an, dass die Elemente im Ordner als gelesen markiert werden.</span><span class="sxs-lookup"><span data-stu-id="f4685-115">A text value of **true** for the **ReadFlag** element indicates that the items in the folder will be marked as read.</span></span> <span data-ttu-id="f4685-116">Der Wert **false** gibt an, dass die Elemente im Ordner als ungelesen gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="f4685-116">A value of **false** indicates that the items in the folder will be marked as unread.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f4685-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4685-117">Remarks</span></span>

<span data-ttu-id="f4685-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f4685-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f4685-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f4685-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f4685-120">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f4685-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f4685-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="f4685-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f4685-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f4685-122">Schema name</span></span>  <br/> |<span data-ttu-id="f4685-123">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="f4685-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f4685-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f4685-124">Validation file</span></span>  <br/> |<span data-ttu-id="f4685-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="f4685-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f4685-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f4685-126">Can be empty</span></span>  <br/> ||
   

