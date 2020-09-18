# Changelog

## [3.0.10] - 2020-03-06
### Fixed
- 1220091 SpriteShapeController leaks memory when zero control points are used
- 1216990 Colliders should also respect Pivot property of Edge Sprites.
- 1225366 Ensure SpriteShape are not generated when not in view on Runtime.

## [3.0.9] - 2020-02-11
### Changed
- Improved Memory Allocations.

### Fixed
- Fixed OnDrawGizmos to Get/Release RenderTexture through CommandBuffer.

## [3.0.8] - 2019-12-02
### Changed
- Updated License file
- Updated Third Party Notices file
- Changed how Samples are installed into user's project

### Fixed
- Fixed where the last point of the Sprite Shape does not behave correctly when using Continuous Points in a closed shape (case 1184721)

## [3.0.7] - 2019-10-27
### Fixed
- Added missing meta file

### Changed
- Update com.unity.2d.path package dependency

## [3.0.7] - 2019-10-27
### Fixed
- Added missing meta file

### Changed
- Update com.unity.2d.path package dependency

## [3.0.6] - 2019-09-27
### Added
- Added support to set CornerAngleThreshold.
- Burst is now enabled for performance boost.
### Fixed
- Fix (Case 1041062) Inputting Point Position manually causes mesh to not conform to the spline
- Fix GC in confirming Spline Extras sample.
- Fix hash Validation errors.
- Removed resources from Packages.

## [3.0.5] - 2019-09-05
### Fixed
- Fix (Case 1159767) Error generated when using a default sprite for Corner sprite or Angle Range sprite in Sprite Shape Profile
- Fix (Case 1178579) "ArgumentOutofRangeException" is thrown and SpriteShapeProfile freezes on reset

## [3.0.4] - 2019-08-09
### Added
- Added tangent channel support for proper 2D lighting in URP.

## [3.0.3] - 2019-07-24
### Added
- Add related test packages

## [3.0.2] - 2019-07-13
### Changed
- Update to latest Mathematics package version

## [3.0.1] - 2019-07-13
### Changed
- Mark package to support Unity 2019.3.0a10 onwards.

## [3.0.0] - 2019-06-19
### Changed
- Stable Version.
- Remove experimental namespace.

## [2.1.0-preview.8] - 2019-6-12
### Changed
- Fix (Case 1152342) The first point of the Sprite Shape does not behave correctly when using Continuous Points
- Fix (Case 1160009) Edge and Polygon Collider does not seem to follow the spriteshape for some broken mirrored tangent points
- Fix (Case 1157201) Edge Sprite Material changed when using a fill texture that is already an edge sprite on spriteshape
- Fix (Case 1162134) Open ended Spriteshape renders the fill texture instead of the range sprite

## [2.1.0-preview.7] - 2019-06-02
### Changed
- Fix Variant Selection.

## [2.1.0-preview.6] - 2019-06-02
### Changed
- Fix Null reference exception caused by SplineEditorCache changes.
- Fill Inspector changes due to Path integration.

## [2.1.0-preview.4] - 2019-05-28
### Changed
- Upgrade Mathematics package.
- Use path editor.

## [2.1.0-preview.2] - 2019-05-13
### Changed
- Initial version for 2019.2
- Update for common package.

## [2.0.0-preview.8] - 2019-05-16
### Fixed
- Fixed issue when sprites are re-ordered in Angle Range.
- Updated Samples.

## [2.0.0-preview.7] - 2019-05-10
### Fixed
- Version Update and fixes.

