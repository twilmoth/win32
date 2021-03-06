---
title: Sample(S,float,int,float,uint) function
description: Samples a Texture2D with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.
ms.assetid: 1B9F48C4-DDB9-4547-B4AF-81A3ADA44C3F
keywords:
- Sample function HLSL
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: article
ms.date: 05/31/2018
api_location: 
---

# Sample(S,float,int,float,uint) function

Samples a [**Texture2D**](sm5-object-texture2d.md) with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.

> [!Note]  
> Requires [shader model 5](d3d11-graphics-reference-sm5.md) or higher.

 

## Syntax

``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float Location,
  in  int Offset,
  in  float Clamp,
  out uint Status
);
```

## Parameters

<dl> <dt>

*S* \[in\]
</dt> <dd>

A [Sampler state](dx-graphics-hlsl-sampler.md). This is an object declared in an effect file that contains state assignments.

</dd> <dt>

*Location* \[in\]
</dt> <dd>

The texture coordinates. The argument type is dependent on the texture-object type.



| Texture-Object Type                    | Parameter Type |
|----------------------------------------|----------------|
| Texture1D                              | float          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

*Offset* \[in\]
</dt> <dd>

An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling. Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware. The argument type is dependent on the texture-object type. For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).



| Texture-Object Type           | Parameter Type |
|-------------------------------|----------------|
| Texture1D, Texture1DArray     | int            |
| Texture2D, Texture2DArray     | int2           |
| Texture3D                     | int3           |
| TextureCube, TextureCubeArray | not supported  |



 

</dd> <dt>

*Clamp* \[in\]
</dt> <dd>

An optional value to clamp sample LOD values to. For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.

</dd> <dt>

*Status* \[out\]
</dt> <dd>

The status of the operation. You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function. **CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](https://docs.microsoft.com/windows/desktop/direct3d11/direct3d-11-2-features). If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.

</dd> </dl>

## Return value

The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](https://docs.microsoft.com/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## Remarks

Texture sampling uses the texel position to look up a texel value. An offset can be applied to the position before lookup. The sampler state contains the sampling and filtering options. This method can be invoked within a pixel shader, but it is not supported in a vertex shader or a geometry shader.

### Calculating Texel Positions

Texture coordinates are floating-point values that reference texture data, which is also known as normalized texture space. Address wrapping modes are applied in this order (texture coordinates + offsets + wrap mode) to modify texture coordinates outside the \[0...1\] range.

For texture arrays, an additional value in the location parameter specifies an index into a texture array. This index is treated as a scaled float value (instead of the normalized space for standard texture coordinates). The conversion to an integer index is done in the following order (float + round-to-nearest-even integer + clamp to the array range).

### Applying Texture Coordinate Offsets

The offset parameter modifies the texture coordinates, in texel space. Even though texture coordinates are normalized floating-point numbers, the offset applies an integer offset.

The data format returned is determined by the texture format. For example, if the texture resource was defined with the DXGI\_FORMAT\_A8B8G8R8\_UNORM\_SRGB format, the sampling operation converts sampled texels from gamma 2.0 to 1.0, filter, and writes the result as a floating-point value in the range \[0..1\].

## See also

<dl> <dt>

[Sample methods](texture-sample-overload.md)
</dt> <dt>

[Texture-Object](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 




