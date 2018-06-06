---
title: VML ImageSize Attribute
description: VML ImageSize Attribute
ms.assetid: 6b021ac1-e447-46ad-9153-91f936fca0d8
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# VML ImageSize Attribute

This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9. Webpages and applications that rely on VML should be [migrated to SVG](http://go.microsoft.com/fwlink/p/?LinkID=236964) or other widely supported standards.

> [!Note]  
> As of December 2011, this topic has been archived. As a result, it is no longer actively maintained. For more information, see [Archived Content](https://msdn.microsoft.com/library/hh772377). For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](http://go.microsoft.com/fwlink/p/?linkid=204313).

 

Defines the size of the image for the stroke. Read/write. **VgVector2D**.

**Applies To**

[Stroke](msdn-online-vml-stroke-element.md)

**Tag Syntax**

&lt;v: *element* imagesize=" *expression* "&gt;

**Script Syntax**

*element* .imagesize="*expression*"

*expression*=*element*.imagesize

**Remarks**

Default is the size of the image.

*VML Standard Attribute*

**Example**

The stroke image will be a 10-by-10 point size.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imagesize="10pt,10pt"/>
   </v:shape>
```



 

 



