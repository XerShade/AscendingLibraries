# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)
## Unreleased

## 0.9.0 (6. June, 2024)
### Changed
- (Breaking) Added Rendering layer to Text, Mesh.
- (Breaking) DrawOrder Width, Height and DrawType Removed. 
- (Breaking) DrawType Removed.
- (Breaking) Rename GpuBuffer as VertexBuffer.
- (Breaking) Bounds functions now use Vec2 instead of Vec3 since we do not use Z.
- (Breaking) Removed tex_buf from Text to reduce Ram usage.

### Fixed
- Ensure all renderers use Alpha checks and Rendering Layer for Ordering

### Added
- More Documentation.

## 0.8.2 (30. May, 2024)
### Fixed
- sRGB to Linear color within shader to give same or closer results to Paint and other editing programs that use RGB

## 0.8.1 (17. May, 2024)
### Fixed
- fixed Y ordering offsets.

## 0.8.0 (24. April, 2024)
### Changed
- (Breaking) updated to support winit 0.30.0.
- (Breaking) renderer update now takes &WindowEvent.

### Added
- Z axis angle Rotation and Flip to image.

## 0.7.0 (24. April, 2024)
### Changed
- (Breaking) system not supports a secondary manual Mat4x4 and Scale.
- (Breaking) use_camera is now set as camera_type and uses a enumeration which tells the shader how to use the camera's.
- (Breaking) projected_world_to_screen and world_to_screen now both use CameraType instead of scale.
- (Breaking) shaders were rewritten to allow multiple views and scales.

### Fixed
- rect not rendering correctly due to scale was always being applied even when view was not.


## 0.5.0 (24. April, 2024)
### Changed
- (Breaking)  BufferStore::new now expects sizes for vertex and indexs Vec

### Fixed
- Updated Rendering types to have persistant data to avoid recreation upon update, which avoids allocations.
