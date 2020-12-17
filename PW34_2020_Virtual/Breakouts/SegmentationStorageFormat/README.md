# Segmentation storage format

In this breakout session we try to come up with a consensus on how to best store image segmentation that is convenient for many workflows and software tools

## Attendees
1. Andras Lasso (Queen's University)
1. Steve Pieper (Isomics)
1. Matt McCormick (Kitware)

## Current State

Commonly used formats:
- 3D image + colormap file: nrrd/nift and separate file in custom file format for storing segment names and color (3D Slicer, ITK-Snap, ...)
- 3D Slicer seg.nrrd file: standard nrrd with custom fields ([specification](https://github.com/Slicer/Slicer/blob/master/Libs/MRML/Core/vtkMRMLSegmentationStorageNode.h#L68-L102))
- DICOM segmentation object

## Needs

- Easy reading/writing in Python, C++, JavaScript
- Compatibility with 3D Slicer, ITK, DICOM, ...
- Web friendly (JSON)
- _add your needs here_

## Suggested solutions

- NRRD with single json object in a custom field
- Label JSON compatible with or using the [OME-NGFF `image-label` metadata](https://ngff.openmicroscopy.org/latest/#label-md)
- _add your suggestions here_