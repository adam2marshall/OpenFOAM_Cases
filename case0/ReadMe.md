# Case 0 command list

## Geometry
Export the geometry from Onshape as individual STLs and rename them to remove the front part of the filename so you are left with "BW.stl" for example

## Commands

#### Clean things up:
foamCleanPolyMesh
foamCleanTutorials

#### Mesh:
blockMesh
surfaceFeatureExtract
snappyHexMesh
checkMesh

#### Sort out the patches
createPatch -dict system/createPatchDict0
createPatch -dict system/createPatchDict1
rm -rf constant/polyMesh/
cp -r 5/polyMesh/ constant/
rm -rf 5/ 4/ 3/ 2/ 1/

#### Run!
cp -r 0.org/ 0



