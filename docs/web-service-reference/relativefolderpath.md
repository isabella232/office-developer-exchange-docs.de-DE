---
title: RelativeFolderPath
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 54e3ba52-08a6-4d48-8a44-6fd5fdbffb25
description: Das RelativeFolderPath-Element enthält ein Array von Ordnern, die angeben, den relativen Ordnerpfad des Ordnerpfads erstellt werden soll.
ms.openlocfilehash: f568d282e47a41c0aaf6d70ef383e5ef3e2b54bf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831051"
---
# <a name="relativefolderpath"></a><span data-ttu-id="f1b94-103">RelativeFolderPath</span><span class="sxs-lookup"><span data-stu-id="f1b94-103">RelativeFolderPath</span></span>

<span data-ttu-id="f1b94-104">Das **RelativeFolderPath** -Element enthält ein Array von Ordnern, die angeben, den relativen Ordnerpfad des Ordnerpfads erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1b94-104">The **RelativeFolderPath** element contains an array of folders that indicate the relative folder path of the folder path to be created.</span></span> 
  
```XML
<RelativeFolderPath>
   <Folder/>
   <CalendarFolder/>
   <ContactsFolder/>
   <SearchFolder/>
   <TasksFolder/>
</RelativeFolderPath>
```

 <span data-ttu-id="f1b94-105">**NonEmptyArrayOfFoldersType**</span><span class="sxs-lookup"><span data-stu-id="f1b94-105">**NonEmptyArrayOfFoldersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f1b94-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f1b94-106">Attributes and elements</span></span>

<span data-ttu-id="f1b94-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f1b94-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f1b94-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f1b94-108">Attributes</span></span>

<span data-ttu-id="f1b94-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f1b94-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f1b94-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f1b94-110">Child elements</span></span>

<span data-ttu-id="f1b94-111">[Ordner](folder.md) | [CalendarFolder](calendarfolder.md) | [ContactsFolder](contactsfolder.md) | [SearchFolder](searchfolder.md) | [TasksFolder](tasksfolder.md)</span><span class="sxs-lookup"><span data-stu-id="f1b94-111">[Folder](folder.md) | [CalendarFolder](calendarfolder.md) | [ContactsFolder](contactsfolder.md) | [SearchFolder](searchfolder.md) | [TasksFolder](tasksfolder.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f1b94-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f1b94-112">Parent elements</span></span>

[<span data-ttu-id="f1b94-113">CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="f1b94-113">CreateFolderPath</span></span>](createfolderpath.md)
  
## <a name="remarks"></a><span data-ttu-id="f1b94-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f1b94-114">Remarks</span></span>

<span data-ttu-id="f1b94-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f1b94-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f1b94-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f1b94-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f1b94-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f1b94-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f1b94-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="f1b94-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f1b94-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f1b94-119">Schema name</span></span>  <br/> |<span data-ttu-id="f1b94-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="f1b94-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f1b94-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f1b94-121">Validation file</span></span>  <br/> |<span data-ttu-id="f1b94-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f1b94-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f1b94-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f1b94-123">Can be empty</span></span>  <br/> ||
   

