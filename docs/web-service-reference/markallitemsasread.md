---
title: MarkAllItemsAsRead
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22244afb-99ec-41b4-8f73-3fbccd56d1ab
description: Das MarkAllItemsAsRead-Element enthält die Anforderung an alle Elemente in einem Ordner als gelesen markiert.
ms.openlocfilehash: 9d7eb8eb7194cb5d77e909dc08abfb70e2385d56
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830346"
---
# <a name="markallitemsasread"></a><span data-ttu-id="b6437-103">MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="b6437-103">MarkAllItemsAsRead</span></span>

<span data-ttu-id="b6437-104">Das **MarkAllItemsAsRead** -Element enthält die Anforderung an alle Elemente in einem Ordner als gelesen markiert.</span><span class="sxs-lookup"><span data-stu-id="b6437-104">The **MarkAllItemsAsRead** element contains the request to mark all the items in a folder as read.</span></span> 
  
```XML
<MarkAllItemsAsRead>
   <ReadFlag/>
   <SuppressReadReceipts/>
   <FolderIds/>
</MarkAllItemsAsRead>
```

 <span data-ttu-id="b6437-105">**MarkAllItemsAsReadType**</span><span class="sxs-lookup"><span data-stu-id="b6437-105">**MarkAllItemsAsReadType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b6437-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b6437-106">Attributes and elements</span></span>

<span data-ttu-id="b6437-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b6437-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b6437-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b6437-108">Attributes</span></span>

<span data-ttu-id="b6437-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b6437-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b6437-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b6437-110">Child elements</span></span>

<span data-ttu-id="b6437-111">[ReadFlag](readflag.md) | [SuppressReadReceipts](suppressreadreceipts.md) | [FolderIds](folderids.md)</span><span class="sxs-lookup"><span data-stu-id="b6437-111">[ReadFlag](readflag.md) | [SuppressReadReceipts](suppressreadreceipts.md) | [FolderIds](folderids.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b6437-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b6437-112">Parent elements</span></span>

<span data-ttu-id="b6437-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="b6437-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b6437-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b6437-114">Remarks</span></span>

<span data-ttu-id="b6437-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b6437-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b6437-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b6437-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b6437-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b6437-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b6437-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="b6437-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b6437-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b6437-119">Schema name</span></span>  <br/> |<span data-ttu-id="b6437-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="b6437-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b6437-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b6437-121">Validation file</span></span>  <br/> |<span data-ttu-id="b6437-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b6437-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b6437-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b6437-123">Can be empty</span></span>  <br/> ||
   

