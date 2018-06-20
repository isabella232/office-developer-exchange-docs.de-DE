---
title: CreateFolderPath
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 282576cb-a921-49f7-8748-64158fd50c41
description: Das CreateFolderPath-Element wird verwendet, um ein Ordnerpfad erstellen und umfasst eine Id des übergeordneten Ordners und einer relativen Ordnerpfad.
ms.openlocfilehash: bfe31d894cfaa0f36da2d1d0045f723e0d261759
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757759"
---
# <a name="createfolderpath"></a><span data-ttu-id="8bbe2-103">CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="8bbe2-103">CreateFolderPath</span></span>

<span data-ttu-id="8bbe2-104">Das **CreateFolderPath** -Element wird verwendet, um ein Ordnerpfad erstellen und umfasst eine Id des übergeordneten Ordners und einer relativen Ordnerpfad.</span><span class="sxs-lookup"><span data-stu-id="8bbe2-104">The **CreateFolderPath** element is used to create a folder path and includes a parent folder Id and a relative folder path.</span></span> 
  
```XML
<CreateFolderPath>
   <ParentFolderId/>
   <RelativeFolderPath/>
</CreateFolderPath>
```

 <span data-ttu-id="8bbe2-105">**CreateFolderPathType**</span><span class="sxs-lookup"><span data-stu-id="8bbe2-105">**CreateFolderPathType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8bbe2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8bbe2-106">Attributes and elements</span></span>

<span data-ttu-id="8bbe2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8bbe2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8bbe2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8bbe2-108">Attributes</span></span>

<span data-ttu-id="8bbe2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="8bbe2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8bbe2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8bbe2-110">Child elements</span></span>

<span data-ttu-id="8bbe2-111">[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) | [RelativeFolderPath](relativefolderpath.md)</span><span class="sxs-lookup"><span data-stu-id="8bbe2-111">[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) | [RelativeFolderPath](relativefolderpath.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8bbe2-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8bbe2-112">Parent elements</span></span>

<span data-ttu-id="8bbe2-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="8bbe2-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8bbe2-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8bbe2-114">Remarks</span></span>

<span data-ttu-id="8bbe2-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8bbe2-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8bbe2-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="8bbe2-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8bbe2-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8bbe2-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8bbe2-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="8bbe2-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8bbe2-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8bbe2-119">Schema name</span></span>  <br/> |<span data-ttu-id="8bbe2-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="8bbe2-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8bbe2-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8bbe2-121">Validation file</span></span>  <br/> |<span data-ttu-id="8bbe2-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8bbe2-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8bbe2-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="8bbe2-123">Can be empty</span></span>  <br/> |<span data-ttu-id="8bbe2-124">false</span><span class="sxs-lookup"><span data-stu-id="8bbe2-124">false</span></span>  <br/> |
   

