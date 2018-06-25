---
title: ReadFlag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9d91aa89-9f9f-4877-846d-aaf48bbeec7c
description: Das ReadFlag-Element gibt den Zustand "gelesen", um für Elemente in einem Ordner festzulegen.
ms.openlocfilehash: f3156a51fbdd3372dd28f2065499d26a50b3d497
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830954"
---
# <a name="readflag"></a><span data-ttu-id="60ab3-103">ReadFlag</span><span class="sxs-lookup"><span data-stu-id="60ab3-103">ReadFlag</span></span>

<span data-ttu-id="60ab3-104">Das **ReadFlag** -Element gibt den Zustand "gelesen", um für Elemente in einem Ordner festzulegen.</span><span class="sxs-lookup"><span data-stu-id="60ab3-104">The **ReadFlag** element indicates the read state to set on items in a folder.</span></span> 
  
```XML
<ReadFlag>true | false</ReadFlag>
```

 <span data-ttu-id="60ab3-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="60ab3-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="60ab3-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="60ab3-106">Attributes and elements</span></span>

<span data-ttu-id="60ab3-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="60ab3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="60ab3-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="60ab3-108">Attributes</span></span>

<span data-ttu-id="60ab3-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="60ab3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="60ab3-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="60ab3-110">Child elements</span></span>

<span data-ttu-id="60ab3-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="60ab3-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="60ab3-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="60ab3-112">Parent elements</span></span>

[<span data-ttu-id="60ab3-113">MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="60ab3-113">MarkAllItemsAsRead</span></span>](markallitemsasread.md)
  
## <a name="text-value"></a><span data-ttu-id="60ab3-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="60ab3-114">Text value</span></span>

<span data-ttu-id="60ab3-115">Der Textwert **true** für das **ReadFlag** -Element gibt an, dass die Elemente im Ordner als gelesen markiert werden.</span><span class="sxs-lookup"><span data-stu-id="60ab3-115">A text value of **true** for the **ReadFlag** element indicates that the items in the folder will be marked as read.</span></span> <span data-ttu-id="60ab3-116">Der Wert **"false"** gibt an, dass die Elemente im Ordner markiert werden als ungelesen.</span><span class="sxs-lookup"><span data-stu-id="60ab3-116">A value of **false** indicates that the items in the folder will be marked as unread.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="60ab3-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="60ab3-117">Remarks</span></span>

<span data-ttu-id="60ab3-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="60ab3-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="60ab3-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="60ab3-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="60ab3-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="60ab3-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="60ab3-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="60ab3-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="60ab3-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="60ab3-122">Schema name</span></span>  <br/> |<span data-ttu-id="60ab3-123">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="60ab3-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="60ab3-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="60ab3-124">Validation file</span></span>  <br/> |<span data-ttu-id="60ab3-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="60ab3-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="60ab3-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="60ab3-126">Can be empty</span></span>  <br/> ||
   