## [2.0.0-preview.6] - 2019-05-08
### Fixed
- Added Sprite Variant Selector.
- Fix Variant Bug (https://forum.unity.com/threads/spriteshape-preview-package.522575/page-6#post-4480936)
- Fix (Case 1146747) SpriteShape generating significant GC allocations every frame (OnWillRenderObject)

## [2.0.0-preview.5] - 2019-04-18
### Fixed
- Shape angle does not show the accurate sprite on certain parts of the shape.
- SpriteShape - Unable to use the Depth buffer (https://forum.unity.com/threads/spriteshape-preview-package.522575/page-6#post-4413142)

## [2.0.0-preview.4] - 2019-03-28
### Changed
- Disable burst for now until we have a final release.

## [2.0.0-preview.3] - 2019-03-25
### Fixed
- Update Common version.

## [2.0.0-preview.2] - 2019-03-08
### Fixed
- Fix Edge Case Scenario where Vertices along Continuous segment could be duplicated..
- Ensure that Collider uses a valid Sprite on Generation.

## [2.0.0-preview.1] - 2019-02-27
### Changed
- Updated version.

## [1.1.0-preview.1] - 2019-02-10
### Added
- Spriteshape tessellation code is re-implemented in C# Jobs and utilizes Burst for Performance.
- Added Mirrored and Non-Mirrored continous Tangent mode.
- Simplified Collider Generation support and is part of C# Job/Burst for performance.
- Added Shortcut Keys (for setting Tangentmode, Sprite Variant and Mirror Tangent).
- Ability to drag Spriteshape Profile form Project view to Hierarchy to create Sprite Shape in Scene.
- Simplified Corner mode for Points and is now enabled by default.
- Added Stretch UV support for Fill Area.
- Added Color property to SpriteShapeRenderer.

### Fixed
- SpriteShapeController shows wrong Sprites after deleting a sprite from the top angle range.
- Empty SpriteShapeController still seem to show the previous Spriteshape drawcalls
- Streched Sprites are generated in between non Linked Points
- Corners sprites are no longer usable if user only sets the corners for the bottom
- Sprites in SpriteShape still shows even after user deletes the SpriteShape Profile
- SpriteShape doesn't update Point Positions visually at runtime for Builds
- Spriteshape Colliders does not update in scene immediately
- Fixed constant Mesh baking (https://forum.unity.com/threads/spriteshape-preview-package.522575/page-4#post-3925789)
- Fixed Bounds generation issue (https://forum.unity.com/threads/spriteshape-preview-package.522575/page-5#post-4079857)
- Sprite Shape Profile component breaks when creating range
- Fixed when sprite is updated in the sprite editor, the spriteshape is not updated.
- Fixed cases where Spline Edit is disabled even when points are selected. (https://forum.unity.com/threads/spriteshape-preview-package.522575/#post-3436940)
- Sprite with SpriteShapeBody Shader gets graphical artifacts when rotating the camera.
- When multiple SpriteShapes are selected, Edit Spline button is now disabled. (https://forum.unity.com/threads/spriteshape-preview-package.522575/page-3#post-3764413)
- Fixed texelSize property (https://forum.unity.com/threads/spriteshape-preview-package.522575/page-4#post-3877081)
- Fixed Collider generation for different quality levels. (https://forum.unity.com/threads/spriteshape-preview-package.522575/page-4#post-3956062)
- Fixed Framing Issues (https://forum.unity.com/threads/spriteshape-preview-package.522575/page-5#post-4137214)
- Fixed Collider generation for Offsets (https://forum.unity.com/threads/spriteshape-preview-package.522575/page-5#post-4149841)
- Fixed Collider generation for different Heights (https://forum.unity.com/threads/spriteshape-preview-package.522575/page-5#post-4190116)

### Changed
- SpriteShape Asset parameters WorldSpace UV, PixelPerUnit have been moved to SpriteShapeController properties.
- Collider generation has been simplified and aligns well with the generated geometry (different height, corners etc.)

### Removed
- Remove redundant parameters BevelCutoff and BevelSize that can be done by simply modifying source spline.

## [1.0.12-preview.1] - 2018-08-03
### Added
- Fix issue where Point Positions do not update visually at runtime for Builds

## [1.0.11-preview] - 2018-06-20
### Added
- Fix Spriteshape does not update when Sprites are reimported.
- Fix SpriteShapeController in Scene view shows a different sprite when user reapplies a Sprite import settings
- Fix Editor Crashed when user adjusts the "Bevel Cutoff" value
- Fix Crash when changing Spline Control Points for a Sprite Shape Controller in debug Inspector
- Fix SpriteShape generation when End-points are Broken.
- Fix cases where the UV continuity is broken even when the Control point is continous.

## [1.0.10-preview] - 2018-04-12
### Added
- Version number format changed to -preview

## [0.1.0] - 2017-11-20
### Added
-  Bezier Spline Shape
-  Corner Sprites
-  Edge variations
-  Point scale
-  SpriteShapeRenderer with support for masking
-  Auto update collision shape
