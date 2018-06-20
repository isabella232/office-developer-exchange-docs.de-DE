---
title: ArchiveItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c2172e61-876a-4f76-bc9c-263c8be11429
description: Das ArchiveItem-Element enthält die Id des Quellordners und ein Array der Element-Ids für das Archivelement zugeordnete.
ms.openlocfilehash: 7f2d79f5a9e6798fafcf64e8b1bb680390800992
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757372"
---
# <a name="archiveitem"></a><span data-ttu-id="50dfa-103">ArchiveItem</span><span class="sxs-lookup"><span data-stu-id="50dfa-103">ArchiveItem</span></span>

<span data-ttu-id="50dfa-104">Das **ArchiveItem** -Element enthält die Id des Quellordners und ein Array der Element-Ids für das Archivelement zugeordnete.</span><span class="sxs-lookup"><span data-stu-id="50dfa-104">The **ArchiveItem** element contains the source folder Id and an array of item Ids for the associated archive item.</span></span> 
  
```XML
<ArchiveItem>
   <ArchiveSourceFolderId/>
   <ItemIds/>
</ArchiveItem>
```

 <span data-ttu-id="50dfa-105">**ArchiveItemType**</span><span class="sxs-lookup"><span data-stu-id="50dfa-105">**ArchiveItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="50dfa-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="50dfa-106">Attributes and elements</span></span>

<span data-ttu-id="50dfa-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="50dfa-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="50dfa-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="50dfa-108">Attributes</span></span>

<span data-ttu-id="50dfa-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="50dfa-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="50dfa-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="50dfa-110">Child elements</span></span>

<span data-ttu-id="50dfa-111">[ArchiveSourceFolderId](archivesourcefolderid.md) | [Artikelnummern ein.](itemids.md)</span><span class="sxs-lookup"><span data-stu-id="50dfa-111">[ArchiveSourceFolderId](archivesourcefolderid.md) | [ItemIds](itemids.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="50dfa-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="50dfa-112">Parent elements</span></span>

<span data-ttu-id="50dfa-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="50dfa-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="50dfa-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="50dfa-114">Remarks</span></span>

<span data-ttu-id="50dfa-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="50dfa-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="50dfa-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="50dfa-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="50dfa-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="50dfa-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="50dfa-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="50dfa-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="50dfa-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="50dfa-119">Schema name</span></span>  <br/> |<span data-ttu-id="50dfa-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="50dfa-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="50dfa-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="50dfa-121">Validation file</span></span>  <br/> |<span data-ttu-id="50dfa-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="50dfa-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="50dfa-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="50dfa-123">Can be empty</span></span>  <br/> |<span data-ttu-id="50dfa-124">false</span><span class="sxs-lookup"><span data-stu-id="50dfa-124">false</span></span>  <br/> |
   

