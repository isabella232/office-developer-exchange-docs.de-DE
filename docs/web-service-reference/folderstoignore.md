---
title: FoldersToIgnore
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b5d18516-a617-4daf-8baf-c7ce29c76f6b
description: Das FoldersToIgnore-Element identifiziert eine Liste von Ordnern, die ignoriert werden, wenn Elemente in einer Unterhaltung abgerufen werden. Alle Unterhaltungselemente in den ignorierten Ordnern werden nicht in einer GetConversationItems-Antwort zurückgegeben.
ms.openlocfilehash: 07813a54a9a3afa3de23ae94f1c9b191d1cb6fac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44453357"
---
# <a name="folderstoignore"></a><span data-ttu-id="58d11-104">FoldersToIgnore</span><span class="sxs-lookup"><span data-stu-id="58d11-104">FoldersToIgnore</span></span>

<span data-ttu-id="58d11-105">Das **FoldersToIgnore** -Element identifiziert eine Liste von Ordnern, die ignoriert werden, wenn Elemente in einer Unterhaltung abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="58d11-105">The **FoldersToIgnore** element identifies a list of folders that are ignored when getting items in a conversation.</span></span> <span data-ttu-id="58d11-106">Alle Unterhaltungselemente in den ignorierten Ordnern werden nicht in einer **GetConversationItems** -Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="58d11-106">All conversation items in the ignored folders are not returned in a **GetConversationItems** response.</span></span> 
  
```XML
<FoldersToIgnore>
   <FolderId/>
   <DistinguishedFolderId/>
</FoldersToIgnore>
```

 <span data-ttu-id="58d11-107">**NonEmptyArrayOfBaseFolderIdsType**</span><span class="sxs-lookup"><span data-stu-id="58d11-107">**NonEmptyArrayOfBaseFolderIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="58d11-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="58d11-108">Attributes and elements</span></span>

<span data-ttu-id="58d11-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="58d11-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="58d11-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="58d11-110">Attributes</span></span>

<span data-ttu-id="58d11-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="58d11-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="58d11-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="58d11-112">Child elements</span></span>

<span data-ttu-id="58d11-113">[Ordner-Nr](folderid.md)  |  [DistinguishedFolderId](distinguishedfolderid.md)</span><span class="sxs-lookup"><span data-stu-id="58d11-113">[FolderId](folderid.md) | [DistinguishedFolderId](distinguishedfolderid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="58d11-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="58d11-114">Parent elements</span></span>

[<span data-ttu-id="58d11-115">GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="58d11-115">GetConversationItems</span></span>](getconversationitems.md)
  
## <a name="remarks"></a><span data-ttu-id="58d11-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58d11-116">Remarks</span></span>

<span data-ttu-id="58d11-117">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="58d11-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="58d11-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="58d11-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="58d11-119">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="58d11-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="58d11-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="58d11-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="58d11-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="58d11-121">Schema name</span></span>  <br/> |<span data-ttu-id="58d11-122">Schematypen</span><span class="sxs-lookup"><span data-stu-id="58d11-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="58d11-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="58d11-123">Validation file</span></span>  <br/> |<span data-ttu-id="58d11-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="58d11-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="58d11-125">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="58d11-125">Can be empty</span></span>  <br/> |<span data-ttu-id="58d11-126">False</span><span class="sxs-lookup"><span data-stu-id="58d11-126">false</span></span>  <br/> |
   

