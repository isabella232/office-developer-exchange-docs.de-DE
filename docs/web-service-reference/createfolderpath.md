---
title: CreateFolderPath
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 282576cb-a921-49f7-8748-64158fd50c41
description: Das CreateFolderPath-Element wird zum Erstellen eines Ordnerpfads verwendet und enthält eine übergeordnete Ordner-ID und einen relativen Ordnerpfad.
ms.openlocfilehash: e6ce6c9b6e12a6a0fb6792b63368a79c87d06f07
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457536"
---
# <a name="createfolderpath"></a><span data-ttu-id="3cf9e-103">CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="3cf9e-103">CreateFolderPath</span></span>

<span data-ttu-id="3cf9e-104">Das **CreateFolderPath** -Element wird zum Erstellen eines Ordnerpfads verwendet und enthält eine übergeordnete Ordner-ID und einen relativen Ordnerpfad.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-104">The **CreateFolderPath** element is used to create a folder path and includes a parent folder Id and a relative folder path.</span></span> 
  
```XML
<CreateFolderPath>
   <ParentFolderId/>
   <RelativeFolderPath/>
</CreateFolderPath>
```

 <span data-ttu-id="3cf9e-105">**CreateFolderPathType**</span><span class="sxs-lookup"><span data-stu-id="3cf9e-105">**CreateFolderPathType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3cf9e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3cf9e-106">Attributes and elements</span></span>

<span data-ttu-id="3cf9e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3cf9e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3cf9e-108">Attributes</span></span>

<span data-ttu-id="3cf9e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3cf9e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3cf9e-110">Child elements</span></span>

<span data-ttu-id="3cf9e-111">[Parentfolderid (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)  |  [RelativeFolderPath](relativefolderpath.md)</span><span class="sxs-lookup"><span data-stu-id="3cf9e-111">[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) | [RelativeFolderPath](relativefolderpath.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3cf9e-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3cf9e-112">Parent elements</span></span>

<span data-ttu-id="3cf9e-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3cf9e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3cf9e-114">Remarks</span></span>

<span data-ttu-id="3cf9e-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3cf9e-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3cf9e-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3cf9e-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3cf9e-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3cf9e-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="3cf9e-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3cf9e-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3cf9e-119">Schema name</span></span>  <br/> |<span data-ttu-id="3cf9e-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="3cf9e-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3cf9e-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3cf9e-121">Validation file</span></span>  <br/> |<span data-ttu-id="3cf9e-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="3cf9e-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3cf9e-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="3cf9e-123">Can be empty</span></span>  <br/> |<span data-ttu-id="3cf9e-124">false</span><span class="sxs-lookup"><span data-stu-id="3cf9e-124">false</span></span>  <br/> |
   

