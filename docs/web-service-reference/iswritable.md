---
title: IsWritable
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d4af8eee-7001-4a8e-b9bd-d14882f2406b
description: Das IsWritable-Element gibt an, ob die zugrunde liegende Kontakt oder eine Active Directory-Empfänger geschrieben werden kann.
ms.openlocfilehash: 03f258d01ecfc12dfa4e09ac88f4a75340d2acf3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830158"
---
# <a name="iswritable"></a><span data-ttu-id="1a3db-103">IsWritable</span><span class="sxs-lookup"><span data-stu-id="1a3db-103">IsWritable</span></span>

<span data-ttu-id="1a3db-104">Das **IsWritable** -Element gibt an, ob die zugrunde liegende Kontakt oder eine Active Directory-Empfänger geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="1a3db-104">The **IsWritable** element specifies whether the underlying contact or Active Directory recipient can be written to.</span></span> 
  
```XML
<IsWritable> true | false </IsWritable>
```

 <span data-ttu-id="1a3db-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="1a3db-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1a3db-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1a3db-106">Attributes and elements</span></span>

<span data-ttu-id="1a3db-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1a3db-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1a3db-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1a3db-108">Attributes</span></span>

<span data-ttu-id="1a3db-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1a3db-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1a3db-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1a3db-110">Child elements</span></span>

<span data-ttu-id="1a3db-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="1a3db-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1a3db-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1a3db-112">Parent elements</span></span>

[<span data-ttu-id="1a3db-113">Zuweisung (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="1a3db-113">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
  
## <a name="text-value"></a><span data-ttu-id="1a3db-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="1a3db-114">Text value</span></span>

<span data-ttu-id="1a3db-115">Der Textwert **true** für das **IsWritable** -Element gibt an, dass der Kontakt oder die Active Directory-Objekt für den Schreibzugriff verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="1a3db-115">A text value of **true** for the **IsWritable** element indicates that the contact or Active Directory object is available for write access.</span></span> <span data-ttu-id="1a3db-116">Der Wert **false** gibt an, dass der Kontakt oder die Active Directory-Objekt nicht für den Schreibzugriff verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="1a3db-116">A value of **false** indicates that the contact or Active Directory object is not available for write access.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1a3db-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1a3db-117">Remarks</span></span>

<span data-ttu-id="1a3db-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1a3db-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1a3db-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1a3db-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  

