---
title: RelativeFolderPath
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 54e3ba52-08a6-4d48-8a44-6fd5fdbffb25
description: Das RelativeFolderPath-Element enthält ein Array von Ordnern, die den relativen Ordnerpfad des zu erstellenden Ordnerpfads angeben.
ms.openlocfilehash: 8a0fc0020943afdbe6cd4c79d51d61337f8dd329
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457158"
---
# <a name="relativefolderpath"></a><span data-ttu-id="210c2-103">RelativeFolderPath</span><span class="sxs-lookup"><span data-stu-id="210c2-103">RelativeFolderPath</span></span>

<span data-ttu-id="210c2-104">Das **RelativeFolderPath** -Element enthält ein Array von Ordnern, die den relativen Ordnerpfad des zu erstellenden Ordnerpfads angeben.</span><span class="sxs-lookup"><span data-stu-id="210c2-104">The **RelativeFolderPath** element contains an array of folders that indicate the relative folder path of the folder path to be created.</span></span> 
  
```XML
<RelativeFolderPath>
   <Folder/>
   <CalendarFolder/>
   <ContactsFolder/>
   <SearchFolder/>
   <TasksFolder/>
</RelativeFolderPath>
```

 <span data-ttu-id="210c2-105">**NonEmptyArrayOfFoldersType**</span><span class="sxs-lookup"><span data-stu-id="210c2-105">**NonEmptyArrayOfFoldersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="210c2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="210c2-106">Attributes and elements</span></span>

<span data-ttu-id="210c2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="210c2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="210c2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="210c2-108">Attributes</span></span>

<span data-ttu-id="210c2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="210c2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="210c2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="210c2-110">Child elements</span></span>

<span data-ttu-id="210c2-111">[Ordner](folder.md)  |  [CalendarFolder](calendarfolder.md)  |  [ContactsFolder](contactsfolder.md)  |  [SearchFolder](searchfolder.md)  |  [TasksFolder](tasksfolder.md)</span><span class="sxs-lookup"><span data-stu-id="210c2-111">[Folder](folder.md) | [CalendarFolder](calendarfolder.md) | [ContactsFolder](contactsfolder.md) | [SearchFolder](searchfolder.md) | [TasksFolder](tasksfolder.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="210c2-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="210c2-112">Parent elements</span></span>

[<span data-ttu-id="210c2-113">CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="210c2-113">CreateFolderPath</span></span>](createfolderpath.md)
  
## <a name="remarks"></a><span data-ttu-id="210c2-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="210c2-114">Remarks</span></span>

<span data-ttu-id="210c2-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="210c2-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="210c2-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="210c2-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="210c2-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="210c2-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="210c2-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="210c2-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="210c2-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="210c2-119">Schema name</span></span>  <br/> |<span data-ttu-id="210c2-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="210c2-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="210c2-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="210c2-121">Validation file</span></span>  <br/> |<span data-ttu-id="210c2-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="210c2-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="210c2-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="210c2-123">Can be empty</span></span>  <br/> ||
   

