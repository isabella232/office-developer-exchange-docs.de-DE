---
title: FoldersToIgnore
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b5d18516-a617-4daf-8baf-c7ce29c76f6b
description: Das FoldersToIgnore-Element gibt eine Liste der Ordner, die beim Abrufen von Elementen in einer Unterhaltung ignoriert werden. Alle Unterhaltungselemente in den Ordnern ignorierten werden nicht in einer Antwort GetConversationItems zurückgegeben.
ms.openlocfilehash: 96c094996c601e685dc1c7e6b869a790ce7d74a1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758522"
---
# <a name="folderstoignore"></a><span data-ttu-id="ac63c-104">FoldersToIgnore</span><span class="sxs-lookup"><span data-stu-id="ac63c-104">FoldersToIgnore</span></span>

<span data-ttu-id="ac63c-105">Das **FoldersToIgnore** -Element gibt eine Liste der Ordner, die beim Abrufen von Elementen in einer Unterhaltung ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="ac63c-105">The **FoldersToIgnore** element identifies a list of folders that are ignored when getting items in a conversation.</span></span> <span data-ttu-id="ac63c-106">Alle Unterhaltungselemente in den Ordnern ignorierten werden nicht in einer Antwort **GetConversationItems** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ac63c-106">All conversation items in the ignored folders are not returned in a **GetConversationItems** response.</span></span> 
  
```XML
<FoldersToIgnore>
   <FolderId/>
   <DistinguishedFolderId/>
</FoldersToIgnore>
```

 <span data-ttu-id="ac63c-107">**NonEmptyArrayOfBaseFolderIdsType**</span><span class="sxs-lookup"><span data-stu-id="ac63c-107">**NonEmptyArrayOfBaseFolderIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ac63c-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ac63c-108">Attributes and elements</span></span>

<span data-ttu-id="ac63c-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ac63c-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ac63c-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="ac63c-110">Attributes</span></span>

<span data-ttu-id="ac63c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ac63c-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ac63c-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac63c-112">Child elements</span></span>

<span data-ttu-id="ac63c-113">[FolderId](folderid.md) | [DistinguishedFolderId](distinguishedfolderid.md)</span><span class="sxs-lookup"><span data-stu-id="ac63c-113">[FolderId](folderid.md) | [DistinguishedFolderId](distinguishedfolderid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ac63c-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac63c-114">Parent elements</span></span>

[<span data-ttu-id="ac63c-115">GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="ac63c-115">GetConversationItems</span></span>](getconversationitems.md)
  
## <a name="remarks"></a><span data-ttu-id="ac63c-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ac63c-116">Remarks</span></span>

<span data-ttu-id="ac63c-117">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ac63c-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ac63c-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ac63c-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ac63c-119">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ac63c-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ac63c-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac63c-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ac63c-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ac63c-121">Schema name</span></span>  <br/> |<span data-ttu-id="ac63c-122">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ac63c-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="ac63c-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ac63c-123">Validation file</span></span>  <br/> |<span data-ttu-id="ac63c-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ac63c-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ac63c-125">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="ac63c-125">Can be empty</span></span>  <br/> |<span data-ttu-id="ac63c-126">false</span><span class="sxs-lookup"><span data-stu-id="ac63c-126">false</span></span>  <br/> |
   

