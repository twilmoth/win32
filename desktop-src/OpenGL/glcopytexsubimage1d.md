---
title: glCopyTexSubImage1D function
description: The glCopyTexSubImage1D function copies a sub-image of a one-dimensional texture image from the framebuffer.
ms.assetid: 718aee8a-6dce-49e1-a441-19beccd89f8d
keywords:
- glCopyTexSubImage1D function OpenGL
topic_type:
- apiref
api_name:
- glCopyTexSubImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: article
ms.date: 05/31/2018
---

# glCopyTexSubImage1D function

The **glCopyTexSubImage1D** function copies a sub-image of a one-dimensional texture image from the framebuffer.

## Syntax


```C++
void WINAPI glCopyTexSubImage1D(
   GLenum  target,
   GLint   level,
   GLint   xoffset,
   GLint   x,
   GLint   y,
   GLsizei width
);
```



## Parameters

<dl> <dt>

*target* 
</dt> <dd>

The target to which the image data will be changed. Must have the value GL\_TEXTURE\_1D.

</dd> <dt>

*level* 
</dt> <dd>

The level-of-detail number. Level 0 is the base image. Level *n* is the *n*th mipmap reduction image.

</dd> <dt>

*xoffset* 
</dt> <dd>

The texel offset within the texture array.

</dd> <dt>

*x* 
</dt> <dd>

The window x-plane coordinate of the lower-left corner of the row of pixels to be copied.

</dd> <dt>

*y* 
</dt> <dd>

The window y-plane coordinate of the lower-left corner of the row of pixels to be copied.

</dd> <dt>

*width* 
</dt> <dd>

The width of the sub-image of the texture image. Specifying a texture sub-image with zero width has no effect.

</dd> </dl>

## Return value

This function does not return a value.

## Error codes

The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.



| Name                                                                                                  | Meaning                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL\_INVALID\_ENUM**</dt> </dl>      | *target* was not an accepted value.<br/>                                                                                                                                                                               |
| <dl> <dt>**GL\_INVALID\_VALUE**</dt> </dl>     | *level* was less than zero or *level* is greater than *log*2(*max*), where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.<br/>                                                                                 |
| <dl> <dt>**GL\_INVALID\_VALUE**</dt> </dl>     | *xoffset* was less than *border* or (*xoffset* + *width*)was greater than (*w* + *border*), where *w* is GL\_TEXTURE\_WIDTH and *border* is GL\_TEXTURE\_BORDER. Note that *w* includes twice the *border* width.<br/> |
| <dl> <dt>**GL\_INVALID\_VALUE**</dt> </dl>     | *width* was less than *border* or *y* was less than *border*, where *border* is the border width of the texture array.<br/>                                                                                            |
| <dl> <dt>**GL\_INVALID\_OPERATION**</dt> </dl> | The texture array was not defined by a previous [**glTexImage1D**](glteximage1d.md) operation.<br/>                                                                                                                   |
| <dl> <dt>**GL\_INVALID\_OPERATION**</dt> </dl> | The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).<br/>                                                                                        |



## Error codes

The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.



| Name                                                                                                  | Meaning                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL\_INVALID\_ENUM**</dt> </dl>      | *target* was not an accepted value.<br/>                                                                                                                                                                               |
| <dl> <dt>**GL\_INVALID\_VALUE**</dt> </dl>     | *level* was less than zero or *level* is greater than *log*2(*max*), where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.<br/>                                                                                 |
| <dl> <dt>**GL\_INVALID\_VALUE**</dt> </dl>     | *xoffset* was less than *border* or (*xoffset* + *width*)was greater than (*w* + *border*), where *w* is GL\_TEXTURE\_WIDTH and *border* is GL\_TEXTURE\_BORDER. Note that *w* includes twice the *border* width.<br/> |
| <dl> <dt>**GL\_INVALID\_VALUE**</dt> </dl>     | *width* was less than *border* or *y* was less than *border*, where *border* is the border width of the texture array.<br/>                                                                                            |
| <dl> <dt>**GL\_INVALID\_OPERATION**</dt> </dl> | The texture array was not defined by a previous [**glTexImage1D**](glteximage1d.md) operation.<br/>                                                                                                                   |
| <dl> <dt>**GL\_INVALID\_OPERATION**</dt> </dl> | The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).<br/>                                                                                        |



## Remarks

The **glCopyTexSubImage1D** function replaces a portion of a one-dimensional texture image using pixels from the current framebuffer, rather than from main memory as is the case for [**glTexSubImage1D**](gltexsubimage1d.md).

A row of pixels beginning with the window coordinates specified by *x* and *y* and with the length *width* replaces the portion of the texture array with the indexes *xoffset* through *xoffset* + (*width* - 1). The destination in the texture array cannot include any texels outside the originally specified texture array.

The **glCopyTexSubImage1D** function processes the pixels in a row in the same way as [**glCopyPixels**](glcopypixels.md) except that before the final conversion of the pixels, all pixel component values are clamped to the range \[0,1\] and converted to the texture's internal format for storage in the texture array. Pixel ordering is determined with lower *x* coordinates corresponding to lower texture coordinates. If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.

No change is made to the *internalFormat*, *width*, or *border* parameter of the specified texture array or to texel values outside the specified texture sub-image.

You cannot include calls to **glCopyTexSubImage1D** in display lists.

> [!Note]  
> The **glCopyTexSubImage1D** function is only available in OpenGL version 1.1 or later.

 

Texturing has no effect in color-index mode. The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) functions affect texture images in exactly the way they affect the way pixels are drawn using [**glDrawPixels**](gldrawpixels.md).

The following functions retrieve information related to **glCopyTexSubImage1D**:

[**glGetTexImage**](glgetteximage.md)

[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_1D

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 2000 Professional \[desktop apps only\]<br/>                              |
| Minimum supported server<br/> | Windows 2000 Server \[desktop apps only\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Library<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## See also

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glCopyTexSubImage2D**](glcopytexsubimage2d.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glFog**](glfog.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glTexEnv**](gltexenv-functions.md)
</dt> <dt>

[**glTexGen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





