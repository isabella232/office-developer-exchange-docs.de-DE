---
title: MarkAllItemsAsRead
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22244afb-99ec-41b4-8f73-3fbccd56d1ab
description: Das MarkAllItemsAsRead-Element enthält die Anforderung zum Markieren aller Elemente in einem Ordner als gelesen.
ms.openlocfilehash: 0338b2a1eed503b7e8fb0ec8b4a8ebcf12b6dbd6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530888"
---
# <a name="markallitemsasread"></a><span data-ttu-id="b1d9a-103">MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="b1d9a-103">MarkAllItemsAsRead</span></span>

<span data-ttu-id="b1d9a-104">Das **MarkAllItemsAsRead** -Element enthält die Anforderung zum Markieren aller Elemente in einem Ordner als gelesen.</span><span class="sxs-lookup"><span data-stu-id="b1d9a-104">The **MarkAllItemsAsRead** element contains the request to mark all the items in a folder as read.</span></span> 
  
```XML
<MarkAllItemsAsRead>
   <ReadFlag/>
   <SuppressReadReceipts/>
   <FolderIds/>
</MarkAllItemsAsRead>
```

 <span data-ttu-id="b1d9a-105">**MarkAllItemsAsReadType**</span><span class="sxs-lookup"><span data-stu-id="b1d9a-105">**MarkAllItemsAsReadType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b1d9a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b1d9a-106">Attributes and elements</span></span>

<span data-ttu-id="b1d9a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b1d9a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b1d9a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b1d9a-108">Attributes</span></span>

<span data-ttu-id="b1d9a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b1d9a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b1d9a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b1d9a-110">Child elements</span></span>

<span data-ttu-id="b1d9a-111">[ReadFlag](readflag.md)  |  [SuppressReadReceipts](suppressreadreceipts.md)  |  [FolderIds](folderids.md)</span><span class="sxs-lookup"><span data-stu-id="b1d9a-111">[ReadFlag](readflag.md) | [SuppressReadReceipts](suppressreadreceipts.md) | [FolderIds](folderids.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b1d9a-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b1d9a-112">Parent elements</span></span>

<span data-ttu-id="b1d9a-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="b1d9a-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b1d9a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1d9a-114">Remarks</span></span>

<span data-ttu-id="b1d9a-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b1d9a-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b1d9a-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b1d9a-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b1d9a-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b1d9a-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b1d9a-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="b1d9a-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b1d9a-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b1d9a-119">Schema name</span></span>  <br/> |<span data-ttu-id="b1d9a-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="b1d9a-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b1d9a-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b1d9a-121">Validation file</span></span>  <br/> |<span data-ttu-id="b1d9a-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="b1d9a-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b1d9a-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b1d9a-123">Can be empty</span></span>  <br/> ||
   

