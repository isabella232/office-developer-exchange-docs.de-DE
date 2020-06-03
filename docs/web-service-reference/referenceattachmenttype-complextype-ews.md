---
title: ReferenceAttachmentType complexType (EWS)
manager: sethgros
ms.date: 03/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 18bfa012-e903-d7f3-528a-31ccceb65463
ms.openlocfilehash: 24f5a62eadd490b5b0000dfe048850c44540f266
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528734"
---
# <a name="referenceattachmenttype-complextype-ews"></a><span data-ttu-id="1356c-102">ReferenceAttachmentType complexType (EWS)</span><span class="sxs-lookup"><span data-stu-id="1356c-102">ReferenceAttachmentType complexType (EWS)</span></span>

## <a name="type-information"></a><span data-ttu-id="1356c-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="1356c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1356c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1356c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1356c-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="1356c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1356c-106">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="1356c-106">types.xsd</span></span>  <br/> |
|<span data-ttu-id="1356c-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="1356c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1356c-108">t:AttachmentType</span><span class="sxs-lookup"><span data-stu-id="1356c-108">t:AttachmentType</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1356c-109">Definition</span><span class="sxs-lookup"><span data-stu-id="1356c-109">Definition</span></span>

```XML
<xs:complexType name="ReferenceAttachmentType">
    <xs:complexContent>
        <xs:extension base="t:AttachmentType">
            <xs:sequence>
                <xs:element name="AttachLongPathName" type="xs:string" maxOccurs="1" minOccurs="0"></xs:element>
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="1356c-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="1356c-110">Elements and attributes</span></span>

<span data-ttu-id="1356c-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="1356c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1356c-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1356c-112">Child elements</span></span>

|<span data-ttu-id="1356c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1356c-113">**Element**</span></span>|<span data-ttu-id="1356c-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1356c-114">**Type**</span></span>|<span data-ttu-id="1356c-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1356c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1356c-116">AttachLongPathName</span><span class="sxs-lookup"><span data-stu-id="1356c-116">AttachLongPathName</span></span>](attachlongpathname.md) <br/> |<span data-ttu-id="1356c-117">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1356c-117">xs:string</span></span>  <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1356c-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="1356c-118">Attributes</span></span>

<span data-ttu-id="1356c-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="1356c-119">None.</span></span>
  

